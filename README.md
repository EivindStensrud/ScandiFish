## ScandiFish
### Contributors
The database is a collaborative work between Stensrud E., Töpel M. and Eiler A. as a part of the master thesis of Stensrud.

Citation: If you use ScandiFish, please cite Stensrud et al. 2021, ScandiFish, a metabarcoding reference database for Scandinavian fish communities. Havforskermøtet, Bergen, 23. November 2021. 
### 
ScandiFish is a metabarcoding reference database for the Scandinavian fish community.
The database is based on the MiFish-U primers, which amplify a hypervariable region of (~170bp) of the mitochondrial 12s rRNA gene region.
For more information for the primer check out the articles listed in suggested reading.
Fish species found present in November 2020 in www.artsdatabanken.no/, https://www.artdatabanken.se/, www.naturbasen.dk were extracted and offical latin names were obtained through FishBase (https://www.fishbase.se/search.php) which uses COL taxanomy https://www.catalogueoflife.org/. This process resulted in 525 Scandinavian fish species.
The list of Scandinavian fish species can be found in the repository. 

The first update, ScandiFish_12s_v1.0 (09.11.2021) contained 744 FASTA sequences for 380 Scandinavian fish species.

### Workflow of the database pipeline
All sequences matching the taxon names in the list of taxon names are downloaded from GenBank database at NCBI, https://www.ncbi.nlm.nih.gov/genbank/.

The build-up of the database is based on sequence similarity where the new sequences are BLASTed https://blast.ncbi.nlm.nih.gov/Blast.cgi against a reference database, this allows for sequences not annotated belonging to the 12s rRNA gene region to be analyzed.

Further the database is produced on a non-linear pipeline, which saves analysed accession numbers to prevent them from being analyzed multiple times. This allows for faster and less labour intensive manual updates in the future.

The sequences are then checked for quality, length, intraspecific duplications, and identified sequences are removed.
MAFFT aligned sequence are then placed on a genetree based on FastTree before being approved in the database.

### Specs
ScandiFish_12s_v1.0:

744 unique sequences

380 of 525* Scandinavian fish species is found in the database*

32 non-unique sequences

55 different species shares ≥1 sequences with other species

Marks:

*The species found in the Scandinavian databases do not use a common taxonomic classification for fish species, and contains some sub-species.
The species are then controlled against Catalogue of Life(COL) through FishBase which is a standard for classification. 
Then the species name obtained from Catalogue of Life is used to search for sequences in NCBI's Genbank which is using another classification than COL.
We discovered that some species, especially Swedish Coregonus species found in the Scandinavian databases are not accepted in NCBI's classification, while accepted in COL.
This results in a inflated number of non-found fish species, n=54.
The same goes with rare species which have been observed a few times are often registered in the Scandinavian databases but not in NCBI. 
This is the case for several deepwater species as Lycodes and Careproctus species.




