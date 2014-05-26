# What is this?

This is a toy application that shows some basic capabilities of FLOD. FLOD is a framework for Linked Data, available at [https://github.com/alangrafu/flod](https://github.com/alangrafu/flod).

# Installation

## Data loading

Download the data from `http://graves.cl/ghi/globalHungerIndex.rdf.gz` and load it into your triple store in the named graph `http://graves.cl/ghi`

## Installing FLOD and this application

First, open a terminal and enter

```
bash < <(curl -skL http://lodspeakr.org/flod)
```

Git will clone the flod engine repository. When asked `Do you want to use an existing repository as a default component folder? Add URL if yes, empty otherwise:` you must enter THIS repo's git URI

```
https://github.com/alangrafu/ghi-flod-app.git
```

## Configuring

Open `flod/components/settings.json` and edit your `local` endpoint to point correctly. In my case I used Fuseki, so my endpoint was `http://localhost:3030/ghi/query`

```
"endpoints": {
        "local": "http://localhost:3030/ghi/query",
        "dbpedia": "http://dbpedia.org/sparql"
    },
```

## Running

```
cd flod
./start.sh
```

and point your browser to `http://localhost:5113`