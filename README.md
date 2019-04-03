# get_plasmids

Detect and extract plasmids in fragmented (draft) genomes.

Usually, draft genomes in RefSeq database don't present a clear annotation regarding the presence of plasmids. It may lead to the lack of information about the location of specific genes.

Because of their modularity and constant rearrengement, detect plasmids using BLASTn against already known plasmids (e.g. RefSeq genomes) only permits to compare against plasmids already described and hide the possibility to detect new plasmids not described yet.

To solve this problem and detect non-described plasmids in draft genomes (or plasmidic elements incorporated into the chromosome), get_plasmids is proposed.

It will detect contigs which not described as plasmids (or 

get_plasmids pipeline:

    1 - Download your dataset with your desired plasmids genomes
    
    2 - Fragment the plasmids genomes
    
    3 - Perform get_plasmids search
    
    4 - Extract plasdmids


Scripts:

contigs2gbk.py - Extract the complete contig from your .gbk/.gbff file and save it on the genbank format.

    contig2gbk.py -c [contig_ID] -g [genome] -o [output_name|stdout]
    
