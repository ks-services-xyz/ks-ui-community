# ks-avatar

## Overview

The `ks-avatar` component displays a user's profile image, initials, or icon representation. It supports multiple sizes, shape variations, visual variants, and fallback display options when an image is unavailable.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `alt` | Alternative text for the avatar image. | `string` | `''` |
| `icon` | Icon displayed when neither `src` nor `initials` is provided. | `string` | `''` |
| `initials` | Initials displayed when no image is available. | `string` | `''` |
| `size` | Avatar size. | `"sm" \| "md" \| "lg" \| "xl"` | `'md'` |
| `square` | Displays a rounded-square avatar instead of the default circular avatar. | `boolean` | `false` |
| `src` | Avatar image URL. Takes priority over initials and icon. | `string` | `''` |
| `variant` | Visual variant used when displaying initials or an icon. | `"brand" \| "danger" \| "info" \| "neutral" \| "success" \| "warning"` | `'brand'` |

# Usage

## React

```tsx
import { KsAvatar } from '@kraft.stitch/react';

function App() {
  return (
    <KsAvatar
      src="/assets/avatar.png"
      alt="John Doe"
      size="lg"
    />
  );
}
```

### Initials Avatar

```tsx
<KsAvatar
  initials="JD"
  size="lg"
  variant="brand"
/>
```

## Angular

```typescript
import { KsAvatarComponent } from '@kraft.stitch/angular';
```

```html
<ks-avatar
  src="/assets/avatar.png"
  alt="John Doe"
  size="lg">
</ks-avatar>
```

### Initials Avatar

```html
<ks-avatar
  initials="JD"
  size="lg"
  variant="brand">
</ks-avatar>
```