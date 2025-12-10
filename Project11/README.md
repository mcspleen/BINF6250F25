# Introduction
This project explores Profile Hidden Markov Models and protein motif predictions.

# Pseudocode

```
Need function to read fasta files and extract msa's.
  - Sequences returned as key-value pairs with header
  - Read line by line
  - Header line starts with ">"
  - Account for end line

Need to define helper function _count_transitions_from _msa() for transition estimate.
  - Store as a dictionary
  - Start with "Begin" for future functions
  - "-" codes for deletion
  - Attach "End" for future functions

Need to change Viterbi, Forward, Backward, and Baum-Welch to work with states "I", "M", and "D"
and alphabet "ACDEFGHIKLMNPQRSTVWY".
  - Once adapted, we can fill  out `_forward_table()`, `_backward_table()`, `_compute_posterior()`,
    `_reestimate_emissions()`, and `_reestimate_transitions()`

```

# Successes
We successfully added functions to extract msa's from fasta files, hard-code allowable transitions, and count transitions 
from the msa's. We also were able to the Viterbi and Forward algorithms from the `HMMBase` class to work with the new 
states and alphabet in the Profile HMM. 

# Struggles
We were unable to get to `_reestimate_emissions()` and `_reestimate_transitions()`, as well as fully adapting the Backward 
and Baum-Welch algorithms. Within our `_compute_posterior()`, we utilized `HMMBase`'s Backward algorithm. 

# Personal Reflections
## Group Leader (Jason)
This project was really tough, especially with the timing of the semester. I would love to continue learning about this as 
the coding behind protein structure prediction has been a mystery to me since first learning about it in biochemistry. 

## Other member
Other members' reflections on the project

# Generative AI Appendix
As per the syllabus
