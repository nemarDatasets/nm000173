# Motor Imagery ataset from Ofner et al 2017

Motor Imagery ataset from Ofner et al 2017.

## Dataset Overview

- **Code**: Ofner2017
- **Paradigm**: imagery
- **DOI**: 10.1371/journal.pone.0182578
- **Subjects**: 15
- **Sessions per subject**: 2
- **Events**: right_elbow_flexion=1536, right_elbow_extension=1537, right_supination=1538, right_pronation=1539, right_hand_close=1540, right_hand_open=1541, rest=1542
- **Trial interval**: [0, 3] s
- **Runs per session**: 10
- **Session IDs**: movement_execution, motor_imagery
- **File format**: gdf

## Acquisition

- **Sampling rate**: 512.0 Hz
- **Number of channels**: 61
- **Channel types**: eeg=61, eog=3, misc=32
- **Channel names**: C1, C2, C3, C4, C5, C6, CCP1h, CCP2h, CCP3h, CCP4h, CCP5h, CCP6h, CP1, CP2, CP3, CP4, CP5, CP6, CPP1h, CPP2h, CPP3h, CPP4h, CPP5h, CPP6h, CPz, Cz, F1, F2, F3, F4, FC1, FC2, FC3, FC4, FC5, FC6, FCC1h, FCC2h, FCC3h, FCC4h, FCC5h, FCC6h, FCz, FFC1h, FFC2h, FFC3h, FFC4h, FFC5h, FFC6h, FTT7h, FTT8h, Fz, P1, P2, P3, P4, PPO1h, PPO2h, Pz, TTP7h, TTP8h, armeodummy-0, armeodummy-1, armeodummy-10, armeodummy-11, armeodummy-12, armeodummy-2, armeodummy-3, armeodummy-4, armeodummy-5, armeodummy-6, armeodummy-7, armeodummy-8, armeodummy-9, eog-l, eog-m, eog-r, gesture, index_far, index_middle, index_near, litte_far, litte_near, middle_far, middle_near, middle_ring, pitch, ring_far, ring_little, ring_near, roll, thumb_far, thumb_index, thumb_near, thumb_palm, wrist_bend
- **Montage**: standard_1005
- **Hardware**: g.tec medical engineering GmbH
- **Reference**: right mastoid
- **Ground**: AFz
- **Sensor type**: active
- **Line frequency**: 50.0 Hz
- **Online filters**: 0.01-200 Hz bandpass (8th order Chebyshev), 50 Hz notch

## Participants

- **Number of subjects**: 15
- **Health status**: healthy
- **Age**: mean=27.0, std=5.0, min=22.0, max=40.0
- **Gender distribution**: female=9, male=6
- **Handedness**: {'right': 14, 'left': 1}
- **Species**: human

## Experimental Protocol

- **Paradigm**: imagery
- **Number of classes**: 7
- **Class labels**: right_elbow_flexion, right_elbow_extension, right_supination, right_pronation, right_hand_close, right_hand_open, rest
- **Study design**: Trial-based paradigm with sustained movements/motor imagery. Each trial: fixation cross at 0s, cue presentation at 2s, sustained movement/MI execution. Subjects performed both movement execution (ME) and motor imagery (MI) in separate sessions.
- **Feedback type**: none
- **Stimulus type**: visual cue
- **Synchronicity**: synchronous
- **Mode**: offline
- **Training/test split**: False
- **Instructions**: Subjects were instructed to execute sustained movements in ME session and perform kinesthetic motor imagery in MI session. For rest class, subjects were instructed to avoid any movement and to stay in the starting position.

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  right_elbow_flexion
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine
          ├─ Flex
          └─ Right, Elbow

  right_elbow_extension
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine
          ├─ Stretch
          └─ Right, Elbow

  right_supination
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine
          ├─ Turn
          ├─ Right, Forearm
          └─ Label/supination

  right_pronation
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine
          ├─ Turn
          ├─ Right, Forearm
          └─ Label/pronation

  right_hand_close
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine
          ├─ Close
          └─ Right, Hand

  right_hand_open
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine
          ├─ Open
          └─ Right, Hand

  rest
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Rest

```
## Paradigm-Specific Parameters

- **Detected paradigm**: motor_imagery
- **Imagery tasks**: elbow_flexion, elbow_extension, forearm_supination, forearm_pronation, hand_open, hand_close

## Data Structure

- **Trials**: 420
- **Trials per class**: elbow_flexion=60, elbow_extension=60, forearm_supination=60, forearm_pronation=60, hand_open=60, hand_close=60, rest=60
- **Trials context**: per_session

## Preprocessing

- **Preprocessing applied**: False

## Signal Processing

- **Classifiers**: sLDA
- **Feature extraction**: time-domain signals, discriminative spatial patterns (DSP)
- **Frequency bands**: analyzed=[0.3, 3.0] Hz
- **Spatial filters**: sLORETA source localization

## Cross-Validation

- **Method**: 10x10-fold cross-validation
- **Folds**: 10
- **Evaluation type**: within-session

## Performance (Original Study)

- **Mov Vs Mov Me**: 55.0
- **Mov Vs Rest Me**: 87.0
- **Mov Vs Mov Mi**: 27.0
- **Mov Vs Rest Mi**: 73.0

## BCI Application

- **Applications**: neuroprosthesis, robotic_arm
- **Environment**: laboratory
- **Online feedback**: False

## Tags

- **Pathology**: Healthy
- **Modality**: Motor
- **Type**: Motor Imagery, Motor Execution

## Documentation

- **DOI**: 10.1371/journal.pone.0182578
- **Associated paper DOI**: 10.1371/journal.pone.0182578
- **License**: CC-BY-4.0
- **Investigators**: Patrick Ofner, Andreas Schwarz, Joana Pereira, Gernot R. Müller-Putz
- **Senior author**: Gernot R. Müller-Putz
- **Contact**: gernot.mueller@tugraz.at
- **Institution**: Graz University of Technology
- **Department**: Institute of Neural Engineering, BCI-Lab
- **Country**: AT
- **Repository**: BNCI Horizon 2020
- **Data URL**: https://bnci-horizon-2020.eu/database/data-sets
- **Publication year**: 2017
- **Funding**: H2020-643955 MoreGrasp; ERC Consolidator Grant ERC-681231 Feel Your Reach
- **Ethics approval**: Medical University of Graz, approval number 28-108 ex 15/16
- **Acknowledgements**: Data are available from the BNCI Horizon 2020 database at http://bnci-horizon-2020.eu/database/data-sets (accession number 001-2017) and from Zenodo at DOI 10.5281/zenodo.834976
- **Keywords**: upper limb movements, EEG, motor imagery, movement execution, low-frequency, time-domain, BCI, neuroprosthesis

## Abstract

How neural correlates of movements are represented in the human brain is of ongoing interest and has been researched with invasive and non-invasive methods. In this study, we analyzed the encoding of single upper limb movements in the time-domain of low-frequency electroencephalography (EEG) signals. Fifteen healthy subjects executed and imagined six different sustained upper limb movements. We classified these six movements and a rest class and obtained significant average classification accuracies of 55% (movement vs movement) and 87% (movement vs rest) for executed movements, and 27% and 73%, respectively, for imagined movements. Furthermore, we analyzed the classifier patterns in the source space and located the brain areas conveying discriminative movement information. The classifier patterns indicate that mainly premotor areas, primary motor cortex, somatosensory cortex and posterior parietal cortex convey discriminative movement information. The decoding of single upper limb movements is specially interesting in the context of a more natural non-invasive control of e.g., a motor neuroprosthesis or a robotic arm in highly motor disabled persons.

## Methodology

Subjects performed 6 sustained upper limb movements (elbow flexion/extension, forearm supination/pronation, hand open/close) plus rest in two separate sessions (movement execution and motor imagery). EEG was recorded from 61 channels, filtered to 0.3-3 Hz, and classified using shrinkage LDA with discriminative spatial patterns. Source localization was performed using sLORETA. Classification employed both single time-point and time-window approaches with 10x10-fold cross-validation.

## References

Ofner, P., Schwarz, A., Pereira, J. and Müller-Putz, G.R., 2017. Upper limb movements can be decoded from the time-domain of low-frequency EEG. PloS one, 12(8), p.e0182578. https://doi.org/10.1371/journal.pone.0182578
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
