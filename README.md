# Connecting Bioconductor to other bioinformatics tools using `Rcwl` - Application in scRNA-seq data
![](https://github.com/liubuntu/Bioc2020RCWL/workflows/.github/workflows/basic_checks.yaml/badge.svg)

## Instructor(s) name(s) and contact information

* [Qian Liu](https://github.com/liubuntu) (Qian.Liu@roswellpark.org) [twitter](https://twitter.com/QianLiu28878838)
* [Qiang Hu](https://github.com/hubentu) (Qiang.Hu@roswellpark.org) [twitter](https://twitter.com/hubentu)
* Slack channel: community-bioc/#rcwl

## Workshop Description

This workshop introduces the Bioconductor toolchain for usage and
development of reproducible bioinformatics pipelines using packages of
Rcwl and RcwlPipelines. The Common Workflow Language (CWL) is an open
standard for development of data analysis workflows that is portable
and scalable across different tools and working environments. 

Rcwl provides a simple way to wrap command line tools and build CWL
data analysis pipelines programmatically within R. It increases the
ease of usage, development, and maintenance of CWL pipelines, and
furthermore offers higher performance by intuitively supporting
parallel work with high performance computing (HPC). More than a
hundred of pre-built and tested CWL tool/pipeline recipes are included
in RcwlPipelines. These tools and pipelines are highly modularized for
easy customization of complex bioinformatics analysis.

Here we included a scRNAseq preprocessing pipeline which uses
`STARsolo` for alignment and quantification, and `DropletUtils` for
filtering raw gene-barcode matrix and removing empty droplets. This
pipeline demonstrates the typical use case of our packages.

Workshop materials can be found here: http://rcwl.org/Rcwl_scRNAseq/

## Docker instructions:

In order to run the workshop successfully, users need to do either of
the following:

1. Install [docker](https://docs.docker.com/get-docker/).
2. Install needed tools: [STAR](https://github.com/alexdobin/STAR/releases/tag/2.7.3a). 

Users also need to install the following packages: 

```
BiocManager::install(c("rworkflow/Rcwl", "rcwlwork/RcwlPipelines", 
	                "git2r", "DropletUtils", "BiocParallel"))
```

