# Simple Kata Tester

I often set up katas for people with different backgrounds. For this purpose I made this script with the following requirements:

- Work out of the box in any Unix environment
- Work with standard input and output so you can use any language you want
- Simple, stupid test format so anyone can understand and modify them

Then I just ship my katas as a pack with the tester, existing tests and people can start playing with it even if they're not familiar with a test framework

It's quite limited, if you need more complete tests at a bash level, I suggest you to take a look at the excellent bats-core project here: [https://github.com/bats-core/bats-core](https://github.com/bats-core/bats-core)

## Installation

Copy the script in your project

As an alternative, you can also add this repository as a git submodule

## Usage

1. Write a test sample file

```bash
# You can add comments to your tests
# The test are described in the following format:
# standard_input_content:expected_standard_output_content

# Here we're testing the bc calculator
:
1+1:2
2*5:11
```

2. Run the tester. The first parameter is the tested executable. The second parameter is the sample file

```bash
./simple_kata_tester.sh /usr/bin/bc tests_sample.txt
```

3. See the results!

```
OK with input='' 
OK with input='1+1' 
KO with input='2*5' (obtained='10', expected='11')
============================================================
    Results : 1/3 tests failed
```

## Contributing

If you want to contribute, you're more than welcome! :-)

## Licence

WTFPL

