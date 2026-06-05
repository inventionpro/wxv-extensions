# WXV Extensions

This repo serves to store some public extensions, host the basic builder, and the extension docs

## Docs

An extension file is a json object with the following properties:
- name: the extension name (1-50 chars)
- icon: data uri or url that serves as an icon (data uri preffered, optional)
- version: the version of the extension (any format, 1-20 chars, a "v" will be prefixed)
- author: who made the extension (1-20 chars)
- desc: description of the extension (0-250 chars)
- hooks: an object containing the extension hooks

### hooks

each object key is the hook, the ones available are:
- netRequest: (request: { url: String }) => { url: String } | { block: true }
- netResponse: (response: String) => String
- tabCreate: (tab: Tab) => void
- tabLoad: (tab: Tab) => void
- tabFocus: (tab: Tab) => void
- tabClose: (tab: Tab) => void

the strucutre of inner object contains:
- type: currently only "JS"
- code: what to run (as if it was inside a function)
