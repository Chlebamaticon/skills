# File Upload

**Level:** Unclassified  
**Category:** Form

An input control for selecting and uploading files from the user's device.

## When to use
- Uploading documents, images, or media in forms
- Importing data files like CSVs or spreadsheets
- Attaching files to messages or tickets
- Profile photo or avatar uploads
- Bulk file upload in content management systems

## When to avoid
- For simple text or numeric input — use Input instead
- When files should be captured live — use a camera input
- If only a URL is needed — use a text input for the link
- For very large files without chunked upload support
- When the upload destination isn't clear to the user

## States
- **Default** — Ready to accept files — shows drop zone and browse button.
- **Drag Over** — A file is being dragged over the drop zone — visual highlight.
- **Uploading** — File is being uploaded — shows progress bar.
- **Complete** — Upload finished successfully — file appears in the list.
- **Error** — Upload failed — shows error message with retry option.
- **Disabled** — Upload is not available.

## Related
[Input](input.md), [Progress](progress.md), [Button](button.md)

Source: [UX Components](https://www.ux-components.com/components/file-upload)
