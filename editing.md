# Editing

> All the photo, video editing tricks are for macOS.

## Image

### Edit

Use tools:

- Preview
- PPT
- Excalidraw
- emoji
- Photoshop

### Edit metadata

**Use case**:
Bob edits a photo (taken on an iPhone) using AI, photoshop, PPT, ... The edited image becomes a **new file**, so it loses the original iPhone metadata (device info, camera details, location, etc.). Bob wants to send the **edited photo while preserving the original iPhone metadata.**

**Approach**:
Use the original image (with metadata) as the base and overlay the edited image content on top of it in Preview. This way, the visual content changes, but the metadata remains intact.

**Steps**:

1. Open the **edited photo** (overlay image) in Preview.
2. Select the entire image:
   - Edit → Select All (⌘A)
   - Edit → Copy (⌘C)
3. Open the **original iPhone photo** (base image with metadata) in Preview.
4. Remove the existing image content:
   - Edit → Cut (⌘X)
5. Paste the edited image, then resize and position as needed.
6. Save the file.

## Video
