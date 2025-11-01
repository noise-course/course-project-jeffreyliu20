# Project Title

## Project Participants

Format the following information in a markdown table:

* Jeffrey Liu
* jliu26
* Solo

## Project Description

One paragraph description of your project. Summarize the following:
Problem. Detect malware vs. benign network flows directly from raw PCAPs.
Why it matters. Practical malware detection from network traces helps SOCs triage threats when payloads are encrypted or unavailable.
Course fit. This intersects networking and ML:using data of network activity involving malware, converting packets/flows into ML-ready features, training/evaluating models, and reasoning about systems cost.
Related work. netML challenge; nPrint/pcapML pipelines; leaderboards with baseline results using tabular models.
The goal will be to reproduce baseline results on the netML Malware Detection dataset (binary and 19-class).

## Data

Dataset: netML Malware Detection (Stratosphere IPS; <10 GB PCAPs; IPv4 TCP/UDP).

pcapML: flow/time-window statistics (sizes, IATs, flags, ports, burstiness).

nPrint: fixed-length packet fingerprints aggregated per flow (means/max/percentiles) with an optional short packet-sequence encoder.

Models: Logistic Regression, Linear/Kernel SVM, Random Forest

Evaluation:

Primary metric: Balanced Accuracy (per dataset guidance).

Secondary: F1-macro, ROC-AUC (binary), confusion matrices, per-family results.

Robustness: Family-held-out evaluation.

Systems-cost study: Instrument and report wall-clock time, peak RAM, CPU%, and artifact size for each feature pipeline and key ablations (e.g., top-N packets, reduced header fields). Present accuracy-vs-cost curves to recommend a “best value” configuration.

## Deliverables

* Detail what you intend to turn in for the final project. 
Notebook and report

