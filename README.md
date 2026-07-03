# @global-torque/admin-html-patterns

Prepare-next server-rendered HTML pattern catalog for Django/admin consumers.

The package records reusable markup contracts. It does not render application
data, own Django template includes, ship Vue components, read env config, or
import Webdevelop/Advayta/investment packages.

## Install

```sh
pnpm add @global-torque/admin-html-patterns
```

## Usage

```ts
import { getAdminHtmlPattern } from '@global-torque/admin-html-patterns';

const tableContract = getAdminHtmlPattern('table');
```

## Pattern Coverage

The catalog covers alerts, badges, buttons, cards, empty states, progress bars,
status indicators, tables, tabs, toasts, and modals.

Every pattern records:

- required attributes;
- content regions;
- ARIA expectations;
- loading/error/empty states where relevant;
- dark-mode behavior;
- a Django template example.

## Django Ownership

Django templates own final server-side rendering, escaping, URLs, CSRF,
permissions, model-specific text, and form submission behavior. These contracts
are intended to make low-risk admin UI consistent without turning
`../i-djadmin-web` into a Vue SPA.

## Release Status

Prepare-next. Do not publish to npm until package-specific contracts,
attribution, admin consumer validation, and visual verification gates pass.
