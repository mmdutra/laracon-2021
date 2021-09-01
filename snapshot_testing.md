# An instroduction to snapshot testing

### What is Snapshot testing?

Test succeeds if the output matches the snapshot
If not, the thes will fail

### How can we do it in PHP?

- [phpunit-snapshot-assertions](https://github.com/spatie/phpunit-snapshot-assertions)
- [pest-plugin-snapshot](https://github.com/spatie/pest-plugin-snapshots)


### Advantages 
- Very easy to get start with
- Can be used to validate complex output
- Easily update all the tests in one go

### Disavantages 
- Brittle
- Hard to pinpoint exact point of failure 
- Bugs can be easily written in the snapshots