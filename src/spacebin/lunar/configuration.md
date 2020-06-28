# Configuration
As of yet, there are only two values you can configure via `$HOME/.lunar.yaml`:

## `instance`
This is the API instance that you're uploading your documents to. The default is `https://api.spaceb.in`.

## `result-url`
This is the base of the final URL that is output, defaulting to `https://spaceb.in/`. Currently the default URL
does not actually resolve to your document (as the frontend for Spacebin has not been finished), so I recommend
switching it to `https://api.spaceb.in/api/v1/document/` and using the `-r` flag until the frontend is finished.