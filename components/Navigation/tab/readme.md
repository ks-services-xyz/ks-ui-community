# ks-tab

## Overview

The `ks-tab` component organizes content into multiple tabbed sections, allowing users to switch between related views without navigating away from the current page. It supports configurable tab styles, icons, disabled tabs, controlled active state management, and custom content for each tab panel.

In Angular, the component supports two-way binding through the `activeKey` input and `ksTabChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `activeKey` | Key of the currently active tab. Supports Angular two-way binding. | `string` | `''` |
| `tabHeaderStyle` | Visual style used for tab headers. | `"default" \| "button" \| "card" \| "expanded"` | `'default'` |
| `tabs` | Collection of tab definitions. | `KsTabItem[]` | `[]` |

### KsTabItem

```typescript
export interface KsTabItem {
  key: string;
  label: string;
  icon?: string;
  disabled?: boolean;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksTabChange` | Fired when the active tab changes. Returns the selected tab key. | `string` |

# Usage

## React

```tsx
import { KsTab } from '@kraft.stitch/react';

function App() {
  const tabs = [
    {
      key: 'profile',
      label: 'Profile'
    },
    {
      key: 'settings',
      label: 'Settings'
    }
  ];

  return (
    <KsTab
      tabs={tabs}
      activeKey="profile"
    >
      <div ksPanel="profile">
        Profile Content
      </div>

      <div ksPanel="settings">
        Settings Content
      </div>
    </KsTab>
  );
}
```

## Angular

```typescript
import { KsTabComponent } from '@kraft.stitch/angular';
```

```html
<ks-tab
  [tabs]="tabs"
  [(activeKey)]="activeKey">

  <div ksPanel="profile">
    Profile Content
  </div>

  <div ksPanel="settings">
    Settings Content
  </div>

</ks-tab>
```