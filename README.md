# Documentation

This repository lists projects and websites part of the [NYC Space/Time Directory](http://spacetime.nypl.org), how they were built, and how they work together. You can also see the project’s [interactive architecture diagram](http://spacetime.nypl.org/architecture/) for more information.

## Homepage

- __Description__: Project’s homepage
- __URL__: http://spacetime.nypl.org
- __GitHub__: https://github.com/nypl-spacetime/nypl-spacetime.github.io
- __Technology__: Static [Jekyll](https://jekyllrb.com/) website, hosted via [GitHub Pages](https://pages.github.com/)
- __Dependencies__: Users can download open historical geospatial [datasets](#datasets) via the project’s homepage, they are hosted on [AWS S3](#aws-s3)

## Surveyor

- __Description__: Website for crowdsourced geotagging of NYPL’s photo collections
- __URL__: http://spacetime.nypl.org/surveyor
- __GitHub__: https://github.com/nypl-spacetime/surveyor
- __Technology__: React app, hosted on GitHub Pages. Surveyor reads photo data from the Brick-by-brick API, and writes submissions there, too
- __Dependencies__: [Brick-by-brick API](#brick-by-brick)

## Atlas

- __Description__: Map and search interface for NYC Space/Time Directory data
- __URL__: http://spacetime.nypl.org/atlas
- __GitHub__: https://github.com/nypl-spacetime/atlas
- __Technology__: React app, hosted on GitHub Pages
- __Dependencies__: [Search API](#search-api)

## Maps by Decade

- __Description__: Website to browse digitized and georectified NYPL maps in a visual way
- __URL__: http://spacetime.nypl.org/maps-by-decade
- __GitHub__: https://github.com/nypl-spacetime/maps-by-decade
- __Technology__: React app, hosted on GitHub Pages. Maps by Decade needs two JSON data files to function, but does not depend on a database or API
- __Dependencies__: [`group-maps`](http://s3.amazonaws.com/spacetime-nypl-org/datasets/group-maps/maps-by-decade.grouped.json) dataset on [AWS S3](#aws-s3) (served via CloudFront)

## Digital Collections Tab

- __Description__: Browser extension that shows a photo from Ditigal Collections when users open a new tab
- __URL__: https://www.nypl.org/blog/2017/08/31/digital-collections-tab
- __GitHub__: https://github.com/nypl-spacetime/digital-collections-tab
- __Technology__: HTML + JavaScript
- __Dependencies__: [Brick-by-brick](#brick-by-brick) (but the Tab extension will keep working with a set of offline images when Brick-by-brick is offline)

## Extract/Transform/Load modules

- __Description__:
- __URL__:
- __GitHub__:
- __Technology__:
- __Dependencies__:

## Datasets

- __Description__:
- __URL__: http://spacetime.nypl.org/#data
- __Technology__:
- __Dependencies__: [AWS S3](#aws-s3)

## AWS S3

- __Description__:
- __URL__: https://s3.amazonaws.com/spacetime-nypl-org/
- __Dependencies__:

## Search API

- __Description__: Search API for NYC Space/Time Directory data
- __URL__: https://fpr9gjsw3c.execute-api.us-east-1.amazonaws.com/dev/
- __GitHub__: https://github.com/nypl-spacetime/spacetime-api
- __Technology__: Serverless Node.js Express app on AWS Lambda
- __Dependencies__: AWS Elasticsearch index, with NYC Space/Time Directory data, ingested with [`etl-elasticsearch-ingest`](https://github.com/nypl-spacetime/etl-elasticsearch-ingest)

## Brick-by-brick

- __Description__: Simple JSON API for small crowdsourcing apps
- __URL__: http://brick-by-brick.herokuapp.com/
- __GitHub__: https://github.com/nypl-spacetime/brick-by-brick
- __Technology__: Node.js/Express API, with PostgreSQL database
- __Dependencies__: Heroku

## Architecture

- __Description__:
- __URL__: http://spacetime.nypl.org/architecture/
- __GitHub__: https://github.com/nypl-spacetime/architecture
- __Technology__: HTML + JavaScript
- __Dependencies__: [`data-dependencies`](http://s3.amazonaws.com/spacetime-nypl-org/datasets/data-dependencies/spacetime-graph.svg) dataset on [AWS S3](#aws-s3) (served via CloudFront)

## Map Warper

- __Description__: Website for crowdsourced map georectification
- __URL__: http://maps.nypl.org/warper/
- __GitHub__: https://github.com/nypl-spacetime/nypl-warper
- __Technology__: Ruby on Rails with PostgreSQL database, as well as [GDAL](http://www.gdal.org/) and [GeoServer](http://geoserver.org/)
- __Dependencies__: Server hosted by NYPL’s IT Department

## Building Inspector

- __Description__: Crowdsourced extraction of building and address data from historical maps
- __URL__: http://buildinginspector.nypl.org/
- __GitHub__: https://github.com/nypl-spacetime/building-inspector
- __Technology__: Ruby on Rails with PostgreSQL database
- __Dependencies__: Heroku
