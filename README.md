# gbk2bcfgff
Convert Genbank to GFF compatible with "bcftools csq"


## Introduction

A common task in bacterial genome analyis
is comparing your genome to a reference
genome. The differences are usually
represented in a 
[VCF file](https://en.wikipedia.org/wiki/Variant_Call_Format)
as variants such as SNPs at particular
genome coordinates. However, the 
microbiologist is more interested in how
these variants affect the proteins andf
other features. This process is often
refereed to as "consrquences".

The consequences, or effects, that each
variant has on the genome has traditionally
been performed using 
[snpEff](http://pcingola.github.io/SnpEff/)
which requires Java and is challenging to use
with your private reference genomes.

In recent years the standard `htslib`
tool `bcftools` has quietly implemented 
support for calling consequences 
through its `csq` subcommand. 
However, it only accepts a _vary_ particular
[GFF](https://en.wikipedia.org/wiki/General_feature_format#:~:text=In%20bioinformatics%2C%20the%20general%20feature,DNA%2C%20RNA%20and%20protein%20sequences.) 
format which is not used in the
microbial genomics world. The
`gbk2bcfgff` tool presented here 
will convert our standard
bacteiral Genbank format to a GFF that
will work with `bcftools csq`.

## Install
```
conda install -c bioconda bcf2bcfgff  # COMING SOON
```
## Quick Start

FIXME.

## References

* [bcftools csq manual](https://samtools.github.io/bcftools/bcftools.html#csq)
* [csq.c comments](https://github.com/samtools/bcftools/blob/develop/csq.c)

## Author

Torsten Seemann
