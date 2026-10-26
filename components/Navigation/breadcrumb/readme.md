# ks-breadcrumb

## Overview

The `ks-breadcrumb` component displays the user's current location within an application's navigation hierarchy. It helps users understand their context and quickly navigate back to previous sections using a series of hierarchical links.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `items` | Collection of breadcrumb items displayed in order. | `KsBreadcrumbItem[]` | `[]` |
| `separator` | Character or symbol displayed between breadcrumb items. | `string` | `'/'` |
| `size` | Breadcrumb size. | `"sm" \| "md" \| "lg"` | `'lg'` |

### KsBreadcrumbItem

```typescript
export interface KsBreadcrumbItem {
  label: string;
  href?: string;
  icon?: string;
}
```

# Usage

## React

```tsx
import { KsBreadcrumb } from '@kraft.stitch/react';

function App() {
  const items = [
    { label: 'Home', href: '/' },
    { label: 'Products', href: '/products' },
    { label: 'Details' }
  ];

  return (
    <KsBreadcrumb
      items={items}
      separator="/"
      size="lg"
    />
  );
}
```

## Angular

```typescript
import { KsBreadcrumbComponent } from '@kraft.stitch/angular';
```

```html
<ks-breadcrumb
  [items]="items"
  separator="/"
  size="lg">
</ks-breadcrumb>
```