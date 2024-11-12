# paflen

A simple AWK script to calculate length statistics and weighted average identity from PAF (Pairwise Alignment Format) files.

## Description

`paflen` processes PAF alignment files and outputs:
- Total length of target sequences
- Total length of query sequences
- Weighted average identity across all alignments

The identity is weighted by the length of both target and query sequences in each alignment.

## Usage

```bash
./paflen input.paf > output.tsv
```

The output is tab-separated with a header row and contains:
1. Total target length
2. Total query length
3. Weighted average identity (as a decimal between 0 and 1)

## Input Format

Expects standard PAF format with the `id:f:` tag containing alignment identity values.

## Example Output

```
#target query   identity
1000    950     0.982345
```
