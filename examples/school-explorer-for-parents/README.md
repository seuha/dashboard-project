Sample "solution" for the school explorer project.

## What's in here?

A number of the files in this repository should be carried over verbatim into the school-explorer project:
* The _site/_ folder -- Where students' code should go. It's where the application lives.
* Testing files (_.github/_, _\_\_tests\_\_/_)
* Configuration files (.eslintrc, .gitignore, .stylelintrc.json, jest.config.json, package.json)

A few things that don't get carried over to the school-explorer project:
* bin/ -- scripts to prepare the project, mainly for populating the site/data/ folder
* opt/ -- the actual raw data for running the scripts in bin/
* Python configuration -- _pyproject.toml_
* This README.md file

## Where do we get the data from?

The school district has some [data on OpenDataPhilly](https://opendataphilly.org/dataset?organization=school-district-of-philadelphia), but these just link to the school district's own data site. For example, this [school catchment areas](https://opendataphilly.org/dataset/school-information-data/resource/f6a27538-9131-4fbc-9906-808492c2d7ad) dataset on OpenDataPhilly links to [a download page](https://www.philasd.org/performance/programsservices/open-data/school-information/#school_catchment_areas) on the district site. While this is workable, it's not ideal from an automation standpoint -- I doubt the SDP site has any kind of stable API.

## Peparing data

### Schools

1.  Go to the [SDP download page](https://www.philasd.org/performance/programsservices/open-data/school-information/#school_lists) and download the latest CSV. Move it into _opt/_ and rename as _schools.csv_.

### Catchment areas

1.  Go to the [SDP download page](https://www.philasd.org/performance/programsservices/open-data/school-information/#school_catchment_areas) and download the latest shapefile. Move it into the _opt/_ folder and rename it _sdp\_catchments.zip_.