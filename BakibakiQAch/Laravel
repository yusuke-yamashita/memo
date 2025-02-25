---
marp: true
theme: default
---

# テスターがLaravelのFeature TestとUnit Testについて調べた
2025/3/14(金)
やました

---

## 自己紹介

- テスター
- 4月から外資系QA
- PHPerとしてはアマチュア

---

プロのテスター（アマチュアプログラマー）がLaravelのテストについて
解釈してみたという話

**Feature Testの訳語に違和感が合った**

「これは違うよ」ってことがあれば教えて欲しい

---

## Laravelのテスト

- Laravelはデフォルトでtestが実装されている
- `tests/Feature`ディレクトリと`tests/Unit`ディレクトリ
- 技術的な制約で区別しているわけではないっぽい
    - その気になればtests/UnitにFeatureテストをコードを書いても動きそう(あとで調べる)
    - とはいえ、分けることには理由があると思った

---

## Feature Testとは？

> Feature tests test larger portions of your codebase, including the interaction of several objects with each other or even a complete HTTP request to your application.Generally, feature tests exercise a larger slice of your code and often include database interactions. 

> フィーチャテストは、コードベースのより大きな部分、例えば複数のオブジェクト間の相互作用や、アプリケーションへの完全なHTTPリクエストなどをテストします。一般的に、フィーチャテストはコードのより広い範囲を対象とし、データベースとのやり取りを含むことが多いです。

---

## Unit Testとは？

> Unit tests are focused on testing very small, isolated portions of your code. You want to determine if a single method is performing as expected very reliably and quickly. 

> ユニットテストは、コードの非常に小さく、独立した部分をテストすることに焦点を当てています。単一のメソッドが期待どおりに、非常に信頼性が高く、迅速に動作するかどうかを判断したいと考えます。

---

## Feature TestとUnit Testの違い
||Feature Test|Unit Test|
|---|---|---|
|スコープ|複数の部品を結合（大きい）|単体の部品の動作(小さい)|
|実行速度|比較的低速|高速|
|依存|高い|低い|
|ベース|外部仕様など|コード|
|例|HTTPリクエスト、APIなど|関数の返り値|

---

## 「テストレベル」という考え方
- 単体テスト、結合テスト、システムテストとか
- テストレベルを識別する統一的な見解はまだないが、典型的に「システムの結合度」で判断することが多い

**機能テストはテストレベルではない**

## 「テストタイプ」という考え方
- 機能テスト、非機能テスト(性能テスト、負荷テストetc)とか
- 統一的な（略）テストが担保する品質特性で判断することが多い

**機能テストはテストタイプです**

---

## LaravelはFeature testを「機能テスト」って呼んでいる？
- 本とかサイトでは「機能テスト」という訳語を当てている場合があるが、php界隈で統一された見解かは不明

---

## Feature Testを「機能テスト」と捉えると変に思うテスターがいる

- Feature Testを「機能テスト」と訳すと、Functional Test(機能性のテスト)とかぶってしまう
- 単体レベルの機能テスト、結合レベルの機能テスト、システムレベルの機能テストがあると捉えるのがテスト界隈の整理ではある
- LaravelにおけるFeature Testは、**Laravelアプリケーションの複数のコンポーネントが連携した状態での機能性を検証するテスト**であると理解すると、より本質を捉えられるはず

---


## テストレベルを識別する意味

例の一枚絵を貼る
メリットを書く


---

## まとめ

- Feature TestとUnit Testは、それぞれ異なる目的を持つテストであるので、目的意識を持って使い分けよう
- Feature Testは「機能テスト」ではなく、「統合テスト」と捉えるのがだと思う
- テストレベルを識別するとfun testingになれるかも
