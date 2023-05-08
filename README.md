# The COSI singularity container

The definition file Singularity.def can be used to create a COSItools singularity container.

## Creation

This assumes you have installed singularity.
You create the container with:

```
SINGULARITY_TMPDIR=`pwd`/tmp SINGULARITY_CACHEDIR=`pwd`/cache singularity build --fakeroot COSItools.sif Singularity.def
```

In the container, the COSItools are installed in the directory /COSI/COSItools

## Usage examples

### mcosima run
```
singularity exec COSItools.sif /bin/bash -c '. /COSI/COSItools/source.sh; mcosima -z ${MEGALIB}/resource/examples/cosima/source/CrabOnly.source'
```
