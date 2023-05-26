+++
title = "Spatial Omics"
description = ""
date = 2021-05-01T08:00:00+00:00
updated = 2021-05-01T08:00:00+00:00
draft = false
weight = 10
sort_by = "weight"
template = "docs/page.html"

[extra]
toc = true
top = false
+++

Spatial transcriptomics and proteomics are new sequencing or imaging modalities that allow study of the spatial organization of the transcriptome and proteome in tissues.

## Formats

There are two methods of storing these types of datasets:

- Older, better supported:
    - Images as OME-TIFF, which can support faster parsing by using an [offset index](https://hms-dbmi.github.io/generate-tiff-offsets/).
    - Single-cell data in the AnnData format.
    - Supported by napari and Vitessce
- Newer, more experimental:
    - one [SpatialData](https://spatialdata.scverse.org/en/latest/) object, which uses .zarr and AnnData internally.
    - Supported by napari, not yet by Vitessce

Currently one SpatialData dataset is publicly available, a consolidated version of [this cosmx_io dataset](https://spatialdata.scverse.org/en/latest/tutorials/notebooks/datasets/README.html).

Use in [SpatialData](https://github.com/scverse/spatialdata) (with remote reading support):
```python
import spatialdata as sd
sdata = sd.SpatialData('https://dl01.irc.ugent.be/spatial/cosmx/data.zarr/')
```

Use in [napari-spatialdata](https://github.com/scverse/napari-spatialdata):
```  
napari --with-reader napari-spatialdata 'https://dl01.irc.ugent.be/spatial/cosmx/data.zarr/'
```


## More datasets

More datasets can be obtained here:
- [IDR image catalog](https://idr.github.io/ome-ngff-samples/)
- [SpatialData sandbox](https://spatialdata.scverse.org/en/latest/tutorials/notebooks/datasets/README.html)