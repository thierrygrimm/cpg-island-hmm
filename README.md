# CpGIslandHMM
CpG island prediction with Hidden Markov Models, Viterbi and Baum-Welch algorithm


CpGIslandHMM [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=EFQXNQ7UYXYKW&source=url)
=======

[CpGIslandHMM](https://github.com/thierrygrimm/CpGIslandHMM) predicts CpG islands with Hidden Markov Models, the Viterbi and the Baum-Welch algorithm.

## Organization
### Parts
This project consists of two main parts
* [Hidden Markov Model & Viterbi algorithm](https://github.com/thierrygrimm/CpGIslandHMM/blob/master/Jupyter%20Notebooks/CpG%20islands%20Hidden%20Markov%20Model.ipynb)
* [Baum Welch algorithm](https://github.com/thierrygrimm/CpGIslandHMM/blob/master/Jupyter%20Notebooks/Baum-Welch%20algorithm.ipynb)

### Biochemical Foundations 

CpG islands are regions with a high frequency of CpG sites. Many genes in mammalian genomes have CpG islands associated with the promotor (start of the gene). In mammals, 70% to 80% of CpG cytosines are methylated changing the expression of the gene downstream. This field of study is part of epigenetics.

## Sections
### Hidden Markov Model & Viterbi algorithm
We model CpG islands by creating a Hidden Markov Model (HMM) of the 1st order. The model assumes the presence of two “hidden” states: **CpG island** and **nonCpG island**. We estimate parameters of the model by calculating transition, emission and initiation probabilities from a set of sequences. Using the Viterbi algorithm we find the most likely assignment of CpG islands in the test sequence. The results show that changing a nucleotide affects neighbors because we use the forward/backward algorithm.

<p align="center">
  <img src="Images/Viterbi.png">
</p>



### Baum Welch algorithm
We estimate transition and emission probabilities of the model only based on sequences containing CpG islands without known keys. We use the Baum Welch algorithm, which is a special case of the EM (expectation maximization) algorithm.  It makes use of the forward-backward algorithm to compute the statistics for our expectation step.

<p align="center">
  <img src="Images/BaumWelch.png">
</p>



## Issues

Found a bug? Want more features? Find something missing in the documentation? Let us know! Please don't hesitate to [file an issue](https://github.com/thierrygrimm/CpGIslandHMM/issues/new) and make a recommendation.

## License
```
CpGIslandHMM - CpG island prediction with Hidden Markov Models, Viterbi and Baum-Welch algorithm.

The MIT License (MIT)

Copyright (c) 2019 Thierry Grimm

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software ("CpGIslandHMM") and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```

