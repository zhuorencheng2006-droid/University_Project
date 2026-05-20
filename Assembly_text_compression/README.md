# Text Compressor in Motorola 88110 Assembly

**University Project**  
**Course**: Ensamblador / Computer Architecture  
**University**: Universidad Politécnica de Madrid (UPM)  
**Academic Year**: 2025-2026

## Project Overview
This project implements a **lossless text compression and decompression** system in Motorola 88110 Assembly language.  
All the code is contained in a single file: **`CDV25.ens`**.

## Main Subroutines

- **`LongCad`** — Calculates the length of a null-terminated string
- **`BuscaCar`** — Searches for a specific character in a string within a given range
- **`CoincidenCad`** — Compares two strings and returns the length of the matching prefix
- **`BuscaMax`** — Finds the longest matching substring in the previous part of the text (provided by professor)
- **`Comprime`** — Compresses the input text using a simplified dictionary method (references to previous occurrences)
- **`Descomprime`** — Decompresses the compressed data back to the original text
- **`PoneBitA1`** — Sets a specific bit to 1 in the bit map
- **`LeeBit`** — Reads the value of a specific bit in the bit map
- **`Verifica`** — Full verification: compress → decompress and check if result matches the original text

## Key Features
- Implemented using stack for parameters and local variables
- Follows strict 88110 calling conventions and stack discipline
- Complete compression/decompression pipeline
- Includes test programs for each subroutine

## Technologies
- Motorola 88110 Assembly Language
- 88110 Processor Emulator

## Main File
- `CDV25.ens` (contains all subroutines)

## Status
Completed

## How to Compile and Run

### 1. Assemble
```bash
88110e -e 0 -o CDV25.bin CDV25.ens

### 1. Execute
```bash
mc88110.bat CDV25.bin
