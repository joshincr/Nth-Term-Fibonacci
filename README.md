# N<sup>th</sup> Term of Fibonacci Sequence
![UI](https://user-images.githubusercontent.com/78969613/120752790-dbfb2d80-c527-11eb-91ad-2d8da2e8e201.png)

A simple and light-weight webpage where the user inputs an integer N and obtains the n<sup>th</sup> term of the Fibonacci sequence. The Fibonacci Sequence is a series of numbers where each number is the sum of the last two numbers, starting with 0 and 1. F<sub>n</sub> = F<sub>n-1</sub> + F<sub>n-2</sub>

### Test Cases handled:
* Calculates values that are way greater than Number.MAX_SAFE_INTEGER i.e. 9007199254740991 in JavaScipt (e.g. where N > 10000) using BigInt.
* Negative terms are also considered.
* Strings are disallowed and alert is raised if input is a floating-point number.

### References:
* [Fibonacci Sequence](https://www.mathsisfun.com/numbers/fibonacci-sequence.html)
* [BigInt - JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt)

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
