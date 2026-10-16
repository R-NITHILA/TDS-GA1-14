# Live MCP Challenge Server

Requires Node.js 20 or newer.

## Run locally

```bash
npm install
npm start
```

Local endpoint: `http://localhost:3000/mcp`

## Deploy on Render

1. Push these files to a GitHub repository.
2. In Render, select **New + → Blueprint** and connect the repository.
3. Render reads `render.yaml` and deploys the web service.
4. Submit `https://YOUR-SERVICE.onrender.com/mcp` as the MCP endpoint.

Keep the service available through the grading window. Check your hosting plan's sleep behavior.

The server exposes exactly one tool, `solve_challenge`, with no required input properties. For every POST request it reads `X-Exam-Challenge` from that request's HTTP headers and returns the first 16 lowercase hex characters of SHA-256 over `challenge:24f3001488@ds.study.iitm.ac.in`. Signature verification is omitted because it is optional.
