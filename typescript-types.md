### Getting the type of the last item in a Tuple

```typescript
type GetLength<original extends any[]> = original extends { length: infer L } ? L : never
export type Prev<T extends number> = [-1, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62][T];

function tuple<T extends any[]>(...args: T): T[Prev<GetLength<T>>] {
    return args[args.length - 1];
}

const t1 = tuple("foo", 1, true);  // t1 = boolean
```
