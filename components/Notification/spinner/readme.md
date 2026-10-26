# ks-spinner

## Overview

The `ks-spinner` component provides a visual loading indicator for asynchronous operations and background processes. It supports multiple sizes, color variants, optional descriptive text, and automatic centering within its container.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `centered` | Centers the spinner within its container. | `boolean` | `false` |
| `size` | Spinner size. | `"sm" \| "md" \| "lg" \| "xl"` | `'md'` |
| `text` | Optional text displayed alongside the spinner. | `string` | `''` |
| `variant` | Visual style variant. | `"brand" \| "danger" \| "info" \| "neutral" \| "success" \| "warning"` | `'brand'` |

# Usage

## React

```tsx
import { KsSpinner } from '@kraft.stitch/react';

function App() {
  return (
    <KsSpinner
      size="lg"
      text="Loading..."
      variant="brand"
    />
  );
}
```

### Centered Spinner

```tsx
<KsSpinner
  centered={true}
  size="xl"
  text="Please wait..."
/>
```

## Angular

```typescript
import { KsSpinnerComponent } from '@kraft.stitch/angular';
```

```html
<ks-spinner
  size="lg"
  text="Loading..."
  variant="brand">
</ks-spinner>
```

### Centered Spinner

```html
<ks-spinner
  [centered]="true"
  size="xl"
  text="Please wait...">
</ks-spinner>
```