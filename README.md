# CancerDataServices-SubmissionValidationR
Tool for validating the Cancer Data Service's (CDS) Metadata Template in R

This R Script takes a data file that is formatted to the [submission template for CDS](https://github.com/CBIIT/cds-model/tree/main/metadata-manifest) as input. It will output a file that describes whether sections of the Metadata table PASS, ERROR or WARNING on the checks.

To run the script on a CDS template, run the following command in a terminal where R is installed for help.

```
Rscript --vanilla CDS-Submission_ValidationR.R --help
```


```
Usage: CDS-Submission_ValidationR.R [options]

CDS-Submission_ValidationR v2.0.0

Options:
	-f CHARACTER, --file=CHARACTER
		dataset file (.xlsx, .tsv, .csv)

	-t CHARACTER, --template=CHARACTER
		dataset template file, CDS_submission_metadata_template

	-h, --help
		Show this help message and exit
```

To test the script on one of the provided test files:

```
Rscript --vanilla CDS-Submission_ValidationR.R -f test_files_v1.3.1/a_all_pass-v1.3.1.xlsx -t CDS_submission_metadata_template
```

`Note: The AWS bucket checks will not work with any of the test files, as the files and their locations are fake data`
