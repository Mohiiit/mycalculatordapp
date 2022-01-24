# mycalculatordapp

anchor init <project_name>
cd <project_name>
anchor build
anchor test

although while running the anchor test, it failed and mentioned that ```Unable to start test validator. Check .anchor/test-ledger-log.txt for errors.
```

Then I tried to run the test-validator in a seperate terminal but that results me in a different error.

Then I tried: ```anchor test --skip-local-validator```

It ran the test but I got: ```Error: failed to send transaction: Transaction simulation failed: Attempt to load a program that does not exist```

So what I changed the program ID mentioned in the lib.rs and Anchor.toml.

How to get programID?
When you deploy(by using anchor deploy) your program, you will get the program ID.

After this the test passed and then I further developed the calulator logic, mainly in the lib.rs

After that, I wrote the test cases for every function I developed.
