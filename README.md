# Toeplitz‑Quantum‑Extractor

Tiny Colab project that:  
1. simulates two biased QRNG streams  
2. XOR‑fuses them (Qrypt style)  
3. squeezes bias with a memory‑safe Toeplitz universal hash  
4. validates output with NIST‑style tests & entropy plot  

## Why cryptographers should care
- **Classical RNG flaws**: software PRNGs and simple QRNG‑XOR can leak bias or correlations, leaving keys vulnerable to back‑door attacks.  
- **Provable extraction**: toeplitz hashing is a 2‑universal hash that guarantees the output’s min‑entropy matches the security bound, even if an attacker knows the bias.  
- **Scalable & memory‑safe**: our FFT‑based, streaming implementation runs in O(n log n) time and uses linear RAM—no 600 GB matrix needed—so you can deploy it on Colab, edge devices, or integrate into Vault/CI pipelines.

## Quick start
1. Open `notebook.ipynb` in Google Colab.  
2. Run cells top→bottom (‑‑> at the end).  
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
