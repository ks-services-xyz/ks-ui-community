# ks-message

## Overview

The `ks-message` component displays contextual feedback, alerts, notifications, and status messages. It supports visual variants, custom icons, dismissible behavior, and custom content through slots, making it suitable for communicating important information to users.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `dismissible` | Displays a dismiss button that allows users to close the message. | `boolean` | `false` |
| `icon` | Optional icon displayed alongside the message. | `string` | `''` |
| `text` | Main message text. | `string` | `''` |
| `variant` | Visual style variant. | `"brand" \| "danger" \| "info" \| "neutral" \| "success" \| "warning"` | `'info'` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `dismissed` | Fired when the message is dismissed. | `void` |

## Slots

| Slot | Description |
| ---- | ----------- |
| Default | Custom content displayed inside the message. |

# Usage

## React

```tsx
import { KsMessage } from '@kraft.stitch/react';

function App() {
  return (
    <KsMessage
      text="Profile updated successfully."
      variant="success"
      dismissible={true}
    />
  );
}
```

### Custom Content

```tsx
<KsMessage variant="warning">
  <strong>Warning:</strong> Changes have not been saved.
</KsMessage>
```

## Angular

```typescript
import { KsMessageComponent } from '@kraft.stitch/angular';
```

```html
<ks-message
  text="Profile updated successfully."
  variant="success"
  [dismissible]="true">
</ks-message>
```

### Custom Content

```html
<ks-message variant="warning">
  <strong>Warning:</strong>
  Changes have not been saved.
</ks-message>
```