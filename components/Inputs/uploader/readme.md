# ks-uploader

## Overview

The `ks-uploader` component provides a drag-and-drop file upload experience with support for file selection, file type validation, file size restrictions, image previews, and multiple file uploads. It helps users easily upload and manage files within an application.

## Properties

| Property | Description | Type | Default |
| -------- | ----------- | ---- | ------- |
| `accept` | Accepted file types or extensions (for example: `image/*,.pdf`). | `string` | `''` |
| `disabled` | Disables the uploader. | `boolean` | `false` |
| `label` | Custom label displayed inside the drop zone. | `string` | `'or Drop files here'` |
| `maxSize` | Maximum allowed file size in bytes. Set to `0` for no limit. | `number` | `0` |
| `multiple` | Allows selecting multiple files. | `boolean` | `false` |
| `previewImages` | Displays thumbnail previews for image files. | `boolean` | `true` |

### KsUploadedFile

```typescript
export interface KsUploadedFile {
  file: File;
  preview?: string;
}
```

## Events

| Event | Description | Type |
| ------- | ----------- | ---- |
| `ksFilesChange` | Fired when accepted files are selected or dropped. | `KsUploadedFile[]` |
| `ksFilesRejected` | Fired when files are rejected because of file type or size restrictions. | `File[]` |

# Usage

## React

```tsx
import { KsUploader } from '@kraft.stitch/react';

function App() {
  return (
    <KsUploader
      accept="image/*,.pdf"
      multiple={true}
      maxSize={5 * 1024 * 1024}
      previewImages={true}
    />
  );
}
```

## Angular

```typescript
import { KsUploaderComponent } from '@kraft.stitch/angular';
```

```html
<ks-uploader
  accept="image/*,.pdf"
  [multiple]="true"
  [maxSize]="5242880"
  [previewImages]="true">
</ks-uploader>
```