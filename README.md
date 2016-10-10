## Synopsis

I made a word count for the top 100 words Donald Trump said in the 2nd dresidential debate

## Code Example
```
var text = "";
var wordRegExp = /\w+(?:'\w{1,2})?/g;
var words = {};
var matches;
while ((matches = wordRegExp.exec(text)) != null)
{
    var word = matches[0].toLowerCase();
    if (typeof words[word] == "undefined")
    {
        words[word] = 1;
    }
    else
    {
        words[word]++;
    }
}

// Sort 'em!
var wordList = [];
for (var word in words)
{
    if (words.hasOwnProperty(word))
    {
        wordList.push([word, words[word]]);
    }
}
wordList.sort(function(a, b) { return b[1] - a[1]; });

// Come back any time, straaanger!
var n = 100;
var message = ["The top " + n + " words are:"];
for (var i = 0; i < n; i++)
{
    message.push(wordList[i][0] + " - " + wordList[i][1] + " occurance" +
                 (wordList[i][1] == 1 ? "" : "s"));
}
```

## Motivation

Curosity by the frequency of hearing repetitive words from Donald Trump  




## Contributors

Hunter Hawes
github: hunterhawes13
twitter: @tikishackfun

## License

This project is licensed under the terms of the MIT license.

## Results 

"The top 100 words are:

the - 150 occurances
---
and - 120 occurances
---
to - 103 occurances

i - 90 occurances

you - 81 occurances

a - 76 occurances

of - 72 occurances

that - 69 occurances

it - 54 occurances

she - 51 occurances

have - 47 occurances

is - 43 occurances

we - 41 occurances

in - 40 occurances

for - 37 occurances

so - 34 occurances

but - 33 occurances

this - 33 occurances

going - 32 occurances

was - 29 occurances

were - 28 occurances

because - 27 occurances

they - 26 occurances

people - 26 occurances

its - 25 occurances

on - 25 occurances

about - 24 occurances

do - 23 occurances

be - 23 occurances

country - 23 occurances

know - 23 occurances

at - 21 occurances

when - 21 occurances

are - 20 occurances

with - 20 occurances

been - 19 occurances

one - 19 occurances

very - 18 occurances

hillary - 18 occurances

things - 18 occurances

im - 18 occurances

not - 17 occurances

all - 17 occurances

them - 17 occurances

has - 17 occurances

her - 17 occurances

shes - 17 occurances

from - 16 occurances

say - 16 occurances

what - 16 occurances

our - 16 occurances

like - 15 occurances

think - 15 occurances

many - 14 occurances

taxes - 14 occurances

great - 14 occurances

just - 14 occurances

never - 13 occurances

bad - 13 occurances

where - 13 occurances

if - 13 occurances

want - 13 occurances

said - 13 occurances

dont - 13 occurances

me - 12 occurances

look - 12 occurances

your - 12 occurances

again - 11 occurances

didnt - 11 occurances

thats - 11 occurances

did - 11 occurances

had - 11 occurances

clinton - 11 occurances

my - 11 occurances

as - 10 occurances

see - 10 occurances

an - 10 occurances

back - 10 occurances

tell - 10 occurances

president - 9 occurances

states - 9 occurances

other - 9 occurances

years - 9 occurances

united - 9 occurances

women - 9 occurances

would - 9 occurances

get - 9 occurances

go - 9 occurances

or - 9 occurances

doing - 9 occurances

emails - 9 occurances

no - 9 occurances

after - 9 occurances

over - 9 occurances

their - 9 occurances

make - 8 occurances

really - 8 occurances

up - 8 occurances

anything - 8 occurances

will - 8 occurances"

