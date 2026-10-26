# ks-carousel

## Overview

The `ks-carousel` component displays a collection of slides in a rotating gallery. It supports automatic playback, navigation controls, slide indicators, and manual navigation, making it suitable for showcasing images, banners, featured content, and promotional items.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `autoPlay` | Automatic slide transition interval in milliseconds. Set to `0` to disable autoplay. | `number` | `0` |
| `showControls` | Displays previous and next navigation controls. | `boolean` | `true` |
| `showDots` | Displays slide indicator dots. | `boolean` | `true` |
| `slides` | Collection of slides displayed in the carousel. | `KsCarouselSlide[]` | `[]` |

### KsCarouselSlide

```typescript
export interface KsCarouselSlide {
  key: string;
  imageUrl?: string;
  alt?: string;
  label?: string;
  caption?: string;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `slideChange` | Fired when the active slide changes. Returns the current slide index. | `number` |

# Usage

## React

```tsx
import { KsCarousel } from '@kraft.stitch/react';

function App() {
  const slides = [
    {
      imageUrl: '/assets/banner-1.jpg',
      label: 'Welcome',
      caption: 'Explore our platform'
    },
    {
      imageUrl: '/assets/banner-2.jpg',
      label: 'Features',
      caption: 'Discover powerful tools'
    }
  ];

  return (
    <KsCarousel
      slides={slides}
      autoPlay={5000}
      showControls={true}
      showDots={true}
    />
  );
}
```

## Angular

```typescript
import { KsCarouselComponent } from '@kraft.stitch/angular';
```

```html
<ks-carousel
  [slides]="slides"
  [autoPlay]="5000"
  [showControls]="true"
  [showDots]="true">
</ks-carousel>
```