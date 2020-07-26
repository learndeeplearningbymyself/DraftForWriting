## Jest Architecture

For example with the command

```shell
jest my-test.js
```

We have:
- jest-cli
-- jest-config: figure out what person wants to do or what should happend on a CI environment, it takes the config information and the arguments. In this package, we have the function called **normalize**


