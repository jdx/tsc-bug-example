This repo demonstrates a bug with tsc.

Setup:
```
git clone https://github.com/jdxcode/tsc-bug-example
cd tsc-bug-example
npm i
```

This fails on the last step and shows the bug that `tsc` does not generate the `./lib` files:

```
./node_modules/.bin/tsc
rm -rf lib
./node_modules/.bin/tsc
ls lib
```

This makes it work again:

```
rm tsconfig.tsbuildinfo
./node_modules/.bin/tsc
ls lib
```
