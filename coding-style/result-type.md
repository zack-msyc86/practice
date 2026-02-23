# Result 型

バックエンドやコアロジックでは Result 型を使う。ライブラリは [praha/byethrow](https://github.com/praha-inc/byethrow)。

## 理由

例外を throw すると、関数のシグネチャからエラーの存在が見えない。
Result 型なら成功/失敗が戻り値の型に現れるため、呼び出し側がエラーを無視できなくなる。
