# ks-sidebar

## Overview

The `ks-sidebar` component provides a slide-in navigation or content panel that can appear from the left or right side of the screen. It supports overlay and push behaviors, configurable widths, controlled visibility, custom header and footer content, and programmatic open/close operations.

In Angular, the component supports two-way binding through the `open` input and `ksOpenChange` output.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `open` | Controls whether the sidebar is visible. Supports Angular two-way binding. | `boolean` | `false` |
| `position` | Side from which the sidebar appears. | `"left" \| "right"` | `'left'` |
| `target` | Target element ID where the sidebar should be rendered. Leave empty to use the page. | `string` | `''` |
| `type` | Sidebar display behavior. | `"over" \| "push"` | `'over'` |
| `width` | Width of the sidebar panel. | `string` | `'18rem'` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksOpenChange` | Fired when the sidebar open state changes. | `boolean` |

## Methods

### openPanel()

Opens the sidebar.

```typescript
openPanel(): Promise<void>
```

### close()

Closes the sidebar.

```typescript
close(): Promise<void>
```

### toggle()

Toggles the sidebar open state.

```typescript
toggle(): Promise<void>
```

## Slots

| Slot | Description |
| ---- | ----------- |
| Default | Main sidebar content. |
| `header` | Custom sidebar header content. |
| `footer` | Custom sidebar footer content. |

# Usage

## React

```tsx
import { KsSidebar, KsButton } from '@kraft.stitch/react';

function App() {
  return (
    <KsSidebar
      open={true}
      position="left"
      width="20rem"
    >
      <div slot="header">
        Navigation
      </div>

      <div>
        Sidebar content goes here.
      </div>

      <div slot="footer">
        <KsButton name="Close" />
      </div>
    </KsSidebar>
  );
}
```

## Angular

```typescript
import { KsSidebarComponent } from '@kraft.stitch/angular';
```

```html
<ks-sidebar
  [(open)]="sidebarOpen"
  position="left"
  width="20rem">

  <div slot="header">
    Navigation
  </div>

  <div>
    Sidebar content goes here.
  </div>

  <div slot="footer">
    <ks-button name="Close"></ks-button>
  </div>

</ks-sidebar>
```