# Vaevictis

Experimental combination of various ideas for dimensional reduction nad manifold analysis

Currently (re)implements ideas from following published results:

The ivis algorithm as described in the paper [Structure-preserving visualisation of high dimensional single-cell datasets](https://www.nature.com/articles/s41598-019-45301-0).


The scvis algorith as described in the paper [Interpretable dimensionality reduction of single cell transcriptome data with deep generative models](https://www.nature.com/articles/s41467-018-04368-5)

## Installation

Vaevictis runs on top of TensorFlow. 

In R 
```
reticulate::py_install("git+https://github.com/stuchly/vaevictis.git@master",pip=TRUE)
```

## Example (R)
```
vae<-reticulate::import("vaevictis")
red=vae$dimred(as.matrix(iris[,1:4]))
plot(red[[1]],col=iris[,5])
```
