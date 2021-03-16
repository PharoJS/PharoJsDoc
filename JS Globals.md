# JS Globals

`PjJavascriptGlobals` and its subclasses such as `PjDomGlobals` are pools of shared variables. Those are variables shared among different classes. A class that uses a pool refers to it in definition under `poolDictionaries:` . See for example `PjDOMApplication`.

Note that pool dictionaries is a feature of Pharo. We're just using it to define and use JS globals.