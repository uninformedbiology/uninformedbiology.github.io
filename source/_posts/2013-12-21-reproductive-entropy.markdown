---
layout: post
title: "Reproductive Entropy"
date: 2013-12-21 16:41:43 -0800
comments: true
categories: chromosomes entropy
---

I've had some down time recently which I've partly used to write a meiosis simulator and a punnet
square generator -- https://github.com/uberj/mendelism 

This side project plus being confused about how linked genes affect the law of independent
assortment made me take the time to write this up.

First some definitions:

-   *the law of segregation* -- during meiosis alleles are separated and each germ cell randomly gets
    one of the alleles.

-   *the law of independent assortment* -- during meiosis the probability of a single gene's allele
    going to a specific germ cell is independent of other genes.

-   *linked genes* -- genes that are "close" to each other on a chromosome (not sure how close is close
    enough).

The law of segregation is a result of Anaphase I. During Anaphase I a homologous pair of chromosomes (2 chromosomes, 4 chromatids) splits. One of the pair  has the first allele and the second has the second allele. Meiosis I finishes with two daughter cells containing disjoint sets of alleles (i.e. each gene   has its alleles spread across both cells).

The law of independent assortment can be seen as a result of Metaphase I.  During Metaphase I, right before Anaphase I, two alleles line up on either side of the Metaphase I plate. Which cell an allele joins for meiosis II depends on which side of the plate they were on -- this sidedness is random.

So how do linked genes interact with these two laws? The law of segregation is still true because even if two alleles (who were members of different genes) were on the same chromosome, they would still split into two cells. Said another way: the product cells of meiosis I would still have disjoint sets of alleles.

Linked genes do interact with the law of independent assortment. If two genes are on the same chromosome then their configuration in the Metaphase I plate will always be the same.

Here is an experiment: Say we have four genes. All four genes are on their own chromosomes. During Metaphase I the Metaphase plate forms and the homologs   line up. For each gene there is 50/50 chance of going to either of the cells produced by Cytokinesis I. With four chromosomes this gives 2 * 2 * 2 * 2 or 2 ^ 4 or 16 different possibilities.

Another experiment: Say we have four genes. There are only _two_ chromsomes and the genes are split evenly between the chromosomes. We can calculate the number of possible plate configurations 2 * 2 or 2 ^ 2 or 4.

In information theory, entropy is a measure of unpredictability of information content (<cite>[Wikipedia][0]</cite>).
In this way we can interpret an increase in the number of chromosomes to mean an increase in unpredictability of the genotype of the germ cells. We could call this sexual entropy or reproductive entropy.

[0]:http://en.wikipedia.org/wiki/Entropy_%28information_theory%29

