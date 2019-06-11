reproduction:

```
git clone https://github.com/jdxcode/tsc-bug-example
cd tsc-bug-example
npm i

./node_modules/.bin/tsc
ls lib # errors because tsc is not generating ./lib

rm tsconfig.tsbuildinfo
./node_modules/.bin/tsc
ls lib # works
```
