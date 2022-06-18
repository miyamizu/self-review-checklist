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

## プリミティブ値

- 文字列、数値、審議地、BigInt, null, undefined, シンボル

## TS の数値型の特徴

- number 型は整数と小数の区別がない

## 数値リテラル

- TS における数値は IEEE754 倍精度浮動小数点数である(他の言語でよく言われる、double 型相当)

```
const binary = 0b1010; //2進数リテラル
const octal = 0o755; //8進数リテラル
const hexadecimal = 0xff; //16進数リテラル

// 10 493 255 と表示される
console.log(binary, octal, hexadeximal)
```

```
const big = 1e8;
const small = 4e-5;

// 100000000 0.00004と表示される
console.log(big, small)
```

## 任意精度整数(BigInt)

- 任意精度（どれだけ大きな数腕も誤差なく表すことができる）の整数

## 文字列型と 3 種類の文字列リテラル

```
const str1: string = "Hello";
const str2: string = "world!";
console.log(`${str1},${str2}`) //Hello, world!と表示される
```

## 真偽値と真偽値リテラル

- true と false は「値」である

## null と undefined

- どちらも「データがない」という意味
- 本書では undefined がおすすめ
- でもコンポーネントとかは null で返すことが多い

### プリミティブ型同士の変換

- 暗黙の型変換について
- TS には、変数の型を自動的に判断してくれる、型推論という機能がある。

### NaN

- 数値型の特殊な値
- 数値が必要な場面で数値が得られなかった場合に出現する

### 演算子

- - - - / % `**`
- 文字列の結合+演算子
- 比較演算子について。==と!=は基本的には使わない。
- ==と===の違いについて

```
const str: any = "3";

// true　文字列が数値に変換される
console.log(str == 3);

// false
console.log(str === 3);
```

- 論理演算子

```
&&
||
!123 //false
!null //true

// 「データがない」状況と「空文字列がある」状況を区別したいときは、||より??が適している
const secret = process.env.SECRET ?? "default";
console.log(`secretは${secret}です`);
```

## FizzBazz

```
for (let i = 1; i < 100; i++) {
  if (i%3 === 0 && i%5 === 0) {
    console.log('FizzBazz')
  } else if (i%3 === 0) {
    console.log('Fizz')
  } else if (i%5 === 0) {
    console.log('Bazz')
  } else {
    console.log(i);
  };
};
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
