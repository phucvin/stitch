cd ..

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

. "$HOME/.cargo/env"

cargo build --release

cargo bench

```
$ time cargo run --release test/fib32.wasm fib 40
102334155
real    0m6.987s
user    0m6.331s
sys     0m0.020s
```