# ks-badge

## Overview

The `ks-badge` component is used to display status indicators, labels, counts, and short pieces of contextual information. It supports multiple sizes, color variants, pill styling, and compact dot indicators for notifications and status displays.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `dot` | Displays a small status dot instead of text content. | `boolean` | `false` |
| `label` | Text displayed within the badge. | `string` | `''` |
| `pill` | Displays the badge with fully rounded corners. | `boolean` | `true` |
| `size` | Badge size. | `"sm" \| "md" \| "lg"` | `'md'` |
| `variant` | Visual color variant. | `"brand" \| "danger" \| "info" \| "neutral" \| "success" \| "warning"` | `'brand'` |

# Usage

## React

```tsx
import { KsBadge } from '@kraft.stitch/react';

function App() {
  return (
    <KsBadge
      label="New"
      variant="success"
    />
  );
}
```

### Dot Badge

```tsx
<KsBadge
  dot={true}
  variant="danger"
/>
```

## Angular

```typescript
import { KsBadgeComponent } from '@kraft.stitch/angular';
```

```html
<ks-badge
  label="New"
  variant="success">
</ks-badge>
```

### Dot Badge

```html
<ks-badge
  [dot]="true"
  variant="danger">
</ks-badge>
```