# [cauldera](https://github.com/aaronjones111/cauldera/releases)
Distillations, expansions and riffs on Rocktastic

Why cauldera? As potent as I've found rocktastic to be, and wickedly effective using PACK has been, I picture the gargantuon results of their combination to be a massive, simmering pool of doom. Like Yellowstone.
## wot
[Rocktastic12a](https://labs.nettitude.com/tools/rocktastic/) is an awesome wordlist. It is an absolute beast. 

PACK is an amazing tool for extracting patterns and increasing yer cracks. 

Did you ever wonder what might happen if you could actually run [PACK](https://github.com/iphelix/pack) rulegen against something this huge?

Me too.

It took about 5 days to finish and promptly crapped itself on analyzing 310 gigs of rules. 

Thats about 23 times the size of Rocktastic itself. 

If we're liberal with estimates, that's about 230 billion rules...

Anyways, it involved a rediculous amount rules and gigantic files. I hope you find the results as interesting and useful as I have.


## some stats
*Top 10 Words*

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

*Top 10 Rules (leaving out :)*

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

## now
It's still a work in progress, counting & uniquing the billions of rules that are present in the 7-10 combo sets is a 'bigdata' problem I'm bumbling through. SO, instead of just sitting on everything perpetually I thought I'd release an incomplete, yet still VERY USEFUL collection.

There are 7z files of the 1-6 rulesets, as well as the basewords. Sorted, uniqued, and counted, formated as such:
```
739684 <<div>> sa@ $@ $1
724181 <<div>> sa@ $@ $3
719557 <<div>> sa@ $@ $2
```
Before you ask, I used ```" <<div>> "``` as the count & value separator becasue I wasn't sure what the hell might actually end up in the rules.
 
## future
I'm in the process of running [pcfg_cracker](https://github.com/lakiw/pcfg_cracker) (another amazing tool) against Rocktastic to experiment with that. 


## get it
### https://github.com/aaronjones111/cauldera/releases
