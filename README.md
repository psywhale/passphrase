# passphrase

Generates a passphase of variable length and complexity. Based on Diceware Passphrase generation using EFF's short and long word lists

```bash
usage: wordlists.py [-h] [-s SEPARATOR] [-S] [-r char char] [-rc REPLACECOUNT]
                    [-C]
                    words

positional arguments:
  words                 Number of words to roll for or how long the phrase
                        will be

optional arguments:
  -h, --help            show this help message and exit

Word Separation options (optional):
  -s SEPARATOR, --separator SEPARATOR
                        Optional separator character between words.
  -S, --randseparator   Use a random separator between words

Replace Characters (optional):
  Replace characters in the phrase options

  -r char char, --replace char char
                        replace characters with another
  -rc REPLACECOUNT, --replacecount REPLACECOUNT
                        How many characters in the phrase to replace. Default
                        ALL
  -C                    RaNdom CapItaLiZe the phrase

```

You can a separator or use a random separator

```bash
$ python wordlists.py 4 -s "-"
sixth-wildcard-gala-cattishly

$ python wordlists.py 4 -S
manor*feast_acutely.sky

```

Replace characters 

```bash
$ python wordlists.py 4 -r a 4
educ4tedcontort4ppl4useflint

$ python wordlists.py 4 -r a 4 -s .
overjoyed.h4te.debit.drove

#only replace the first 3 characters
$ python wordlists.py 6 -r a 4 -rc 3 -s .
cro4k.joyfully.p4rtition.popper.s4ge.dragonfly

```

Random Capitalize as well and all of the above.

```bash

$ python wordlists.py 3 -C
StUnTrefurbIshZesty


$ python wordlists.py 6 -r o 0 -rc 3 -S -C
juice?gag-chaper0ne*happinesS*fr0nt-cRavinG



```