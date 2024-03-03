===========================
Introduction
===========================

Welcome to the Theunissen lab CRCNS data, released February 2011.

This data took years to collect, and any work derived from this data should be properly attributed to the experimenters, Sarah M.N. Woolley sw2277@columbia.edu and Thane Fremouw Thane_Fremouw@umit.maine.edu.  It's also good manners to *ask* them first if you could use their fine data, and it's pretty much essential to include them in the paper-editing process and to give them co-authorship if they want to be included. If worst comes to worst, they do not have veto power over what you do with this data, but it's better for everyone if we don't go all legalistic on each other.

On this volume, you will find all of the raw data collected by Sarah and Thane which went into the preprocessing paper (Gill et Al. 2006) as well as all the other stimuli which were played to these neurons.  Additionally, you will find every neuron with a compatible stimulus presentation protocol in regions MLd, L, and CM which the Theunissen lab has collected as of September 1st, 2007.

The root directory of this CD has two special directories:

* all_stims: all the .wav files used  as stimuli
* all_cells: all the cells with their associated stimulus/response data

It also contains some useful .csv files

* cell_regions.csv: maps cell names to an anatomical region. Regions MLd, OV (Nucleus Ovidalis, Amin et Al. 2010), Field L (L1, L2a, L2b, L3), and CM are included. "None" signifies that a region was not identified with the cell.
* cell_stim_classes.csv: maps cell names to the stimulus classes supplied (conspecific, flatrip, songrip)
* stim_data.csv: maps .wav files to the following columns: fileName,sampleRate,depth,numSamples,stimClass


References:

http://www.ncbi.nlm.nih.gov/pubmed/16633939
Sound representation methods for spectro-temporal receptive field estimation.
Journal of Computational Neuroscience (10.1007/s10827-006-7059-4).
Patrick Gill, Junli Zhang, Sarah M. N. Woolley, Thane Fremouw and Frederic E. Theunissen

Information about stimuli and responses from OV can be found in this paper:

http://www.ncbi.nlm.nih.gov/pubmed/20554842
Role of the Zebra Finch Auditory Thalamus in Generating Complex Representations for Natural Sounds.
Journal of Neurophysiology (2010 Aug;104(2):784-98).
Noopur Amin, Patrick Gill, Frederic E Theunissen


===========================
Stimulus Classes
===========================

Each cell is presented with stimuli from 2-3 classes:

1) flatrip: modulation-limited noise with a (somewhat) flat modulation spectrum (ML-Noise)
2) songrip: ripple stimuli with the same modulation spectrum as song
3) conspecific: natural birdsong from zebra finch


===========================
Stimuli
===========================

The "all_stims" directory contains the .wav file corresponding to each stimulus used. All .wav files here had a sampling rate of 32000 Hz and a sampling depth of 16 bits. See the next section for information on how to relate a stimulus to a response.


===========================
The all_cells Directory
===========================

This directory contains a list of all cells in the dataset. Each cell directory is named with a pattern:

<bird name>_<unit number>

For example, "blugr1612_2" corresponds to bird "blugr1612", cell "2". There are 4 cells from that bird. A look into "cell_regions.csv" shows that all 4 cells from bird blugr1612 correspond to the anatomical region OV.

Another example: the directory "rr1416_5_B" corresponds to bird bird "rr1416", cell "5_B". A look into cell_regions.csv shows that there are 4 cells from this bird, all in Field L.

The subdirectory of each cell type contains a set of directories, each corresponding to a stimulus class, either "conspecific", "flatrip", or "songrip" (see "Stimulus Classes" above).

In each stimulus class subdirectory, there is a group of files:

1) Spike files: prefixed with "spike", contains a list of spike times for each stimulus presentation. The # of rows in this file is equal to the # of stimulus presentations, spike times with respect to stimulus onset are given in milliseconds. Negative spike times are given for spikes that occur prior to stimulus presentation.

2) Stimulus Files: prefixed with "stim". The stim1, stim2, etc. files are plain text files, and contain just the stimulus name. So, if a stim file has the text "D54ABC42488F995C789F351A34316039.wav" it means the corresponding wav file is in all_stims/D54ABC42488F995C789F351A34316039.wav.

Have fun!  Frederic Theunissen can be contacted at theunissen@berkeley.edu.


