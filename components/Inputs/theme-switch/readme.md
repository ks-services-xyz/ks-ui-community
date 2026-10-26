# ks-theme-switch

## Overview

The `ks-theme-switch` component provides an interface for switching application themes and color palettes. It supports light mode, dark mode, system theme detection, and configurable color palettes, allowing users to personalize the appearance of the application.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `includePalette` | Displays the color palette selector. | `boolean` | `false` |
| `includeSystem` | Enables System mode alongside Light and Dark modes. | `boolean` | `true` |
| `mode` | Initial theme mode. | `ThemeMode.Light \| ThemeMode.Dark \| ThemeMode.System` | `ThemeMode.Light` |
| `onlyIcon` | Displays icons only without labels. | `boolean` | `false` |
| `palette` | Initial color palette. | `"Default" \| "ForestGreen" \| "BurntOrange" \| "VioletVelvet" \| "Black&White" \| "Beige&Brown"` | `'ForestGreen'` |

# Usage

## React

```tsx
import { KsThemeSwitch } from '@kraft.stitch/react';

function App() {
  return (
    <KsThemeSwitch
      includeSystem={true}
      includePalette={true}
      mode="light"
      palette="ForestGreen"
    />
  );
}
```

## Angular

```typescript
import { KsThemeSwitchComponent } from '@kraft.stitch/angular';
```

```html
<ks-theme-switch
  [includeSystem]="true"
  [includePalette]="true"
  mode="light"
  palette="ForestGreen">
</ks-theme-switch>
```