# useEffect の使用を避ける

useEffect は外部システムとの同期のみに使用。それ以外は使わない。

## 使ってはいけない場面

### レンダリング中に計算できること
```typescript
// NG
const [fullName, setFullName] = useState('');
useEffect(() => {
  setFullName(firstName + ' ' + lastName);
}, [firstName, lastName]);

// OK
const fullName = firstName + ' ' + lastName;
```

### ユーザーイベントの処理
```typescript
// NG
useEffect(() => {
  if (product.isInCart) {
    showNotification(`Added!`);
  }
}, [product]);

// OK
function handleBuyClick() {
  addToCart(product);
  showNotification(`Added!`);
}
```

### 重い計算のキャッシュ
```typescript
// NG
useEffect(() => {
  setVisibleTodos(getFilteredTodos(todos, filter));
}, [todos, filter]);

// OK
const visibleTodos = useMemo(
  () => getFilteredTodos(todos, filter),
  [todos, filter]
);
```

### prop 変更時の状態リセット
```typescript
// NG
useEffect(() => {
  setComment('');
}, [userId]);

// OK: key でリセット
<Profile userId={userId} key={userId} />
```

## 使うべき場面

- 外部システムとの同期（WebSocket、ブラウザ API、サードパーティライブラリ）
- コンポーネントの表示自体がトリガーとなる処理（画面表示時のアナリティクス送信など）

**原則**: イベントで処理できることはイベントハンドラで、計算できることはレンダリング中に行う。
