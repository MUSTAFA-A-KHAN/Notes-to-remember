# HTMX Attribute `hx-request` to Disable Headers

When working with HTMX and encountering issues related to CORS (Cross-Origin Resource Sharing), such as fetching JSON data from GitHub's raw content, you may encounter errors due to the browser's CORS policy.

To resolve this issue, you can utilize the `hx-request` attribute in HTMX, specifically by setting `noHeaders` to `true`. This attribute allows you to disable headers, thus bypassing CORS restrictions without the need to clear headers in the callback function.

Here's how you can implement it:

```html
<button hx-get="/data.json" hx-request='{"noHeaders": true}'>Fetch Data</button>
```

With this setup, HTMX will make the request without sending any additional headers, thereby avoiding CORS-related errors.

Remember to refer to this note whenever you encounter similar CORS issues in the future while working with HTMX.
