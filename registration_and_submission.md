---
title: Registration and Submissions
feature_image: "https://raw.githubusercontent.com/MUnitQuest/MUnitQuest.github.io/refs/heads/main/Images/header2.jpeg"
feature_text: 
---

### Registartion

The registration plattform will be launched soon.


### Dataset submissions

For obtaining a diverse competition data collection that balances relism and label quality, we invite the submission of both experimental and simulated data. In short, depending on the type of data you want to contribute, a submission consists of the following parts: 

![Submission Requirements](/Images/submissionRequirements.jpg)

- **EMG data and metadata:** We will provide the EMG data entering the competition in the standardized [EMG-BIDS](https://bids-specification.readthedocs.io/en/stable/modality-specific-files/electromyography.html) format. To make getting started with EMG-BIDS as easy as possible, we support two options for your data submission:
    - Upload of EMG-BIDS-formatted data, which we facilitate by providing template files that you can adopt according to your specific recording setup
    - Assisted generation of EMG-BIDS compatible metadata files through a web interface (coming soon)

- **Labeled Motor Unit Spike Trains:** A key requirement for a competition on motor unit identification methods is the availability of labeled ground truth spikes. Thus, we additionally require submitting:
    - for each recording, a *.tsv* file (BIDS-events file, see example below) containing the labeled motor unit spike trains 
    - a short description (2-page PDF) of the utilized labelling approach (for experimental EMG data)
    - or a short description (2-page PDF) of the simulation model (for synthetic EMG data)

Further details are comming soon.    

### Algorithm submission   

This is a prediction submission competition. During both **Phase 1** and **Phase 2** you will be asked to upload, for each recording, a tabular file (*_events.tsv*) containing your predicted motor unit spikes (BIDS-events file) together with a *_log.json* file describing essential process metadata (further details to be announced). To be eligible for awards, you need to openly share your code (e.g., via GitHub). 


### Example: how to report motor unit spike trains

Here is a minimal example of the format (BIDS-event file) used for submitting motor unit spike trains (both for labels and algorithm predictions):    

| **onset** | **duration** | **sample** | **unit_id** | **event_description** |
| --------- | ------------ | ---------- | ----------- | ----------------------|
| 0.001     | 0            | 1          | 0           | Motor-unit-spike      |
| 0.005     | 0            | 5          | 1           | Motor-unit-spike      |
| 0.011     | 0            | 11         | 0           | Motor-unit-spike      |
| 0.012     | 0            | 12         | 2           | Motor-unit-spike      |
| 0.016     | 0            | 16         | 1           | Motor-unit-spike      |
| ...       | ...          | ...        | ...         | ...      |
 
