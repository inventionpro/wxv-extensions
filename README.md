# WXV Extensions

This repo serves to store some public extensions, host the basic builder, and the extension docs

## Docs

An extension file is a json object with the following properties:
- title: the extension title
- icon: data uri or url that serves as an icon (data uri preffered)
- version: the version of the extension (any format)
- author: who nade the extension
- desc: description of the extension
- hooks: an object containing the extension hooks

### hooks

each object key is the hook, the ones available are:
- netRequest
- netResponse
- tabCreate
- tabLoad
- tabFocus
- tabClose

the strucutre of inner object contains:
- type: currently only "JS"
- code: what to run (as if it was inside a function)
