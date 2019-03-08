# CSV Validator

Our platform allows users to upload files in CSV form that must follow a
very specific format. We currently have no fast way of checking the
validity of these CSV files prior to upload and only encounter errors
during a rather slow conversion process server-side. The challenge is to
develop a tool or extension to our [Python API
Bindings](https://github.com/analyzere/analyzere-python) that can quickly
and flexibly perform validity checks on large CSV files client-side before
upload.

## Objectives

- Develop a client-side tool (preferably integrated with the [Analyze Re
  Python API Extras
  Package](https://github.com/analyzere/analyzere-python-extras)) which
  performs validation of input files before upload
- Detect as many formatting errors simultaneously as possible to avoid
  revalidating input files one error at a time (just like a compiler output
  more than one error in your source code)
- Keep the acceptable format definition flexible to allow future changes
  and expansion to other CSV formats

## File Format Specification

The specifications for each file format can be found in the Analyze Re Data
Formats documentation:

- [Analyze Re Data Formats](analyze-re-data-formats.pdf) (PDF)

## API Specification

You can validate the effectiveness of your solution by uploading corrected
input files directly to the Analyze Re platform. We have an environment
setup at https://hackaton-api.analyzere.net which you can use during the
event.

You can learn about how to interact with the Analyze Re platform API using
the API documentation which can be found at:

- http://docs.analyzere.net

## Example Data Sets

There are some example files for different formats that you can use to get
started:

- [catalog_correct.csv](catalog_correct.csv) - Event Catalog (correct
  format)
- [catalog_incorrect.csv](catalog_incorrect.csv) - Event Catalog (incorrect
  format)
- [yelt_correct.csv](yelt_correct.csv) - YELT file (correct format)
- [yelt_incorrect.csv](yelt_incorrect.csv) - YELT file (incorrect format)

## Useful Links

- [Analyze Re Python API Bindings](https://github.com/analyzere/analyzere-python)
- [Analyze Re Python API Extras](https://github.com/analyzere/analyzere-python-extras)
- [Analyze Re REST API Documentation](http://docs.analyzere.net/)
- [pipenv](https://pipenv.readthedocs.io/en/latest/) - Python Dev Workflow for Humans
- [Jupyter](https://jupyter.org/) - An interactive notebook
