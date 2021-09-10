# Missing Seed Word

You have a 12 word, BIP39 seed phrase, such as for a Tezos wallet. But you've lost one of the words!! And you don't know what position the missing word should go in!!

This script helps generate valid seed phrases using the 11 words that you still have. You'll find about 1,500 phrases are valid out of a total of about 22,000 phrases. (BIP39 uses a checksum, so not all possible phrases are "valid").

## Prerequisites

### Install python and pip

Install python3 and pip3.

#### MacOS

First install [homebrew](https://brew.sh/). Then install python (it includes pip).

```
brew install python
```

#### Other OS

You are on your own!

### Clone this repository.

```
git clone https://github.com/idlebit1/missing-seed-word.git
```

## Usage

### Verify the word list.

First, open `script.py` in a text editor. Make sure the `word_lang` and `word_blob` are correct.

### Install mneumonic

Open a terminal window, and install the BIP39 library `mnemonic`.

```
pip3 install mnemonic
```

### Run the script

Then run the script. Put your 11 words in the command line arguments. For example:

```
python3 script.py repeat gentle job foster flight mammal spread nut case document bar
```

It will print all of the valid phrases and some stats. For example:

```
absorb repeat gentle job foster flight mammal spread nut case document bar
abstract repeat gentle job foster flight mammal spread nut case document bar
acoustic repeat gentle job foster flight mammal spread nut case document bar
acquire repeat gentle job foster flight mammal spread nut case document bar
...
repeat gentle lizard job foster flight mammal spread nut case document bar
repeat gentle lunch job foster flight mammal spread nut case document bar
repeat gentle magic job foster flight mammal spread nut case document bar
...

Valid candidates: 1554
Total: 24576
```
