<!--
SPDX-FileCopyrightText: 2020 Benedict Harcourt

SPDX-License-Identifier: BSD-2-Clause
-->

# Micro 'TurboLinks' implementation

![JS Lint](https://github.com/javajawa/microturbolinks/workflows/JS%20Lint/badge.svg)
![SPDX Lint](https://github.com/javajawa/microturbolinks/workflows/SPDX%20Lint/badge.svg)

Lightweight library that replaces internal links with an AJAX call and a
partial replace of elements on the page.

It is currently untested.

Usage:

```js
import { addDefaultHooks } from '/path/to/turbolinks.js';

addDefaultHooks();
```

You can prevent a page being loaded this way by cancelling the `turbo:fetch`
event that is raised when the click occurs (the default action will happen
instead).

You can prevent a section of the page being unloaded by cancelling the
`turbo:delete` event. This is useful to prevent JS generated elements from
being removed.
