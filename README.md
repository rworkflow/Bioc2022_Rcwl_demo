# Rcwl/RcwlPipelines: Use R To Build, Read, Write, And execute CWL Workflows"

## Instructor(s) name(s) and contact information

* [Qian Liu](https://github.com/liubuntu) (Qian.Liu@roswellpark.org) [twitter](https://twitter.com/QianLiu28878838)
* Slack channel: community-bioc/#rcwl

## Workshop Description

The Common Workflow Language (CWL) is used to provide portable and
reproducible data analysis workflows across different tools and
computing environments. We have developed Rcwl, an R interface to CWL,
to provide easier development, use and maintenance of CWL pipelines
from within R. We have also collected nearly 200 pre-built tools and
pipelines in RcwlPipelines, ready to be queried and used by
researchers in their own analysis. 

Here we included a scRNAseq preprocessing pipeline which uses
`STARsolo` for alignment and quantification, and `DropletUtils` to
load the data into _R_ as an `singleCellExperiment` object. This
pipeline demonstrates the typical use case of our packages.

For the demo, users also need to install the following packages: 

```
BiocManager::install(c("rworkflow/Rcwl", "rcwlwork/RcwlPipelines", 
	                "git2r", "DropletUtils", "BiocParallel"))
```

