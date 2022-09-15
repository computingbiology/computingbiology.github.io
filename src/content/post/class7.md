+++
date = "13 Sep 2022"
draft = false
title = "Class 7"
author = "David Evans"
slug = "class7"
+++

## Project 2

[Project 2](/project2) is now posted, and is due on Wednesday, 21 September, 8:59pm.

**Correction to Alignment Code!** As was noticed in class today, the code for the gap-based alignment algorithms is wrong. The loops should include all values up to and including _j_ (so should be
```
range(1, j + 1)
```
instead of
```
range(1, j)
```
(note that `range` in Python iterates through the values from the first input up to, but not including, the second input value, so to include `j` in the iteration, we need to use `j + 1` in the range).

Thanks to Diego Wang for submitting [this pull request](https://github.com/computingbiology/Project-2-2022F/pull/1) with the fix and explanation.

If you have already modified your Project 2 notebook (which hopefully
is true for everyone!), you should incorporate [the
change](https://github.com/computingbiology/Project-2-2022F/pull/1/files)
manually into the code in your notebook to avoid losing the work you
have done. 

## Readings

See [Class 5](/class5) for this week's readings.

## Slides

The slides are here: [Class 7: Estimating Evolutionary Distance](https://www.dropbox.com/s/7rdahv7q85jq851/csbio-class7.pdf?dl=0)

Some links to materials for the class:

- Steven Henikoff and Jorja Henikoff. [_Amino acid substitution matrices from protein blocks_](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC50453/pdf/pnas01096-0363.pdf). Proceedings of the National Academy of Science, November 1992. This is the paper that introduced BLOSUM.

- Mark P Styczynski, Kyle L Jensen, Isidore Rigoutsos, and Gregory Stephanopoulos/ [_BLOSUM62 miscalculations improve search performance_](https://www.nature.com/articles/nbt0308-274). Nature Biotechnology, 2008.

- T. F. Smith and M. S. Waterman. [_Identification of common molecular subsequences_](/docs/smithwaterman1981.pdf). Journal of Molecular Biology, 1981. [Michael Waterman's UVA Webpage](https://biocomplexity.virginia.edu/person/michael-s-waterman)

- [NCBI Blast](https://blast.ncbi.nlm.nih.gov/Blast.cgi)


