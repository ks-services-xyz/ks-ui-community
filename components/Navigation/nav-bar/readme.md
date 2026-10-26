# ks-nav-bar

## Overview

The `ks-nav-bar` component provides a flexible navigation sidebar for organizing application navigation links. It supports icon-only navigation, hover-to-expand behavior, and permanently expanded layouts, making it suitable for dashboards, admin portals, and enterprise applications.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `expandedWidth` | Width of the expanded navigation panel. | `string` | `'13rem'` |
| `iconWidth` | Width of the icon-only navigation rail. | `string` | `'3.5rem'` |
| `items` | Collection of navigation items. | `KsNavBarItem[]` | `[]` |
| `mode` | Navigation display mode. | `"iconOnly" \| "hoverToExpand" \| "alwaysOpen"` | `'iconOnly'` |

### KsNavBarItem

```typescript
export interface KsNavBarItem {
  key: string;
  name: string;
  iconClass: string;
  redirectLink: string;
  activationFragment?: string;
  disabled?: boolean;
}
```

# Usage

## React

```tsx
import { KsNavBar } from '@kraft.stitch/react';

function App() {
  const items = [
    {
      key: 'dashboard',
      name: 'Dashboard',
      iconClass: 'ks-icon-dashboard',
      redirectLink: '/dashboard'
    },
    {
      key: 'users',
      name: 'Users',
      iconClass: 'ks-icon-user',
      redirectLink: '/users'
    }
  ];

  return (
    <KsNavBar
      items={items}
      mode="hoverToExpand"
      expandedWidth="14rem"
    />
  );
}
```

## Angular

```typescript
import { KsNavBarComponent } from '@kraft.stitch/angular';
```

```html
<ks-nav-bar
  [items]="items"
  mode="hoverToExpand"
  expandedWidth="14rem">
</ks-nav-bar>
```