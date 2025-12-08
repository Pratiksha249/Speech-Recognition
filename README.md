

 LAB-WISE DETAILS & INFERENCES


 LAB 1 — Basic Speech Analysis

 **Aim**
To analyze a speech signal in the time and frequency domains using waveform visualization, ZCR, energy, and FFT.

 **Key Tasks**
- Load and display audio waveform  
- Compute Zero Crossing Rate and Energy  
- Perform FFT for frequency-domain analysis  

 **Inference**
Voiced and unvoiced regions are distinguishable through ZCR and energy plots. FFT reveals dominant spectral components, validating periodicity in voiced segments and noise-like characteristics in unvoiced segments.



 LAB 2 — STFT & Spectrogram

 **Aim**
To compute the Short-Time Fourier Transform and generate spectrograms.

 **Key Tasks**
- Compute STFT  
- Plot magnitude spectrogram  
- Compare wideband and narrowband patterns  

 **Inference**
Wideband spectrogram shows excellent time resolution, highlighting transitions, while narrowband spectrogram clearly displays harmonic spacing. STFT effectively represents speech as a time–frequency signal.



 LAB 3 — Pitch & Formant Extraction

**Aim**
To extract pitch (F0) and formants using LPC and autocorrelation.

 **Key Tasks**
- Autocorrelation-based pitch estimation  
- LPC analysis for formant extraction  
- Formant tracking visualization  

**Inference**
Pitch contour varies smoothly in voiced segments. LPC-derived formants align with expected F1–F3 patterns of vowels, confirming the effectiveness of LPC in vocal tract modeling.



 LAB 4 — LPC Analysis & Synthesis

**Aim**
To analyze and synthesize speech using Linear Predictive Coding (LPC).

 **Key Tasks**
- Compute LPC coefficients  
- Generate LPC spectrum  
- Reconstruct speech using LPC synthesis  

 **Inference**
LPC successfully models the spectral envelope of speech. Reconstructed audio, although robotic, retains formant structure, demonstrating that LPC efficiently compresses and represents speech.



 LAB 5 — Dynamic Time Warping (DTW)

 **Aim**
To compare speech signals spoken at different speeds using DTW.

 **Key Tasks**
- Extract MFCC features  
- Compute DTW distance and path  
- Visualize alignment  

 **Inference**
DTW effectively aligns slow vs fast utterances by warping the time axis. Lower DTW distance indicates greater similarity. Warping path bends around elongated syllables, proving DTW’s robustness to timing variations.

---

 LAB 7 — Hidden Markov Model (HMM)

 **Aim**
To understand HMM components and compute forward probability.

 **Key Tasks**
- Define states, observations  
- Build transition (A), emission (B), and initial (π) matrices  
- Apply forward algorithm  

 **Inference**
Forward probability gradually decreases as uncertainties accumulate across time. HMM structure accurately models sequential phoneme relationships and probabilistic transitions in speech.



 LAB 8 — Viterbi Algorithm

 **Aim**
To decode the most probable phoneme sequence using the Viterbi algorithm.

 **Key Tasks**
- Use A, B, π and observation sequence  
- Compute delta & psi matrices  
- Extract optimal state path  

 **Inference**
Viterbi identifies the highest-probability phoneme sequence. Delta matrix shows evolving path probabilities, while psi matrix highlights chosen backpointer states. This demonstrates Viterbi’s role in speech recognition decoders.



 LAB 9 — End-to-End Phoneme Decoding  
### *(Audio → MFCC → Clustering → HMM → Viterbi)*

 **Aim**
To perform unsupervised phoneme-like segmentation from raw speech audio.

 **Pipeline**
1. Load audio  
2. Extract MFCC features  
3. Cluster MFCC frames → observation symbols  
4. Estimate HMM parameters (A, B, π) from audio  
5. Apply Viterbi decoding  
6. Visualize:
   - Waveform + segment boundaries  
   - MFCC spectrogram  
   - Hidden state color bar  
   - t-SNE cluster separation  
   - Delta & psi heatmaps  
   - State segmentation timeline  

Lab 10 – Voice-Based Telephone Directory Lookup

A speech recognition system that retrieves telephone directory entries from uploaded MP3 audio containing spelled-out names.

Features:

Upload MP3 audio (e.g., “J O H N”)

Automatic MP3 → WAV conversion

ASR-based letter recognition

Letter-to-name reconstruction

Directory search with suggestions
Example:

Audio: "P R A T I K S H A"
Output: "PRATIKSHA → +91-9876543105"


```bash
jupyter notebook SPR_labX.ipynb
