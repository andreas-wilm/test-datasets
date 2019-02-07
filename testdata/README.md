Create from GIS internal replicate data:

```bash
 n=100000;
 for f in MUX1202/PDH203/PDH203_GTGGCC_NA_R1.fastq.gz MUX1202/PDH203/PDH203_GTGGCC_NA_R2.fastq.gz MUX1202/PDH205/PDH205_CGTACG_NA_R1.fastq.gz MUX1202/PDH205/PDH205_CGTACG_NA_R2.fastq.gz; do
     seqtk sample $f $n | gzip > $(basename $f .fastq.gz).n${n}.fastq.gz;
done;
```

