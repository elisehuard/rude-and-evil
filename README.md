# Rude and Evil

In this project I try to develop a classifiers on them being online harassment or hate speech.  Even before starting on this project there are a few caveats to consider: I am not a linguist, and not an expert on this topic (there are whole groups of academics working on it).  I just have a few ideas, some ML experience and the desire to explore whether something can be done about it.

## The definition problem

What is 'offensive'?  This is likely to be highly cultural, and even subcultural.
Hate speech seems relatively well defined: expressing hate or extreme bias towards a particular group.
Threats of violence are also pretty clear.  The [corpus](http://www.cs.umd.edu/~golbeck/papers/trolling.pdf) I'm using selects both those groups under one label 'harassment'.

It's possible to use other categories: another [corpus](http://www.aclweb.org/anthology/N16-2013) has been labeled on racist and sexist tweets.

Another narrowing down of scope includes the type of text we analyze.  We're focusing on twitter, which is easier since the tweets are shortext.  Analysis of Facebook or other popular social media

## The corpus problem

It's hard to get a good, labeled corpus for this problem: ideally this needs a large, labeled corpus for supervised training.  Which means human intervention: either a group of experts or a crowdsourced workforce.  The first option is expensive but qualitatively probably the best, since the experts agree and cross-reference on what is considered offensive.  With the second option we bump up against the fact that subgroups may have different views and sensitivities, and the resulting corpus is likely to suffer from some different biases.

The corpus used here is produced by a group of experts, and is the one referred to here: <http://www.cs.umd.edu/~golbeck/papers/trolling.pdf>
It's relatively small in size (16K tweets).  As most corpuses in this area it's strongly unbalanced, since fortunately offensive tweets are in the minority (perhaps because the platform already moderates it to some extent).

The corpus is not included (as per the terms) but can be obtained from the article's author on demand, after signing their Terms of Use.

## Approach

I'll try to use a few simple classifiers first, and then go down more elaborate routes involving different features.
I started with some literature study, and may try the techniques mentioned in the given articles first (deep learning).

## Possible future work

* thought on how to obtain a larger corpus (carefully monitored crowdsourcing)?
* would it be possible to include network data?  Who someone follows and interacts with is likely to match their views and attitude. this could bump up against GDPR
* bookmarklet with existing model?
