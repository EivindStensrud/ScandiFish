## ScandiFish 12s v1.2
### Contributors
The database is a collaborative work between Stensrud E., Töpel M. and Eiler A. as a part of the master thesis of Stensrud.

Citation: If you use ScandiFish, please cite Stensrud et al. 2021, ScandiFish, a metabarcoding reference database for Scandinavian fish communities. Havforskermøtet, Bergen, 23. November 2021. 
### 
ScandiFish is a metabarcoding reference database for the Scandinavian fish community.
The database is based on the MiFish-U primers, which amplify a hypervariable region of (~170bp) of the mitochondrial 12s rRNA gene region.
For more information on the primer, check out the articles listed in the suggested reading.
Fish species found present in November 2020 in www.artsdatabanken.no/, https://www.artdatabanken.se/, www.naturbasen.dk were extracted, and and official latin names were obtained through FishBase (https://www.fishbase.se/search.php) which uses COLtaxonomyy https://www.catalogueoflife.org/. This process resulted in 525 Scandinavian fish species.
The list of Scandinavian fish species can be found in the repository. 

ScandiFish 12s v1.2 (23.05.2022) contained 732 FASTA sequences for 380 Scandinavian fish species.

### Workflow of the database pipeline
All sequences matching the taxon names in the list of taxon names are downloaded from GenBank database at NCBI, https://www.ncbi.nlm.nih.gov/genbank/.

The build-up of the database is based on sequence similarity where the new sequences are BLAST analysed https://blast.ncbi.nlm.nih.gov/Blast.cgi against a reference database; this allows for sequences not annotated belonging to the 12s rRNA gene region to be analysed.

Further, the database is produced on a non-linear pipeline, which saves analysed accession numbers to prevent them from being analysed multiple times. This allows for faster and less labour intensive manual updates in the future.

The sequences are then checked for quality, length, and intraspecific duplications, and identified sequences are removed.
MAFFT aligned sequence are then placed ogene treetree to visualise the discriminatory powers of the primers among Scandinavian fish species.
A final curation with MegaBlast, on both the accession number and marker region to control for misanntotation was conducted.

### Streamlined taxonomic sorting
To assure maximum utilisation of ScandiFish, a taxonomic sorting based annotation was integrated in a script developed for ScandiFish.
The taxonomic sorting workflow the annotation script is based on is developed by Beentjes et al. 2019 and is partly based on Huson et al. 2007 MEGAN pipeline, which annotate sequences on a conservative matter, reducing the false positive rate.


### Specs
ScandiFish 12s v1.2:

732 unique sequences

380 of 525* Scandinavian fish species is found in the database*

30 non-unique sequences

53 different species sharesequenceences with other species

Marks:

*The species found in the Scandinavian databases do not use a common taxonomic classification for fish species and contain some sub-species.
The species are then controlled against Catalogue of Life(COL) through FishBase w, atandard for classification. 
Then the species name obtained from Catalogue the of Life is used to search for sequences in NCBI's Genbank, which uses another classification than COL.
We discovered that some species, especially Swedish *Coregonus* species found in the Scandinavian databases, arenot accepted in NCBI's classification, while accepted in COL.
This results in an inflated number of non-found fish species, n=54.
The same goes with rare species which have been observed a few times and are often registered in the Scandinavian databases but not in NCBI. 
This is the case for several deepwater species as *Lycodes* and *Careproctus* species.

Due to NCBI taxonomic classification, *Dicentrarchus labrax*, European seabass, do not have any order ranks. Since the workflow is based on a seven rank system, the classification was manually altered to work with downstream analysis.

From Eukaryota;Chordata;Actinopteri;Moronidae;Dicentrarchus;Dicentrarchus_labrax

To Eukaryota;Chordata;Actinopteri;Moronidae;;Dicentrarchus;Dicentrarchus_labrax

Resources:

Beentjes KK, Speksnijder AGCL, Schilthuizen M, Hoogeveen M, Pastoor R, et al. (2019) Increased performance of DNA metabarcoding of macroinvertebrates by taxonomic sorting. PLOS ONE 14(12): e0226527. https://doi.org/10.1371/journal.pone.0226527

Huson, D. H., Auch, A. F., Qi, J., & Schuster, S. C. (2007). MEGAN analysis of metagenomic data. Genome Research, 17(3), 377–386. http://doi.org/10.1101/gr.5969107
