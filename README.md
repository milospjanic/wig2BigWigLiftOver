# wigLiftOver2bigWig

This script will convert wig files from coordinates hg18 to coordinates hg19 of the human genome and output a bigwig file.

Script:
- converts wig to bigwig
- checks if bigwigToBedGraph is present if not downloads it
- converts the bigwig to bedgraph using bigwigToBedGraph
- checks if liftOver is present if not downloads it
- lifts over the bedgraph preserving the fourth column using -bedPlus=4
- sorts the liftover output bedgraph file
- downloads hg19.chrom.sizes for bedGraphToBigWig
- checks if bedGraphToBigWig is present if not downloads it
- converts the bedgraph back to bigwig using bedGraphToBigWig

Script will save remapped bigwig file with .hg19 extension

#Usage

<pre>
chmod 755 ./wigLiftOver2bigWig.sh
./wigLiftOver2bigWig.sh path/to/bigwig/file.bw
</pre>
