# ks-not-found

## Overview

The `ks-not-found` component provides a customizable error page for handling missing or unavailable routes. It can display custom messages, descriptions, automatic redirection, navigation actions, and additional content to help users recover from navigation errors.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `buttonLabel` | Text displayed on the navigation button. | `string` | `'Go to Home'` |
| `code` | Error code displayed prominently on the page. | `string` | `'404'` |
| `countdown` | Number of seconds before automatic redirection occurs. Set to `0` to disable auto-redirect. | `number` | `30` |
| `description` | Detailed description displayed below the heading. | `string` | `"The page you're looking for doesn't exist or has been moved."` |
| `homeHref` | Destination URL used by the action button and automatic redirect. | `string` | `'./'` |
| `message` | Main message displayed below the error code. | `string` | `'Page not found'` |
| `showActionButtons` | Controls whether action buttons are displayed. | `boolean` | `true` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `redirecting` | Fired immediately before automatic redirection occurs. | `void` |

## Slots

| Slot | Description |
| ---- | ----------- |
| Default | Additional custom content displayed within the page. |

# Usage

## React

```tsx
import { KsNotFound } from '@kraft.stitch/react';

function App() {
  return (
    <KsNotFound
      code="404"
      message="Page not found"
      description="The page you are looking for does not exist."
      homeHref="/"
      countdown={10}
    />
  );
}
```

## Angular

```typescript
import { KsNotFoundComponent } from '@kraft.stitch/angular';
```

```html
<ks-not-found
  code="404"
  message="Page not found"
  description="The page you are looking for does not exist."
  homeHref="/"
  [countdown]="10">
</ks-not-found>
```