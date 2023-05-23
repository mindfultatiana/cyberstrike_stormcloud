# CyberStrike STORMCLOUD Labs
This repository includes the MkDocs data used to build the CyberStrike STORMCLOUD Lab website.  This code has been open-sourced in order to (a) provide a reference for CyberStrike STORMCLOUD students after completing the training and (b) more rapidly deploy updates to student virtual machines as course content is updated. 

# Background
The U.S. Department of Energy (DOE) Office of Cybersecurity, Energy Security and Emergency Response (CESER), in collaboration Idaho National Laboratory (INL), developed the CyberStrike™ training program.  This program has been expanded in collaboration with the DOE Solar Energy Technologies Office (SETO) and DOE Vehicle Technologies Office (VTO), with INL and Sandia National Laboratories, to include cybersecurity training for distributed energy resources (DER) and electric vehicle chargers. 

More information on the program is provided in the following links: 
* [INL Website](https://inl.gov/cyberstrike/)
* [CyberStrike Training Program](https://inl.gov/wp-content/uploads/2022/09/22-50524_CyberstrikeOVERVIEW_r3.pdf)
* [CyberStrike LIGHTS OUT Training](https://inl.gov/wp-content/uploads/2023/01/22-50524_CyberstrikeLIGHTSOUT_r2.pdf)
* [Video](https://www.youtube.com/watch?v=ZvMf5eHg89s)
* [Sandia Progress Update on the DOE SETO Securing Solar for the Grid (S2G) Project](https://www.researchgate.net/publication/368599978_Securing_Solar_for_the_Grid_S2G_-_Progress_Update)

# Website Construction 

1. Install Python 3.7+ 

2. Install MkDocs packages: 

	```
	pip install mkdocs
	pip install markdown
	pip install pymdown-extensions
	pip install mkdocs_custom_fences
	```
	
3. Serve the website and then visit `localhost:8000`.

	`python -m mkdocs serve` 

4. Build the website as standalone webpage in `./docs/`

	`python -m mkdocs build`

5. For developers who would like to create an online version at `https://<name>.github.io/cyberstrike_stormcloud/`

	`python -m mkdocs gh-deploy -f CyberStrike-Lab-Workbook-Solar/mkdocs.yml -v`

# Copyright

Copyright 2023 National Technology & Engineering Solutions of Sandia, LLC (NTESS). Under the terms of Contract DE-NA0003525 with NTESS, the U.S. Government retains certain rights in this software.
