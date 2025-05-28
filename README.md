# Number Sorter Utility

A simple yet efficient Python tool to sort large text files containing numeric data — one number per line. This utility is ideal for handling files that are too big to fit into memory by using a two-phase external sort approach: chunked sorting and heap-based merging.

## Features

- Handles large datasets efficiently by sorting in memory-friendly chunks
- Uses temporary files to store intermediate results
- Supports optional output to a new file or prints sorted numbers to the console
- Ignores invalid (non-numeric) lines gracefully

## How It Works

1. **Chunked Sorting**: The input file is read in fixed-size chunks. Each chunk is sorted in memory and written to a temporary file.
2. **Merging**: All sorted chunks are then merged using a heap-based merge (`heapq.merge`) for optimal performance.

## Usage

```bash
python number_sorter.py input_file.txt [output_file.txt]

