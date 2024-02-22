---
layout: default
title: inspect
parent: Structurizr CLI
nav_order: 8
permalink: /cli/inspect
---

# inspect

The ```inspect``` command allows you to inspect a JSON/DSL workspace via the [workspace inspection feature](/workspaces/inspections).
The return code indicates the number of violations that were shown.

## Options

- -workspace: The path or URL to the workspace JSON/DSL file (required)
- -inspector: Provides a way to use a custom inspector; this needs to extend [Inspector](https://github.com/structurizr/java/blob/master/structurizr-inspection/src/main/java/com/structurizr/inspection/Inspector.java), with the compiled class(es) being available on the CLI classpath or packaged as a JAR file in a directory named `plugins` next to your workspace file (optional)
- -severity: A comma separated list of violation severities to show (optional; defaults to `error,warning,info,ignore`)

## Example

To inspect a JSON workspace definition:

```
./structurizr.sh inspect -workspace workspace.json
```

To inspect a JSON workspace definition, showing only errors and warnings:

```
./structurizr.sh inspect -workspace workspace.json -severity error,warning
```