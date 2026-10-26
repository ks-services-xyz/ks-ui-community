# ks-button

## Overview

The `ks-button` component is a reusable button used to trigger actions within an application. It supports multiple visual variants, sizes, icons, rounded styling, disabled state handling, and click events to provide a consistent user experience across the design system.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `disabled` | Disables the button. | `boolean` | `false` |
| `icon` | Icon class string (e.g. Material Icon or Font Awesome class). | `string` | `''` |
| `isRounded` | Renders the button with fully rounded pill corners. | `boolean` | `false` |
| `name` | Button label text. | `string` | `''` |
| `size` | Button size. | `"lg" \| "md" \| "sm"` | `'md'` |
| `variant` | Visual style variant. | `"brand" \| "brand-outlined" \| "brand-solid" \| "danger" \| "danger-outlined" \| "danger-solid" \| "disabled" \| "info" \| "info-outlined" \| "info-solid" \| "neutral" \| "neutral-outlined" \| "neutral-solid" \| "success" \| "success-outlined" \| "success-solid" \| "warning" \| "warning-outlined" \| "warning-solid"` | `'brand'` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `clicked` | Fired when the button is clicked. | `MouseEvent` |

# Usage

## React

```tsx
import { KsButton } from '@kraft.stitch/react';

function App() {
  return (
    <KsButton
      name="Success"
      variant="success"
      size="sm"
      icon="ks-icon-pencil"
    />
  );
}
```

## Angular

```ts
import { KsButtonComponent } from '@kraft.stitch/angular';
```

```html
<ks-button
  name="Success"
  variant="success"
  size="sm"
  icon="ks-icon-pencil">
</ks-button>
```