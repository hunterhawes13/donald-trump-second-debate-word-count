## Synopsis

I made a word count for each word and the number of occurances that Donald Trump said it in the 2nd presidential debate.

"The top 100 words are:

the - 150 occurances

and - 120 occurances

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

// lets see what donny had to say
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

FULL RESULTS

the - 150 occurances

and - 120 occurances

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

tax - 8 occurances

ive - 8 occurances

which - 8 occurances

can - 8 occurances

could - 8 occurances

why - 8 occurances

now - 8 occurances

talk - 8 occurances

done - 8 occurances

there - 8 occurances

well - 8 occurances

more - 7 occurances

obama - 7 occurances

getting - 7 occurances

two - 7 occurances

out - 7 occurances

disaster - 7 occurances

into - 7 occurances

words - 7 occurances

russia - 7 occurances

senator - 7 occurances

some - 7 occurances

got - 7 occurances

should - 7 occurances

interest - 6 occurances

pay - 6 occurances

allowed - 6 occurances

percent - 6 occurances

thing - 6 occurances

right - 6 occurances

first - 6 occurances

health - 6 occurances

come - 6 occurances

something - 6 occurances

number - 6 occurances

world - 6 occurances

isis - 6 occurances

those - 6 occurances

took - 6 occurances

lot - 6 occurances

he - 6 occurances

big - 6 occurances

seen - 6 occurances

judgment - 6 occurances

fact - 5 occurances

state - 5 occurances

important - 5 occurances

sanders - 5 occurances

take - 5 occurances

subpoena - 5 occurances

respect - 5 occurances

massive - 5 occurances

expensive - 5 occurances

america - 5 occurances

theyre - 5 occurances

fine - 5 occurances

campaign - 5 occurances

name - 5 occurances

made - 5 occurances

wont - 5 occurances

horrible - 5 occurances

obamacare - 5 occurances

wants - 5 occurances

carried - 5 occurances

care - 5 occurances

numbers - 5 occurances

money - 5 occurances

problem - 5 occurances

change - 5 occurances

ill - 4 occurances

proud - 4 occurances

room - 4 occurances

am - 4 occurances

raising - 4 occurances

respond - 4 occurances

difference - 4 occurances

talks - 4 occurances

locker - 4 occurances

iraq - 4 occurances

much - 4 occurances

actually - 4 occurances

bring - 4 occurances

everything - 4 occurances

office - 4 occurances

than - 4 occurances

bernie - 4 occurances

commercials - 4 occurances

class - 4 occurances

give - 4 occurances

frankly - 4 occurances

happen - 4 occurances

insurance - 4 occurances

congress - 4 occurances

youre - 4 occurances

time - 4 occurances

government - 4 occurances

who - 4 occurances

code - 4 occurances

only - 4 occurances

by - 4 occurances

plan - 4 occurances

whether - 4 occurances

saying - 4 occurances

rid - 4 occurances

most - 4 occurances

lines - 4 occurances

millions - 4 occurances

around - 4 occurances

ago - 4 occurances

sheet - 4 occurances

same - 4 occurances

him - 4 occurances

trump - 4 occurances

inner - 3 occurances

competition - 3 occurances

tremendous - 3 occurances

let - 3 occurances

lowering - 3 occurances

single - 3 occurances

trade - 3 occurances

report - 3 occurances

different - 3 occurances

fair - 3 occurances

billion - 3 occurances

nobodys - 3 occurances

bringing - 3 occurances

almost - 3 occurances

corporations - 3 occurances

leaving - 3 occurances

us - 3 occurances

far - 3 occurances

provisions - 3 occurances

word - 3 occurances

little - 3 occurances

four - 3 occurances

then - 3 occurances

nothing - 3 occurances

reason - 3 occurances

wrong - 3 occurances

radical - 3 occurances

here - 3 occurances

tonight - 3 occurances

maybe - 3 occurances

islamic - 3 occurances

border - 3 occurances

help - 3 occurances

absolutely - 3 occurances

way - 3 occurances

three - 3 occurances

facts - 3 occurances

deal - 3 occurances

talking - 3 occurances

even - 3 occurances

down - 3 occurances

letter - 3 occurances

law - 3 occurances

heard - 3 occurances

today - 3 occurances

ashamed - 3 occurances

youve - 3 occurances

endorsed - 3 occurances

apology - 3 occurances

doesnt - 3 occurances

believe - 3 occurances

last - 3 occurances

middle - 3 occurances

gotten - 3 occurances

prosecutor - 3 occurances

need - 3 occurances

safe - 3 occurances

special - 3 occurances

before - 3 occurances

friends - 3 occurances

such - 3 occurances

donors - 3 occurances

these - 3 occurances

havent - 3 occurances

africanamericans - 3 occurances

opinion - 3 occurances

off - 3 occurances

effective - 3 occurances

post - 3 occurances

old - 3 occurances

balance - 3 occurances

san - 2 occurances

depreciation - 2 occurances

putin - 2 occurances

muslims - 2 occurances

embarrassed - 2 occurances

terror - 2 occurances

hate - 2 occurances

sure - 2 occurances

ever - 2 occurances

politician - 2 occurances

allow - 2 occurances

good - 2 occurances

example - 2 occurances

knock - 2 occurances

facebook - 2 occurances

between - 2 occurances

use - 2 occurances

social - 2 occurances

able - 2 occurances

total - 2 occurances

certain - 2 occurances

justice - 2 occurances

cases - 2 occurances

deficit - 2 occurances

strong - 2 occurances

cutting - 2 occurances

payer - 2 occurances

lower - 2 occurances

companies - 2 occurances

including - 2 occurances

says - 2 occurances

changed - 2 occurances

bigger - 2 occurances

fixing - 2 occurances

lincoln - 2 occurances

making - 2 occurances

abraham - 2 occurances

run - 2 occurances

better - 2 occurances

too - 2 occurances

advantage - 2 occurances

latinos - 2 occurances

lied - 2 occurances

hispanics - 2 occurances

lie - 2 occurances

question - 2 occurances

finished - 2 occurances

dollars - 2 occurances

minutes - 2 occurances

person - 2 occurances

coming - 2 occurances

famous - 2 occurances

blaming - 2 occurances

bill - 2 occurances

everybody - 2 occurances

year - 2 occurances

worse - 2 occurances

agree - 2 occurances

sounds - 2 occurances

his - 2 occurances

action - 2 occurances

understand - 2 occurances

hundreds - 2 occurances

soros - 2 occurances

anybody - 2 occurances

goes - 2 occurances

honest - 2 occurances

writeoff - 2 occurances

wealth - 2 occurances

abusive - 2 occurances

nations - 2 occurances

attacked - 2 occurances

letting - 2 occurances

jobs - 2 occurances

giving - 2 occurances

wonderful - 2 occurances

iran - 2 occurances

order - 2 occurances

raped - 2 occurances

folks - 2 occurances

yoga - 2 occurances

wedding - 2 occurances

force - 2 occurances

daughters - 2 occurances

email - 2 occurances

apologize - 2 occurances

cant - 2 occurances

lying - 2 occurances

lost - 2 occurances

okay - 2 occurances

new - 2 occurances

york - 2 occurances

family - 2 occurances

watching - 2 occurances

amazing - 2 occurances

meant - 2 occurances

american - 2 occurances

went - 2 occurances

form - 2 occurances

certainly - 2 occurances

honestly - 2 occurances

potential - 2 occurances

deduction - 2 occurances

cities - 2 occurances

area - 2 occurances

alive - 2 occurances

owe - 2 occurances

ones - 2 occurances

solve - 2 occurances

delete - 2 occurances

mention - 2 occurances

primary - 2 occurances

growth - 2 occurances

chose - 2 occurances

furious - 2 occurances

started - 2 occurances

along - 2 occurances

speak - 2 occurances

theres - 2 occurances

situation - 2 occurances

killed - 2 occurances

happening - 2 occurances

sent - 2 occurances

pictures - 2 occurances

hand - 2 occurances

buffett - 2 occurances

warren - 2 occurances

general - 2 occurances

michelle - 2 occurances

provision - 2 occurances

attorney - 2 occurances

always - 2 occurances

id - 2 occurances

deductions - 2 occurances

race - 2 occurances

square - 2 occurances

unlike - 2 occurances

loans - 2 occurances

problems - 2 occurances

high - 2 occurances

wounded - 2 occurances

wikileaks - 2 occurances

saw - 2 occurances

bernardino - 2 occurances

hacking - 2 occurances

acid - 2 occurances

deleted - 2 occurances

russians - 2 occurances

apologizing - 2 occurances

donald - 2 occurances

paris - 1 occurance

devil - 1 occurance

surprised - 1 occurance

washed - 1 occurance

boxes - 1 occurance

week - 1 occurance

taken - 1 occurance

chance - 1 occurance

mind - 1 occurance

missing - 1 occurance

wassermanschultz - 1 occurance

won - 1 occurance

friend - 1 occurance

win - 1 occurance

instruct - 1 occurance

vicious - 1 occurance

involved - 1 occurance

long - 1 occurance

exactly - 1 occurance

weeks - 1 occurance

television - 1 occurance

lies - 1 occurance

deception - 1 occurance

manager - 1 occurance

hes - 1 occurance

longterm - 1 occurance

workers - 1 occurance

fbi - 1 occurance

winner - 1 occurance

real - 1 occurance

another - 1 occurance

blumenthal - 1 occurance

sidney - 1 occurance

watch - 1 occurance

bleach - 1 occurance

truth - 1 occurance

process - 1 occurance

lives - 1 occurance

destroyed - 1 occurance

fifth - 1 occurance

herself - 1 occurance

disgrace - 1 occurance

disgraceful - 1 occurance

ought - 1 occurance

youd - 1 occurance

jail - 1 occurance

yet - 1 occurance

point - 1 occurance

c - 1 occurance

document - 1 occurance

brings - 1 occurance

also - 1 occurance

whos - 1 occurance

jones - 1 occurance

paula - 1 occurance

practice - 1 occurance

license - 1 occurance

impeached - 1 occurance

girl - 1 occurance

laughing - 1 occurance

represented - 1 occurance

client - 1 occurance

yearsold - 1 occurance

woman - 1 occurance

viciously - 1 occurance

five - 1 occurance"


###"I know words, I have the best words, but their is no better word than stupid"
