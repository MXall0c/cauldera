# [cauldera](https://github.com/aaronjones111/cauldera/releases)
Distillations, expansions and riffs on Rocktastic

Why cauldera? As potent as I've found rocktastic to be, and wickedly effective using PACK has been, I picture the gargantuon results of their combination to be a massive, simmering pool of doom. Like Yellowstone.
## wot
[Rocktastic12a](https://labs.nettitude.com/tools/rocktastic/) is an awesome wordlist. It is an absolute beast. 

PACK is an amazing tool for extracting patterns and increasing yer cracks. 

Did you ever wonder what might happen if you could actually run [PACK](https://github.com/iphelix/pack) rulegen against something this huge?

Me too.

It took about 5 days to finish and promptly crapped itself on analyzing 310 gigs of rules. Actually, when I first tried I ran out of disk space, the second computer I tried it on ran out of memory. The third system I used had 280G of ram, and I still had to break it up into smaller files.

Thats about 23 times the size of Rocktastic itself. 

If we're liberal with estimates, that's about 230 billion rules...

Anyways, it involved a rediculous amount rules and gigantic files. I hope you find the results as interesting and useful as I have.

## PCFG set trained on Rocktastic
!!NEW!! 1/30/2020

I'm sharing a pcfg_cracker set trained on Rocktastic. It's a beast (natch).

It was trained with default settings, the wordlist unmodified. 

**Usage:**
1. Get a computer with at least 32G RAM (I'm not kidding)
2. Clone [pcfg_cracker](https://github.com/lakiw/pcfg_cracker)
3. Grab the trained set in my releases [here](https://github.com/aaronjones111/cauldera/releases)
4. Decompress & place in your ./pcfg_cracker/Rules directory 
5. Ram it into hashcat: 

```python3 ./pcfg_cracker/pcfg_guesser.py -r rock_pcfg | hc -O --stdin-timeout-abort 600 --potfile-path pottypotpot -a 0 -m 1000 ntlmhashes -r superrule.rule ```

Good luck!

## now
It's still a work in progress, counting & uniquing the billions of rules that are present in the 7-10 combo sets is a 'bigdata' problem I'm bumbling through. SO, instead of just sitting on everything perpetually I thought I'd release an incomplete, yet still VERY USEFUL collection.

There are 7z files of the 1-6 rulesets, as well as the basewords. Sorted, uniqued, and counted, formated as such:
```
739684 <<div>> sa@ $@ $1
724181 <<div>> sa@ $@ $3
719557 <<div>> sa@ $@ $2
```
Before you ask, I used ```" <<div>> "``` as the count & value separator becasue I wasn't sure what the hell might actually end up in the rules.

## some info & a strange theory
I find passwords absolutely fascinating. Cracking passwords is this crazy interesection of statistics and psychology that provides endless hours of entertainment. 

Passwords are like a private twitter, but pure, genuine and uncut. Folks will put all kinds of things in there that can reveal a lot about things they love, hate, and where they might just generally be mentally. You know, things like ```Nanaskitchen55@, #Mermaids4life``` or ```Welcomebackasshole1```.

It's with this in mind, that I thought it was interesting that in my cracking endeavors I've found far less derogatory and negative things than I expected (and I've scraped together a wordlist of all the hateful eyewatering insults, slurs, and swears I could find). No, by and large what I've found tends to be either fairly begnin or pretty positive (most used word in rocktastic is love, and other forms of it). 

Not sure what to make of it exactly, but I'm guessing the overall tone might be more accurate than whatever nonsense is happening on twitter.

## some stats
**Top 10 Words**

| hits    | word     |
|---------|----------|
| 1021688 | love     |
| 880061  | j        |
| 808611  | lover    |
| 744948  | Danielle |
| 731081  | lovey    |
| 722901  | loved    |
| 646556  | loves    |
| 641693  | mar      |
| 610015  | Daniel   |
| 590776  | lovesick |

**Top 10 Rules (leaving out ":" )**

| hits    | rule   |
|---------|--------|
| 1651097 | $1     |
| 1311148 | $3     |
| 1263231 | $2     |
| 1205592 | $@     |
| 1189417 | $@ $1  |
| 1175417 | $@ $3  |
| 1168649 | $@ $2  |
| 1136513 | $!     |
| 907113  | sa@ $1 |
| 768875  | sa@ $@ |

## get it
### https://github.com/aaronjones111/cauldera/releases
