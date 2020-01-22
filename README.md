# cauldera
Distillations, expansions and riffs on Rocktastic
## wot
[Rocktastic12a](https://labs.nettitude.com/tools/rocktastic/) is an awesome wordlist. It is an absolute beast. Ever wonder what might happen if you could actually run [PACK](https://github.com/iphelix/pack) against something this huge?

Me too.

It took about 5 days to finish and promptly crapped itself on analyzing 310 gigs of rules. Thats about 23 times the size of Rocktastic itself. 

If we're liberal with estimates, that's about 230 billion rules...

## now
It's still a work in progress, counting & uniquing the billions of rules that are present in the 7-10 combo sets is a 'bigdata' problem I'm bumbling through. SO, instead of just sitting on everything perpetually I thought I'd release an incomplete, yet still VERY USEFUL collection.

There are 7z files of the 1-6 rulesets, as well as the basewords. Sorted, uniqued, and counted, formated as such:
```
739684 <<div>> sa@ $@ $1
724181 <<div>> sa@ $@ $3
719557 <<div>> sa@ $@ $2
```
Before you ask, I used " <<dev>>> " as the count & value separator becasue I wasn't sure what the hell might actually end up in the rules.
 
## future
I'm in the process of running [pcfg_cracker](https://github.com/lakiw/pcfg_cracker) (another amazing tool) against Rocktastic to experiment with that. 
