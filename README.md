# LUNARA AI — Railway Ready

This project serves the LUNARA frontend and a secure server-side OpenAI API endpoint.

## 1. GitHub
Upload these files to the root of your GitHub repository:
- `index.html`
- `server.js`
- `package.json`
- `.gitignore`
- `.env.example`
- `README.md`

Do **not** upload `.env` or a real OpenAI API key.

## 2. Railway
Create a new Railway service from the GitHub repository.

Railway will run:
```bash
npm start
```

No custom port is required; the server uses Railway's `PORT` variable.

## 3. Railway Variables
In Railway → Variables, add:

```text
OPENAI_API_KEY=your_real_openai_api_key
OPENAI_MODEL=gpt-5.6-luna
```

Redeploy after saving variables.

## 4. Test
Open:
```text
https://YOUR-RAILWAY-DOMAIN/health
```

You should see JSON with `ok: true` and `apiConfigured: true`.

Then open the main site and send a chat message.
