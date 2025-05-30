# [Unix系] C Shell (csh) last コマンド: 最後のログイン情報を表示

## 概要
`last` コマンドは、システムにログインしたユーザーの履歴を表示します。このコマンドを使用することで、誰がいつログインしたかを確認することができます。

## 使用法
基本的な構文は以下の通りです。

```
last [options] [arguments]
```

## 一般的なオプション
- `-n [数]`: 表示するログイン履歴の数を指定します。
- `-R`: ホスト名を表示しません。
- `-f [ファイル]`: 指定したファイルからログを読み込みます。

## 一般的な例
以下にいくつかの実用的な例を示します。

- 最後のログイン情報を表示する基本的なコマンド:
  ```csh
  last
  ```

- 最近の5件のログイン情報を表示する:
  ```csh
  last -n 5
  ```

- 特定のユーザーのログイン履歴を表示する:
  ```csh
  last username
  ```

- ログファイルを指定して表示する:
  ```csh
  last -f /var/log/wtmp
  ```

## ヒント
- `last` コマンドは、システムのセキュリティ監視に役立ちます。定期的にログイン履歴を確認することをお勧めします。
- 出力が多くなる場合は、`less` コマンドと組み合わせてページング表示することができます。
  ```csh
  last | less
  ```
- 特定の期間や条件でフィルタリングしたい場合は、`grep` コマンドを使用することもできます。