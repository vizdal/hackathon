# Filter Construction Tool

In our product we have the ability for users to define filters over their
data. Unfortunately, the users will have to know what are all the possible
fields and values they can filter on. In addition they have to represent
the filter in form of an abstract syntax tree (AST) as the system does not
support any query language. This use is not intuitive to users and they
would more likely have an easier time with either a graphical tool or some
query language with [IntelliSense/auto-complete](https://en.wikipedia.org/wiki/Intelligent_code_completion) editor. For this challenge
we provide the data sets whose attributes need to be filtered and a REST
API which accepts filter definitions in form of an abstract syntax tree.

## Objectives

- Develop a solution that helps users define multiple filters against a
  specified data set
- Constructed filters can be saved using the Analyze Re API
- Solution is a service with an intuitive API, some UI, or a combination of both
- Consider a wizard type approach or query language with auto-complete
- Ensure constructed filters are valid, matching only attributes and values that
  occur in the data set
- You can choose whatever programming language you prefer
- If you develop a service, try to leverage server-less frameworks if possible
- If you develop a UI it should either be cross-platform (Windows / Linux / Mac)
  or web-based

## File Format Specification

The data sets for which filters should be generated are called *Event
Catalogs* in Analyze Re terminology. Event catalogs are provided by the
user in form of a CSV file with the following format:

| Column Name | Description                     | Type                             | Required |
|-------------|---------------------------------|----------------------------------|----------|
| EventId     | ID of the event in the catalog  | `integer`                        | yes      |
| Rate        | Rate of occurrence of the event | `float`                          | yes      |
| Meta1       | Event metadata                  | `integer` or `float` or `string` | no       |
| Meta2       | Event metadata                  | `integer` or `float` or `string` | no       |
| ...         | Event metadata                  | `integer` or `float` or `string` | no       |
| MetaN       | Event metadata                  | `integer` or `float` or `string` | no       |

The fields Meta1, Meta2, ..., MetaN are metadata fields that are optional and provide additional information for each event. These are the fields that users typically want to filter on.

## API Specification

An Event Catalog CSV file is uploaded to the Analyze Re platform API
against an Event Catalog metadata object. As part of the upload process the
API server generates an Event Catalog Profile that lists all the attributes
and their distinct values for the catalog. You can inspect an example of
such profile at:

https://hackaton-api.analyzere.net/event_catalogs/a2d9fb3a-b60b-489d-8a6d-1ef738353186/profile

You may use this profile or the data from the CSV file to guide the use
through the creation of filters.

The [Analyze Re REST API documentation](http://docs.analyzere.net/)
describes [how filters are defined and created](http://docs.analyzere.net/#loss-filters) 
on the Analyze Re platform. It provides examples of each of the different filter 
types and how different filters can be combined to define more complex filter
criteria.

## Example Data Sets

You can find two example Event Catalog CSV files
here:

- [catalog_1.csv.xz](catalog_1.csv.xz) (24 MB)
- [catalog_2.csv.xz](catalog_2.csv.xz) (29 kB)

There is also an Analyze Re platform environment set up that already has
some event catalogs configured. They can be found via the following URL:

https://hackaton-api.analyzere.net/event_catalogs/

A specific event catalog is addressed by including its ID in the URL:

https://hackaton-api.analyzere.net/event_catalogs/a2d9fb3a-b60b-489d-8a6d-1ef738353186

In addition, each event catalog comes with a profile, that lists all the
attributes and distinct attribute values:

https://hackaton-api.analyzere.net/event_catalogs/a2d9fb3a-b60b-489d-8a6d-1ef738353186/profile

Each event catalog also links to its respective CSV file:

https://hackaton-api.analyzere.net/uploads/files/a2d9fb3a-b60b-489d-8a6d-1ef738353186.csv


## Useful Links

- [Analyze Re Python API Bindings](https://github.com/analyzere/analyzere-python)
- [Analyze Re C# API Bindings](https://www.nuget.org/packages/AnalyzeRe.Client/)
- [Analyze Re REST API Documentation](http://docs.analyzere.net/)
- [pipenv](https://pipenv.readthedocs.io/en/latest/) - Python Dev Workflow for Humans
- [Jupyter](https://jupyter.org/) - An interactive notebook
- [Bokeh](https://bokeh.pydata.org/en/latest/) - Interactive visualizations in Python
- [JointJS](https://www.jointjs.com/) - JavaScript library for flowchart visualization
