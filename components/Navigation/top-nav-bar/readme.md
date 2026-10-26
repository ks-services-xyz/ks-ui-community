# ks-top-nav-bar

## Overview

The `ks-top-nav-bar` component provides a horizontal navigation bar for displaying primary application navigation links. It supports icons, labels, active navigation indicators, and customizable visual styles, making it ideal for dashboards, websites, and application headers.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `items` | Collection of navigation items. | `KsTopNavBarItem[]` | `[]` |
| `label` | Accessible label for the navigation element. | `string` | `'Top navigation'` |
| `showIcons` | Displays icons alongside navigation labels. | `boolean` | `true` |
| `showLabels` | Displays navigation label text. | `boolean` | `true` |
| `variant` | Style of the active navigation indicator. | `"default" \| "pill" \| "underline"` | `'default'` |

### KsTopNavBarItem

```typescript
export interface KsTopNavBarItem {
  key: string;
  name: string;
  iconClass?: string;
  redirectLink: string;
  activationFragment?: string;
  disabled?: boolean;
}
```

## Slots

| Slot | Description |
| ---- | ----------- |
| Default | Additional custom content displayed within the navigation bar. |

# Usage

## React

```tsx
import { KsTopNavBar } from '@kraft.stitch/react';

function App() {
  const items = [
    {
      key: 'home',
      name: 'Home',
      iconClass: 'ks-icon-home',
      redirectLink: '/'
    },
    {
      key: 'products',
      name: 'Products',
      iconClass: 'ks-icon-box',
      redirectLink: '/products'
    },
    {
      key: 'settings',
      name: 'Settings',
      iconClass: 'ks-icon-settings',
      redirectLink: '/settings'
    }
  ];

  return (
    <KsTopNavBar
      items={items}
      variant="underline"
      showIcons={true}
      showLabels={true}
    />
  );
}
```

## Angular

```typescript
import { KsTopNavBarComponent } from '@kraft.stitch/angular';
```

```html
<ks-top-nav-bar
  [items]="items"
  variant="underline"
  [showIcons]="true"
  [showLabels]="true">
</ks-top-nav-bar>
```