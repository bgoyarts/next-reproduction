## Readme
Steps to reproduce the issue:
1. Install all dependencies `yarn install`
2. Run the next site by going into my-app and running `yarn dev`
3. Result: dependencies from the monorepo are being inlined in the output `my-app/.next/server/pages/index.js`.
   The expected result is to have the dependencies externalized.

To see the correct output, change the `next` dependency in `my-app/package.json` to `10.0.5`. And follow the above steps.
The result is that the dependencies are externalized in `my-app/.next/server/pages/index.js`