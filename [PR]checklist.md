# PR セルフレビュー チェックリスト

## 共通

- [ ] スペルミスがないか
- [ ] デッドコードや console.log、コメントアウトが残っていないか
- [ ] インデントを修正したか

## バックエンド

### N+1

- [ ] 別ターミナルを開いて tail -f log/development.log を表示し、同じような SQL が出ていないか確認する。

### 例外

- [ ] エラー時の挙動を考慮したか

### Rspec

## フロントエンド

### tara

- persisted-queries は 1 個だけ？

### CSS

- [ ] 最上位の要素に margin を書いていないか
- [ ] p, span などの要素セレクターに直接 CSS を書いていないか
- [ ] クラスセレクタをネストしていないか
- [ ] class 名の命名は BEM 方式になっているか
  - Block: それが何であるか(例: Menu, Button など)
  - Element: Block を構成する要素で、Block の外では独立して使用できないもの
  - Modifier: Block や Element の見た目、状態、振る舞いを定義するもの

### lint

### storybook
