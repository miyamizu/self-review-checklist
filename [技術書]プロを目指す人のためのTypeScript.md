## この本の対象者

- JavaScript を知らない人でも OK
- ただし他の言語を多少勉強した人向け

## この本について

- TypeScritp の体系的な理解とベストプラクティスの知識を与える
- あくまで TypeScript という言語そのものを解説する

## 1 章 イントロダクション

- TypeScript は、JavaScript に静的型付けを追加したプログラミング言語
- メリット 1: 型安全性 ... 間違ったコードを書いた際に、コンパイルエラーを出してくれる
- メリット 2: ドキュメント化と入力補完 ... 型の情報がソースコードに書かれているので、プログラムを読解する助けになる。
- TypeScritp が活きるのはコンパイル時。プログラムが実行されるときではない。

- TypeScript はあくまでも、JavaScript+型という様相の言語。そのため、最近の TS では、JavaScript にはない独自の機能は入れないことになっている。思想が違った初期の TS では、enum や namespace などの機能が実装されているが、複雑な挙動をするため、使うことは推奨されていない。

- https://www.typescriptlang.org/play に色々書いていく。

## 2 章 基本的な文法・基本的な型

### 式と文

```
const greeting = "Hello"; // 文
const text = greeting + "world"; // 文 ... 結果がない
console.log(text); //Hello, world! // 式 ... 結果がある
console.log(greeting + target); // 式文 ... 式の後にセミコロンを書く文
```

### 識別子

- \$, \_ ,先頭以外の大文字、大文字小文字が使える

### 型注釈

```
const 変数: 型 = 式; // :型の部分が型注釈
```

### let

- let は宣言時に値を代入しなくても良い
- let にも型をつけられる
- 絶対に let が必要だと断言できるとき以外、なるべく const を使う

```
let greeting: string, target: string;
greeting = "Hello, ";
target = "world!";
console.log(greeting + target);
```

## 3 章

## 4 章

## 5 章

## 6 章

## 7 章

## 8 章

## 9 章

```

```
