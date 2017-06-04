# A benchmark of Thai word tokenizers written in various programming languages

Date: 2017/06/04

The origin post was at https://veer66.wordpress.com/2017/01/19/benchmark-thai-word-tokenizers/ posted on 2017/01/19.

I wonder about speed of programs written in different languages. For example, I wonder whether one written in Kotlin and ran on JVM is slower than one written in Go. Although there are several existing benchmarks, this is one may be still important at least for me, because Thai word tokenizer is my real task.

So @iporsut and me wrote some programs in different programming languages and tried to optimize them.

I conducted the experiment on my laptop computer, which has Intel® Core™ i3-4030U CPU @ 1.90GHz × 4, on a 20MB Thai text corpus.  

| Lang | 1 (seconds) | 2 (seconds) | 3 (seconds) | AVG (seconds) |
|------|---|---|---|-----|
| Rust | 3.366 | 3.247 | 3.241 | 3.284 |
| Go   | 5.415 | 5.405 	| 5.416 | 5.412 |
| Crystal | 5.637 | 5.679 | 5.649 | 5.655 |
| Kotlin+Clojure | 6.547 | 6.743 | 6.628 | 6.639 |
| Julia | 38.316 | 38.112 | 38.237 | 38.221 |
| JavaScript | 49.349 | 49.084 | 49.901 | 49.445 |
| Python | 50.624 | 50.803 | 50.869 | 50.765 |
| Clojure+Kotlin |  63.502 | 67.561 | 67.303 | 66.122 |

## Additional setup

| Env | Source |
|-----|--------|
| Rust Nightly 2017-01-08 | [source](https://gitlab.com/veer66/chamkho) |
| Go 1.7.4 | [source](https://gitlab.com/veer66/mapkha) |
| Crystal 0.20.5 | [source](https://gitlab.com/veer66/kachet) |
| Kotlin 1.0.6 + Clojure 1.8.0 + OpenJDK 1.8 | [source](https://gitlab.com/veer66/yaito), [source](https://gitlab.com/veer66/yaito-clj) |
| Julia 0.5.0 | [source](https://gitlab.com/veer66/wordcut.jl) |
| Node.js v6.5.0 | [source](https://gitlab.com/veer66/prasae) |
| Python 3.5.2 |  [source](https://gitlab.com/veer66/wordocutpy) |
| Clojure 1.8.0 + Kotlin 1.0.6 + OpenJDK 1.8 | [source](https://gitlab.com/veer66/wordcut-clj) |

## Future work

@iporsut has already written multicore versions, so maybe next month I will conduct another experiment.