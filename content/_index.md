+++
title = "DaMBi Data Portal"


# The homepage contents
[extra]
lead = 'The <b>DaMBi Data Portal</b> is a hosting server for single cell and bioimaging datasets maintained by the <a href="https://vib.be/labs/saeys-lab">Data Mining and Modelling for Biomedicine lab</a> of the <a href="https://www.irc.ugent.be/">VIB IRC</a>. It allows access and interactive viewing using a browser, local viewer or notebook.'
url = "/docs/user-guide"
url_button = "Get started"
repo_version = "GitHub v0.1.0"
repo_license = "Open-source MIT License."
repo_url = "https://github.com/saeyslab/portal"

# Menu items
[[extra.menu.main]]
name = "Data"
section = "data"
url = "/data/"
weight = 10

[[extra.menu.main]]
name = "Docs"
section = "docs"
url = "/docs/"
weight = 10

# [[extra.menu.main]]
# name = "Blog"
# section = "blog"
# url = "/blog/"
# weight = 20

[[extra.list]]
title = "Interactive Spatial Omics"
content = 'Spatial Transcriptomics and Proteomics datasets can be viewed interactively in the browser using <a href="http://vitessce.io/">Vitessce</a>.'

[[extra.list]]
title = "Serving Zarr"
content = 'Data is stored as <a href="https://zarr.readthedocs.io/en/stable/">Zarr</a> and can be using locally in <a href="https://jupyter.org/">Jupyter Notebooks</a> and viewers like <a href="https://napari.org">napari</a>.'

[[extra.list]]
title = "Looking for more data?"
content = 'Check the public <a href="https://idr.github.io/ome-ngff-samples/">IDR image catalog</a> and considered contributing your own datasets.'

[[extra.list]]
title = "Support"
content = 'For any questions or to add new data, contact somebody from the <a href="https://vib.be/labs/saeys-lab">DaMBi Lab</a>: <a href="mailto:benjamin.rombaut@irc-vib.ugent.be">benjamin.rombaut@irc-vib.ugent.be</a> '

+++
