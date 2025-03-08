# Glycine
This tool is designed to identify and trim full-length cDNA sequencing reads.  

## No Installation Required  
**Ready to Use After Extraction**  

This software is designed for ease of use without the need for a complicated installation process. Simply extract the contents of the software package to your preferred location on your system, and it's ready to go.  

**How to Start:**  
1. Download the `.tar.gz` file.
2. Extract the contents to a desired location.  
3. Run the `glycine` to start the software.

**Note:** glibc version 2.35 or higher is required.

## Example Usage
`glycine -f sample.fq.gz -5 tso-seq -3 rtp-seq -o /path/to/output -n sample -e 0.25,0.4 -s 100,100 -u 10 -l 10`  

## Command-line Arguments
```
Usage: glycine [OPTIONS] --fastq <fastq file> --tso_seq <tso seq> --rtp_seq <rtp seq> --outdir <output dir> --sample <sample>

Options:
  -f, --fastq <fastq file>       Input a fastq file
  -5, --tso_seq <tso seq>        TSO sequence
  -3, --rtp_seq <rtp seq>        RTP sequence
  -o, --outdir <output dir>      Output directory
  -n, --sample <sample>          Sample name
  -e, --err <err threshold>      Threshold of Levenshtein Distance value or sequencing error rate. Use a comma to separate two numbers, when there are
                                 different thresholds for the 5' and 3' ends [default: 0.25,0.4]
  -s, --shift <shift threshold>  Threshold of shift length for identifying TSO/RTP sequences. Use a comma to separate two numbers, when there are different
                                 thresholds for the 5' and 3' ends [default: 50,50]
  -L, --min_len <min len>        Sequences shorter than the minimum length will be directly classified as discarded [default: 100]
  -Q, --min_qual <min qual>      Read quality lower than the minimum quality will be directly classified as discarded [default: 7.0]
  -u, --trim_len <trim len>      The length of the 3' end barcode sequence to be trimmed [default: 0]
  -l, --tail_len <tail len>      PolyA tail length [default: 10]
  -q, --umi_len <umi len>        The length of the Unique Molecular Identifier (UMI) located between the PolyA tail and the Reverse Transcription Primer
                                 (RTP) [default: 0]
  -t, --thread <thread>          Number of threads [default: 4]
  -h, --help                     Print help
  -V, --version                  Print version
```

## Authors
夏小双 Xiaoshuang Xia (xiaxiaoshuang@genomics.cn)  

## License and Usage Restrictions
**Research Use Only**  

This software is provided strictly for individual research purposes. Commercial use is strictly prohibited. This means:  
**Allowed:** Personal academic research, personal learning, and non-commercial experimentation.  
**Not Allowed:** Any form of commercial application, distribution, or use that generates revenue directly or indirectly. This includes, but is not limited to, integration into commercial products, offering this software as a service, or using it for commercial gain.  

For commercial licensing or permissions, please contact us.
