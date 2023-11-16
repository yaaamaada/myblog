# Rustの疑似乱数生成で使用されるデフォルト値
# はじめに
* ソフトウェアによって生成される乱数は何らかのアルゴリズムに従って生成されるため，真にランダムではない
* なので，その影響は許容できるのか気になって調べた
    * とりあえずRustに関して調べた
        * 乱数を使用するプログラムをRustで書いているため
* 結論，CSPRNG（Cryptographically secure pseudo-random number generator: 暗号的に安全な疑似乱数生成器）であれば，通常問題ない
    * Rustではデフォルト値がそうなっている
        * ただし`thread_rng()`を使用して乱数を生成する場合の話

# メモ
* Rustにおけるデフォルト値
    * アルゴリズム：ChaCha12
        * CSPRNGのひとつ
        * シード値に256bit以上の値を指定すればよさげ
    * シード値：OS（ハードウェア？）から獲得
        * サイズは毎回64kiB（キビバイト）
    * ソース
        * [thread_rng()のドキュメント](https://rust-random.github.io/rand/rand/fn.thread_rng.html)
            * [struct ThreadRngのドキュメント](https://rust-random.github.io/rand/rand/rngs/struct.ThreadRng.html)

# おわりに
参考資料のセクションにあるStack Overflowのおかげで調べられました．
リファレンスがリファレンスを呼ぶので，それぞれの内容をひとつずつ見ていった次第です．

# 参考資料
* [random - What is the PRNG algorithm used in Rust's `rand` crate? - Stack Overflow](https://stackoverflow.com/questions/70392284/what-is-the-prng-algorithm-used-in-rusts-rand-crate)
* [rand - Rust](https://docs.rs/rand/latest/rand/)
    * [Introduction - The Rust Rand Book](https://rust-random.github.io/book/intro.html)
        * [Our RNGs - The Rust Rand Book](https://rust-random.github.io/book/guide-rngs.html)
