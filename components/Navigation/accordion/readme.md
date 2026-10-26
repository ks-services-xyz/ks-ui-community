# ks-accordion

## Overview

The `ks-accordion` component organizes content into expandable and collapsible sections, allowing users to reveal or hide information as needed. It supports single-panel and multi-panel expansion modes, programmatic control of open panels, and custom content for each accordion section.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `items` | Collection of accordion panel definitions. | `KsAccordionItem[]` | `[]` |
| `multi` | Allows multiple panels to be expanded simultaneously. | `boolean` | `false` |
| `openKeys` | Keys of panels that should be expanded initially. | `string[]` | `[]` |

### KsAccordionItem

```typescript
export interface KsAccordionItem {
  key: string;
  label: string;
  disabled?: boolean;
  icon?: string;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `toggled` | Fired when an accordion panel is expanded or collapsed. Returns the panel key. | `string` |

# Usage

## React

```tsx
import { KsAccordion } from '@kraft.stitch/react';

function App() {
  const items = [
    { key: 'profile', label: 'Profile' },
    { key: 'settings', label: 'Settings' }
  ];

  return (
    <KsAccordion
      items={items}
      openKeys={['profile']}
    >
      <div ksPanel="profile">
        Profile content goes here.
      </div>

      <div ksPanel="settings">
        Settings content goes here.
      </div>
    </KsAccordion>
  );
}
```

## Angular

```typescript
import { KsAccordionComponent } from '@kraft.stitch/angular';
```

```html
<ks-accordion
  [items]="items"
  [openKeys]="['profile']">

  <div ksPanel="profile">
    Profile content goes here.
  </div>

  <div ksPanel="settings">
    Settings content goes here.
  </div>

</ks-accordion>
```