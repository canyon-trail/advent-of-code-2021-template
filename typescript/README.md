# Typescript Template

This is a quick start template for typescript testing. See `example.test.ts` for a simple example test.

## Installing and Running

You will need a working [Node Installation](https://nodejs.org/en/download/) in order to run this code. Afterwards, run this command:

```
npm install
```

## Project Layout & Tutorial

This project template has two files, `example.ts` and `example.test.ts`. The `example.ts` file has a simple function in it that adds two numbers. You can see it in action by using the command `npm start -- example.ts`:

```
> npm start -- example.ts
2 + 2 = 4
```

You can also run tests using either `npm run test` or `npm run test:watch`:

```
> npm run test

> test
> jest
 PASS  ./example.test.ts
  √ example 2 + 2 should equal 4 (2 ms)

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        0.668 s, estimated 1 s
Ran all test suites.
>
```

Try experimenting with the test in `example.test.ts` and changing `expect(example(2, 2)).toBe(4)` to `expect(example(2, 2)).toBe(5)` to get familiar with what test failures look like:

```
> npm run test

> test
> jest
 FAIL  ./example.test.ts
  × example 2 + 2 should equal 5 (4 ms)

  ● example 2 + 2 should equal 5

    expect(received).toBe(expected) // Object.is equality

    Expected: 5
    Received: 4

      2 |
      3 | test('example 2 + 2 should equal 5', function () {
    > 4 |       expect(example(2, 2)).toBe(5);
        |                             ^
      5 | });
      6 |

      at Object.<anonymous> (example.test.ts:4:24)

Test Suites: 1 failed, 1 total
Tests:       1 failed, 1 total
Snapshots:   0 total
Time:        0.804 s, estimated 1 s
Ran all test suites.
>
```
