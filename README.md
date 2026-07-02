# Opengis/DOCM

The **Document Generation Platform (DOCM)** lets you create, manage, and export documents based on templates and structured data.

## Functions

✅ Centralized template storage with browsing, editing, and versioning.
✅ Online editor for creating and updating templates with variables and preview support.
✅ Service that combines a template, data, and additional parameters to produce a ready document.
✅ Storage for all created documents with viewing, editing, and status management.
✅ JSON data, form input, or external ID (integration with business systems).
✅ Export to PDF, DOCX

## Install and Usage

### 1. Install the package

```bash
npm install @opengis/docm
```

### 2. Register interfaces

```ts
// router.config.ts
export default [
  {
    path: '/templates/:id?',
    component: () => import('@opengis/docm').then((m) => m.Template),
  },
  {
    path: '/documents/:id?',
    component: () => import('@opengis/docm').then((m) => m.Document),
  },
];
```

### 3. Register API

```ts
import Fastify from 'fastify';
import docmPlugin from '@opengis/docm/plugin.js';

const app = Fastify();
app.register(docmPlugin, { prefix: '/api' });
```

## Resources and Documentation

- [https://docm.opengis.info](https://docm.opengis.info)

## Contributions

We welcome contributions! Feel free to open issues, suggest features, or submit pull requests.

## License

MIT License
