# AxcCourier-WebUI

React components for AxcCourier: API definition editing, docs, single and batch request runs, scenarios and
environments. No accounts, no routing. Data comes through a host-supplied client.

**Status: design stage.** This repository does not yet contain an implementation, an installable package or runnable
examples. The capabilities below are design goals.

## Overview

AxcCourier-WebUI is an installable TypeScript / React component package for the
[AxcCourier](https://github.com/axclogo/AxcCourier) request engine. It provides components for these tasks:

- Editing OpenAPI 3.x definitions and their `x-axc-*` extensions
- Rendering API documentation with Scalar
- Sending single requests and inspecting the request, response and assertion results
- Running Excel-driven batches with template download, upload, progress, stop and result export
- Building multi-step scenarios
- Managing environments and variables
- Importing and exporting definitions, and generating code samples

Assertions and formatting branches are edited with `@axc/uikit/condition`. Bodies, parameters and plugin configs are
edited with `@axc/uikit/json-editor`. The package has no accounts, routing or network layer of its own: the host
passes in a client adapter and handles identity, storage and calls to the engine. TypeScript types are generated from
the JSON Schemas that AxcCourier publishes.

## Related

- [AxcCourier](https://github.com/axclogo/AxcCourier): the request engine.
- [AxcUIKit-TypeScript](https://github.com/axclogo/AxcUIKit-TypeScript): condition and JSON editor components.
