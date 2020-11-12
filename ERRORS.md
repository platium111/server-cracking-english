12/11/2020

- need to have server, React cannot make request that API requires CORS
  -> can't make simple function in Lambda, using serverless to wrap it, so we can write express app with ES6, it will transpile to which we have in Lambda (Lambda now is supporting nodejs12.x)
- serverless run local
  `serverless invoke local --function app`

- run localhost:3000
  `serverless offline` -> will run default function `app` we have in .yml file -> based on `path: /lookup` will run `http://localhost:3000/dev/lookup` in browser

- up to AWS Lambda using
  `serverless deploy`
- configure using `serverless.yml` such as runtime, functions

- [e_cannot_GET_NULL] to run serverless offline in local
  need to have route for it in `app.get("/lookup", async (req, res) => {`
  -> cannot put `/` here, need `lookup`.
  [ref] https://github.com/dougmoscrop/serverless-http/issues/86#issuecomment-627514571
