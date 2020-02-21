# SoalShiftSISOP20_modul1_T16
1a.
#!/bin/bash

echo "Region dengan profit terkecil adalah: "
awk -F'\t' 'FNR > 1{SUM[$13] +=$21} END{for (j in SUM) print j, SUM[j]}' Sample-Superstore.tsv | sort -gk2 | awk 'FNR < 2{print$1}'

1b. 
#!bin/bash
awk -F "\t" 'NR>1 {if( $13=="Central" ) { a[$11]+=$21 }} END { for(i in a) print i","a[i] | "sort -t ',' -g -k2"}' Sample-Superstore.tsv | head -n 2

1c.
!bin/bash
awk -F "\t" 'NR>1 { if( ( $11=="Illinois" || $11=="Texas" ) && $13=="Central" ) { a[$17]+=$21; }} END { for(i in a) print i"="a[i] | "sort -t '=' -g -k2" }' Sample-Superstore.tsv | head -n 10
