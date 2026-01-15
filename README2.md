# Install and run the Effect demo

> source [mikearnaldi lambda-conf-2024](https://github.com/mikearnaldi/lambda-conf-2024)

> presented in [lambda-conf-2024 talk](https://www.youtube.com/watch?v=BHuY6w9ed5o)

## Installation

### `pnpm`

- install pnpm: `curl -fsSL https://get.pnpm.io/install.sh | sh -`

lambda-conf-2024 % which pnpm
/Users/rudifarkas/Library/pnpm/pnpm

- `pnpm install`

- `pnpm approve-builds`; approve all postinstall scripts to run

### demo project

- `pnpm run start:server` # in terminal 1
- `pnpm run start:client` # in terminal 2

Output:

```
lambda-conf-2024 % pnpm run start:client

> lambda-conf-2024@1.0.0 start:client /Users/rudifarkas/GitHub/js/js-2026/lambda-conf-2024
> tsx src/api-client.ts

timestamp=2026-01-09T19:42:50.995Z level=DEBUG fiber=#0 message="found 2 notes"
timestamp=2026-01-09T19:42:50.996Z level=INFO fiber=#0 message="Hey LambdaConf!!!"
timestamp=2026-01-09T19:42:50.996Z level=INFO fiber=#0 message="Look at that!!!"
lambda-conf-2024 % pnpm run start:client                                                              [dev-pnpm L|✚1…3]

> lambda-conf-2024@1.0.0 start:client /Users/rudifarkas/GitHub/js/js-2026/lambda-conf-2024
> tsx src/api-client.ts

timestamp=2026-01-09T19:42:55.475Z level=ERROR fiber=#0 cause="ClientError: could not create note
...

```

The `ClientError` is intended, to demonstrate error reporting.

This error occurs because the demo app's database accepts only unique message items.

## Possible improvements

- a more user friendly error log
- add a timestamp to the message (note)
- add console argument for a new note
- permanent storage of the database
