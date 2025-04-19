# Toeplitz‑Quantum‑Extractor

Tiny Colab project that:
1. simulates two biased QRNG streams  
2. XOR‑fuses them (Qrypt style)  
3. squeezes bias with a memory‑safe Toeplitz universal hash  
4. validates output with NIST‑style tests & entropy plot  

## Quick start
1. Open `notebook.ipynb` in Google Colab.  
2. Run cells top→bottom (‑‑> ✅ at the end).  
3. Optional: replace Cell 3 with live Qrypt Entropy‑as‑a‑Service.

## Requirements
`bitarray scipy tqdm` (Colab installs them automatically).

## Output
* ≥ 0.98 bits/bit min‑entropy after extraction  
* Passes Frequency & Runs tests (p > 0.01)

## Author
Satya Mohit Rao Kamkanampati
Email: saka4331@colorado.edu
Linkedin: https://www.linkedin.com/in/mohitraosatya/
