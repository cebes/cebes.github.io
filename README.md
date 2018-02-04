# Cebes Documentation

Our documentation uses extended Markdown, as implemented by MkDocs.

This repository is a github organization page, therefore all the source docs
is stored in the `source` branch. The `master` branch contains compiled docs,
which will be served by github.

## Building the documentation

- install dependencies: `pip install -r requirements.txt`
- Run:

        $ mkdocs serve # Starts a local webserver: localhost:8000
        $ mkdocs build # Builds a static site in "site" directory
   
## Deploy

    $ mkdocs gh-deploy -b master
    
## API Reference pages

They are taken from `cebes-python`:

```bash
/code/cebes/cebes-python$ pydocmd simple pycebes.core.dataframe.Dataframe++ pycebes.core.dataframe.GroupedDataframe+ > dataframe_reference.md
$ pydocmd simple pycebes.core.functions++ pycebes.core.column.Column+ > dataframe_functions.md
$ pydocmd simple pycebes.core.session.Session++ pycebes.core.session.CsvReadOptions++ pycebes.core.session.JsonReadOptions++ pycebes.core.session.ParquetReadOptions++ > session_api.md
```