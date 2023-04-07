This repo contains the evaluation scripts needed to replicate the IWSLT 2023 speech translation tasks for Quechua to Spanish.

# IWSLT 2023 Dialectal and Low-Resource Speech Translation Task 

This is a Python script for evaluating the performance of speech translation systems using the BLEU and chrF metrics. The script takes as input a reference text file and a folder containing the hypothesis text files. It processes each hypothesis file and outputs the results in a tab-separated values (TSV) file.


<a href="https://iwslt.org/2023/low-resource">IWSLT 2023 task homepage</a>


## Requirements

- Python 3.x
- pandas
- bleu_scorer
- chrF_scorer

## Installation

Markup : 1. Clone the repository: git clone https://github.com/your-username/speech-translation-evaluation-script.git
	     2. Navigate to the repository directory: cd speech-translation-evaluation-script
         3. Install the dependencies: pip install -r requirements.txt

## Usage

Markup : 1. Ensure that your reference file and hypothesis files are named correctly.
         2. Open a terminal and navigate to the repository directory.
         3. Run the script with the following command:

```
python evaluation.py --ref /path/to/reference/file --phyp /path/to/hypotheses/folder
```

		 4. Wait for the script to finish processing all the hypothesis files.
         5. Find the results in a TSV file named results.tsv in the hypothesis folder.


## Reference File

The reference file is a plain text file containing the ground truth translations for each source sentence. Each line in the file represents one sentence, and each sentence should be separated by a newline character.

## Hypotheses Folder

The hypotheses folder should contain one or more plain text files, each containing the translations generated by a speech translation system. Each file should be named in the following format: {team_id}.st.{condition}.primary.que-spa.txt. Here, {team_id} is a unique identifier for the team that generated the translations, {condition} is either constrained or unconstrained, and primary is the name of the translation type.

## Results

The output file results.tsv contains the following columns:

Markup : *Participant: the unique identifier for each team that generated the translations.
         *Condition: the condition under which the translations were generated (constrained or unconstrained).
         *Type: the name of the translation type (primary, contrastive1, or contrastive2).
         *BLEU: the BLEU score for each set of translations.
         *chrF: the chrF score for each set of translations. 

## License

This project is licensed under the MIT License - see the LICENSE file for details.
