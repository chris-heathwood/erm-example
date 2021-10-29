# erm-example

This sample repo shows how you can generate an Entity Relationship Model from a postgres database.

This uses a cut down sample of the test dvd rental database available here:

https://www.postgresqltutorial.com/postgresql-sample-database/

This works by running the database using docker and then a combination of github actions and a go programme to get it to render.

1. https://github.com/achiku/planter
    * Renders the schema as uml
1. https://github.com/cloudbees/plantuml-github-action
    * Takes this uml and turns it in to a png
1. https://github.com/kai-tub/external-repo-sync-action
    * Takes this png and syncs it to the wiki

## Current schema

This schema is auto generated whenever there is a merge out to main:

![Schema](https://github.com/chris-heathwood/erm-example/wiki/schema.png)

You can see the raw uml [here](https://github.com/chris-heathwood/erm-example/wiki/schema.uml).
