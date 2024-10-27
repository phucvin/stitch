cd ..

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

. "$HOME/.cargo/env"

cargo build --release

```
$ cargo bench
...
Benchmarking fib_rec: Warming up for 3.0000 s
Warning: Unable to complete 100 samples in 5.0s. You may wish to increase target time to 404.3s, or reduce sample count to 10.
fib_rec                 time:   [3.9674 s 4.0249 s 4.0975 s]
...
```

```
$ time cargo run --release test/fib32.wasm fib 40
102334155
real    0m6.987s
user    0m6.331s
sys     0m0.020s
```