# CSV Validator

Keywords: Python, CSV, file processing, client-side, REST

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

## API Specification

## Example Data Sets

## Starter Code

## Useful Links

- [Analyze Re Python API Bindings](https://github.com/analyzere/analyzere-python)
- [Analyze Re Python API Extras](https://github.com/analyzere/analyzere-python-extras)
- [Analyze Re REST API Documentation](http://docs.analyzere.net/)
- [pipenv](https://pipenv.readthedocs.io/en/latest/) - Python Dev Workflow for Humans
- [Jupyter](https://jupyter.org/) - An interactive notebook