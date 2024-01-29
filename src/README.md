# Jest: Exceeded Timeout of 5000 ms for a Test

Encountering this error during test runs led me to the decision to address it by adding a timeout value to the test case. After experimenting with a few values, 7000 ms emerged as the optimal choice, and hoorah! 🎉 The test passed.

On another day, rerunning the tests revealed that the same test now failed with a timeout error:

```
Thrown: "Exceeded timeout of 7000 ms for a test.
    Add a timeout value to this test to increase the timeout if it's a long-running test. See https://jestjs.io/docs/api#testname-fn-timeout."
```

Additionally, a couple more errors appeared for other tests:

```
Thrown: "Exceeded timeout of 5000 ms for a test.
    Add a timeout value to this test to increase the timeout if it's a long-running test. See https://jestjs.io/docs/api#testname-fn-timeout."
```

Now, one test failed for a 7000 ms timeout and two others for a 5000 ms timeout. After trial-testing with different values, settling on 10000, 7000, 8000 seemed to solve the issue! 🎉🎉

But wait! Had I truly conquered the battle against Jest test timeouts? Not quite. I found myself grappling with recurring situations, requiring me to engage in manual trial-tests and tweak values in specific test cases. The frustration didn't end there, the tests sometimes passed with different timeout values in distinct environments, such as my peers' machines. This inconsistency in test outcomes not only slowed down code review and delivery processes but also proved to be a bottleneck in CI implementation. It impeded from smoothly pushing codes, and this became painfully annoying.

So, what's the key to finally triumphing over these pesky Jest test timeouts? The adventure continues in my next note post, where I explore overall concept of [Configuring Jest test timeouts.](configuring-jest-test-timeouts.md) Discover the strategies that saved the day 😉.
