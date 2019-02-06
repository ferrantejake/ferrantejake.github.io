# Notes on JavaScript style and practices

### Catching async errors using try/catch

This code will throw and error on line 2 and the try/catch will catch the error.

```javascript
async function throwError() {
    throw new Error('catch me!');
}

async function main() {
    try {
        await throwError();
    } catch (e) {
        console.log('caught error');
        console.log(e);
    }
}

main();
```
