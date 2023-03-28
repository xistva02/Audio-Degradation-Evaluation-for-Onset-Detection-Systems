# The Effect of Audio Degradation on Onset Detection Systems
Supplementary material for the paper: The Effect of Audio Degradation on Onset Detection Systems
  
Source: http://www.elektrorevue.cz/cz/clanky/zpracovani-signalu/0/the-effect-of-audio-degradation-on-onset-detection-systems/
BibTeX: 
@article{Istvanek_Elektrorevue_22,
  author="Matěj {Ištvánek}",
  title="The Effect of Audio Degradation on Onset Detection Systems",
  publisher="Elektrorevue",
  number="1",
  volume="24",
  year="2022",
  month="March",
  pages="1--13"
}

Onset detection is one of the subjects of research in the field of Music Information Retrieval (MIR). Onset detectors achieve relatively good results (see [MIREX website](https://nema.lis.illinois.edu/nema_out/mirex2018/results/aod/)), yet the "imaginary ceiling" has not yet been reached. In our study, we tested the degradation of the input audio signal of detectors to increase the accuracy and robustness of detection systems. The purpose was to explore the possibility of incorporating signal degradation into the pre-processing phase of detection systems to increase their accuracy.

A total of 6 degradations and 5 detection systems were tested. F-score, Recall, and Precision were calculated for each combination. The evaluation window was set to 50 ms and 100 ms.

Dataset: [onsets_ISMIR_2012](https://github.com/CPJKU/onset_db) – 321 audio excerpts with ground truth annotation available. Dataset is also divided into 6 categories: Bowed string (BS), Complex mixtures (CM), Non-pitched percussive (NPP), Pitched percussive (PP), Vocal, and Wind instruments (WI).

Main packages and software used: Python 3.7.6, Matlab 2015a, [Audio Degradation Toolbox](https://code.soundsoftware.ac.uk/projects/audio-degradation-toolbox), FFmpeg (libavcodec), [madmom](https://pypi.org/project/madmom/), [librosa](https://librosa.org/doc/latest/index.html), and [Sonic Visualiser](https://www.sonicvisualiser.org/).

Degradations:
  *	radio broadcast simulation
  *	smartphone playback simulation
  *	smart phone recording simulation
  *	mp3 64 kbps SBR
  *	mp3 320 kbps SBR
  *	Teager–Kaiser energy operator

Onset detectors:
  * [ComplexFlux](https://github.com/CPJKU/madmom/blob/master/bin/ComplexFlux)
  * [Librosa](https://librosa.org/doc/main/onset.html)
  *	[CNN](https://madmom.readthedocs.io/en/latest/modules/features/onsets.html)
  *	[RNN](https://madmom.readthedocs.io/en/latest/modules/features/onsets.html)
  *	[SuperFlux](https://github.com/CPJKU/madmom/blob/master/bin/SuperFluxNN)
