# Project Zero Handbook

A wiki-like set of articles to help _you_ build _your_ game.

## Requirements

### Building Wiki

This project uses [SkyDocs](https://skydocs.skyost.eu/en/) to build the wiki from Markdown.

To build the wiki, run
```
java -jar skydocs.jar build
```

To have the wiki served in localhost, do
```
java -jar skydocs.jar serve
```

# Using GitHub pages

Github Pages will only check `docs/` directory
```
java -jar skydocs.jar build
cp build/* docs/* -r
```
