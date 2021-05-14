# functional-programming-lesson

## 関数型プログラミング　用語集

- 純粋関数型言語  
関数型プログラミングに関する機能のみを備えた言語
- 関数  
関数型言語にとって関数とは「数学の関数とほぼ同じ仕組みを持ち、引数と戻り値を必ず持つ」という意味。従来の言語にとっては「ひとまとまりの手続きであり、引数と戻り値を強制しない」
- 命令文  
従来の言語での、プログラムの基本的な構成要素についての呼び方
- 式  
関数型言語での、プログラムの基本的な構成要素についての呼び方。関数型言語ではあらゆる値が式で構成され、式は必ず戻り値を持つ
- 命令型言語  
命令文で構成されるプログラミング言語のこと
- 実行する  
命令型言語での、命令文の扱われ方。「命令を-。」
- 評価する  
関数型言語での、式の扱われ方。「四季を-。」
- ラムダ式  
  
- 第一級関数  
関数を値として扱えるプログラミング言語の性質。
- 高階関数  
関数を引数として受け取ったり、関数を戻り値として返したりする巻数
- 部分適用  
2つ以上の引数を持つ関数に一部の引数を与えると、残りの引数を持つ別の関数を作成することができる、というプログラミング言語の機能
- カリー化  
  - 「複数の引数を取る関数」を「引数を1つだけ取る関数」を使って順次表現すること
  - 「複数の引数を持つ関数」を、「『元の関数の第1引数』を引数とし、『元の残りの引数を引数として結果を返す関数』を戻り値とする関数」にすること
- 関数合成  
複数の関数をまとめて別の関数を作成する可能なプログラミング言語の機能。
- 副作用  
関数型言語において、引数から戻り値を求めること以外の仕事
- 不変性  
  
- 代入  
命令形言語において、変数に値を代入すること
- 束縛  
関数型言語において、変数に値を代入すること
- 参照透過性  
副作用がない関数は、引数が同じなら戻り地は必ず同じになる
- 遅延評価  
必要になった時点で初めて関数屋敷を評価すること。副作用を起こさないことによエイ、遅延評価方式を実現できる。
- 再帰処理  
関数の中からその関数自身を呼び出す仕組み
- パターンマッチ  
引数に応じて、場合分けして関数を定義する仕組み
- 型推論  
変数や関数の方を宣言しなくても、コンパイラが自動的に方を判定する仕組み。
- 多相性  
不特定多数の方に適用できる汎用的な関数を作るための仕組み
- 型変数  
どんな型でも取り入れることが可能な型
- 多相型  
型変数を使って定義した型のこと
- 等式推論  
  
- 単一責任  
  
- シノニム  
同義語という意味
- ヘテロ  
「異なる」、「別の」、「他の」などという意味
  
- 関数型言語とオブジェクト指向言語の比較
  |  | 関数型 | オブジェクト指向 |
  | :--: | -- | -- |
  | 合成の単位 | 関数 | オブジェクト(クラス) |
  | プログラミングスタイル | 宣言型 | 命令型 |
  | データと振る舞い | 純粋で独立した関数との緩い結合 | クラス内でメソッドと強い結合 |
  | 状態管理 | オブジェクトを不変値として扱う | インスタンスメソッドを利用してオブジェクトの変数を行う |
  | フロー制御 | 関数と再帰 | ループと条件分岐 |
  | スレッド安全性 | 並列プログラミングが可能 | 実現が困難 |
  | カプセル化 | 全てが不変のため不変 | データの整合性を保つために必要 |

- JavaScriptでの実装
```JavaScript
// カリー化
const add = x => y => z => x + y + z;
console.log(add(1)(2)(3));  // -> 6
```
