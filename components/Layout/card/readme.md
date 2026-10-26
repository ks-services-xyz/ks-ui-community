# ks-card

## Overview

The `ks-card` component is a flexible container used to group and display related content. It supports titles, subtitles, images, icons, custom header and footer content, clickable interactions, and multiple visual styles to help organize information in a clean and consistent layout.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `cardTitle` | Card title text. | `string` | `''` |
| `clickable` | Makes the card interactive and emits a click event. | `boolean` | `false` |
| `iconClass` | Icon class displayed in the card header. | `string` | `''` |
| `imageAlt` | Alternative text for the card image. | `string` | `''` |
| `imageUrl` | URL of the card header image. | `string` | `''` |
| `label` | Primary card heading. | `string` | `''` |
| `subtitle` | Secondary card heading. | `string` | `''` |
| `variant` | Visual card style. | `"default" \| "elevated" \| "flat" \| "outlined"` | `'default'` |

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `cardClick` | Fired when the card is clicked. | `MouseEvent` |

## Slots

| Slot | Description |
| ---- | ----------- |
| Default | Main card content. |
| `header` | Custom card header content. |
| `footer` | Custom card footer content. |

# Usage

## React

```tsx
import { KsCard } from '@kraft.stitch/react';

function App() {
  return (
    <KsCard
      label="Project Overview"
      subtitle="Q4 Progress"
      variant="elevated"
    >
      <p>Project delivery is on track and progressing as planned.</p>
    </KsCard>
  );
}
```

### With Header and Footer

```tsx
<KsCard
  label="Project Overview"
  variant="outlined"
>
  <div slot="header">
    Custom Header
  </div>

  <p>Card content goes here.</p>

  <div slot="footer">
    Custom Footer
  </div>
</KsCard>
```

## Angular

```typescript
import { KsCardComponent } from '@kraft.stitch/angular';
```

```html
<ks-card
  label="Project Overview"
  subtitle="Q4 Progress"
  variant="elevated">
  <p>Project delivery is on track and progressing as planned.</p>
</ks-card>
```

### With Header and Footer

```html
<ks-card
  label="Project Overview"
  variant="outlined">

  <div slot="header">
    Custom Header
  </div>

  <p>Card content goes here.</p>

  <div slot="footer">
    Custom Footer
  </div>

</ks-card>
```