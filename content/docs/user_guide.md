+++
title = "User Guide"
description = "User guide"
date = 2025-05-01T08:00:00+00:00
updated = 2021-05-01T08:00:00+00:00
sort_by = "weight"
weight = 1
template = "docs/page.html"
+++

## Finding datasets

Navigate to the desired datatype:
- [Electron Microscopy](/data/electron-microscopy/)
- [Spatial Omics](/data/spatial-omics)
- [Flow Cytometry](/data/flow-cytometry)


## Viewing a dataset

Click on a viewing link in the list to use the browser are copy the URL to use your own code.

### Via pooch

[pooch](https://github.com/fatiando/pooch) fetches files and stores them locally.

```python
import pooch

DAMBI_DATA = pooch.create(
    path=pooch.os_cache("dambi_data"),
    base_url="https://dl01.irc.ugent.be/",
    version="0.1.0",
    # overwriting data path with environment variable
    env="DAMBI_DATA",
    registry={
        "flow/FlowRepository_FR-FCM-ZZPH/Levine_13dim.fcs": None,
        "flow/FlowRepository_FR-FCM-ZZPH_zarr/Levine_13dim.zarr": None,
    }
    registry=None,
)
```

`DAMBI_DATA` can then be used to fetch files locally into a smart local cache and get it's location. 
```python
file = DAMBI_DATA.base_url + "flowFlowRepository_FR-FCM-ZZPH_zarr/Levine_13dim.zarr"
adata = ad.read_zarr(file)
```

### Via URLs

Zarr URLs can be used to lazily view big remote datasets, with interoperability with Dask and AnnData.

```python
import zarr
import anndata as ad
dataset_url = DAMBI_DATA.base_url + 'flow/FlowRepository_FR-FCM-ZYX9_zarr/'
# as raw zarr store
store = zarr.open(dataset_url + 'TC_SPL_L000043215.zarr', mode="r")
# as AnnData
adata = ad.read_zarr(url)
```