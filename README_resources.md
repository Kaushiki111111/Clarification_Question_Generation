# Resources 

Training data, model outputs and pretrained checkpoints for WWW 2021 paper ``Diverse and Specific Clarification Question Generation with Keywords"

- data
  - contains the processed and cleaned *Home and Kitchen* dataset
- data_office
  - contains the processed and cleaned *Office* dataset
- output
  - contains all outputs on the test set of *Home and Kitchen* of the 7 compared systems in Table 4
    - beam: KPCNet(-filter)
    - beam_filt: KPCNet(beam)
    - diverse_beam: KPCNet(divbeam)
    - hMup: hMup
    - kwd_cluster: KPCNet(cluster)
    - kwd_samples: KPCNet(sample)
    - MLE: MLE
  - the suffix like `beam`+X, where X indicates the order in beam search
    - hMup is an exception. X indicates the id of the *expert*. `beam4` achieved the best BLEU, and is thus used in both individual and group level evaluation.
  - the suffix for kwd_cluster and kwd_samples has an additional `a`+X, where X indicates the group id for conditioning keyword set
  - All variants of KPCNet has additional file with suffix `kwd_samples`
    - The words on the i-th line are conditioning keywords for the i-th sample
- ckpt
  - pretrained model checkpoint
- hparams
  - hyperparameters for the pretrained checkpoint