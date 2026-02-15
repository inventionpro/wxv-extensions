# WXV Extensions

This repo serves to store some public extensions, host the basic builder, and the extension docs

## Docs

An extension file is a json object with the following properties:
- title: the extension title (1-50 chars)
- icon: data uri or url that serves as an icon (data uri preffered, optional)
- version: the version of the extension (any format, 1-20 chars)
- author: who nade the extension (1-20 chars)
- desc: description of the extension (0-250 chars)
- hooks: an object containing the extension hooks

### hooks

each object key is the hook, the ones available are:
- netRequest: (Request: { url: string }) => Request | { block: true }
- netResponse: (Response: string) => Response
- tabCreate: (Tab: wxv_object) => void
- tabLoad: (Tab: wxv_object) => void
- tabFocus: (Tab: wxv_object) => void
- tabClose: (Tab: wxv_object) => void

the strucutre of inner object contains:
- type: currently only "JS"
- code: what to run (as if it was inside a function)
