## ScandiFish
### Contributors
The database is a collaborative work between Stensrud E., Töpel M. and Eiler A. as a part of the master thesis of Stensrud.

### 
ScandiFish is a metabarcoding reference database for the Scandinavian fish community.
The database is based on the MiFish-U primers, which amplify a hypervariable region of (~170bp) of the mitochondrial 12s rRNA region.
For more information for the primer check out the articles listed in suggested reading.
Fish species found present in November 2020 in www.artsdatabanken.no/, https://www.artdatabanken.se/, www.naturbasen.dk were extracted and offical latin names were obtained through FishBase(link) which uses COL taxanomy https://www.catalogueoflife.org/.

The first update, ScandiFish_12s_v1.0 (09.11.2021) contained 744 FASTA sequences for 380 Scandinavian fish species.

### Workflow of the database pipeline
All sequences matching the taxon names in the list of taxon names are downloaded from GenBank database at NCBI.

The build-up of the database is based on sequence similarity where the new sequences are BLASTed against a reference database, this allows for sequences not annotated belonging to the 12s rRNA region to be analyzed.

Further is the database based on a non-linear pipeline, which saves analysed accession numbers which prevent them from being analyzed multiple times, which allows for faster and less labour intensive updates in the future.

The sequences are then checked for quality, length, intraspecific sequence duplicates are removed and sequence placement on a genetree based on FastTree before being approved in the database.

### Specs
ScandiFish_12s_v1.0:

744 unique sequences

380 species present

32 non-unique sequences

55 different species shares ≥1 sequences with other species



Citations: If you use ScandiFish, please cite (xxxxxx)
