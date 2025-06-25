# Project Overview

This project, conducted under the course CT216: Introduction to Communication Systems, explores the design, implementation, and performance analysis of Low-Density Parity-Check (LDPC) codes, specifically as adopted in 5G New Radio (NR) standards.

Our objective was to study LDPC encoding/decoding principles, implement both hard and soft decision decoding techniques, and simulate their performance under varying signal-to-noise ratios using MATLAB.

# Topics Covered
Fundamentals of LDPC codes and their structure

- 5G NR Base Graphs: NR_1_5_352 (BG1) and NR_2_6_52 (BG2)
- Sparse parity-check matrix construction and expansion
- Tanner graph representation and message-passing algorithms
- Rate matching: shortening, puncturing, and repetition
- Systematic encoding methodology used in 5G
- Hard Decision Decoding (Bit-Flipping): Algorithm and analytical proof
- Soft Decision Decoding (Belief Propagation): LLR-based inference with Min-Sum approximation
- Simulation-based BER and decoding success analysis for multiple code rates
- Performance comparison with Shannon’s theoretical limit and among decoding types


# Methods Implemented

## Encoding:
- Base matrix expansion using cyclically shifted identity matrices
- Systematic encoding utilizing double-diagonal matrix structure for low-latency generation

## Decoding Algorithms:
- Hard Decision Decoding (HDD): Bit-flipping using syndrome analysis and majority logic
- Soft Decision Decoding (SDD): Belief propagation using LLRs and Min-Sum approximation for efficiency
- MATLAB implementation of both algorithms with adjustable iterations and noise levels


## Simulation:
- Simulated BPSK modulation over AWGN channel
- BER vs SNR plots for various LDPC code rates (1/4, 1/3, 1/2, 3/5, 4/5)
- Comparison of soft and hard decoding performance across base graphs

# Results Summary
- Soft decoding consistently outperforms hard decoding at low SNRs (2–3 dB advantage).
- At high code rates or high SNRs, both decoding techniques converge in performance.
- LDPC decoding achieves BERs near 10⁻⁵ at moderate SNRs, approaching Shannon limit.
- Rate matching mechanisms provide adaptability for varying channel conditions.

# Contents
- ldpc_hard_decode.m: Hard decision decoding function
- ldpc_soft_decode.m: Soft decision (Min-Sum) decoding function
- MATLAB scripts for encoding, simulation, BER plotting
- Analytical proofs and explanations for both decoding methods
-Graphs and performance charts (BER vs. SNR for BG1 and BG2)
- Project Report: Full documentation with theory, implementation, and analysis

# References
- Gallager, R. (1960). Low-Density Parity-Check Codes
- 3GPP TS 38.212 – 5G NR Channel Coding
- Richardson & Urbanke – Modern Coding Theory
- NPTEL Lectures by Prof. Andrew Thangaraj
- Lecture materials by Prof. Yash Vasavda**

