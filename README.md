# AnythingLLM Dokploy Deployment

🚀 **Private ChatGPT with persistent storage** - Deployment configuration for Dokploy.

## Features

- ✅ **Persistent Storage**: All data stored in Docker volume `anythingllm-storage`
- ✅ **Authentication Disabled**: Direct access without login screen
- ✅ **API Tokens**: Pre-configured for API access
- ✅ **Auto-restart**: Container restarts automatically on failure
- ✅ **Health Checks**: Built-in health monitoring

## Deployment URL

https://anything-llm.qub3.uk

## Configuration

### Environment Variables

- `DISABLE_AUTH=true` - Disables login screen
- `STORAGE_DIR=/app/server/storage` - Storage directory
- `SERVER_PORT=3001` - Application port
- `AUTH_TOKEN` - API authentication token
- `JWT_SECRET` - JWT secret for API

### Persistent Storage

All application data (documents, conversations, settings) is stored in:
```
Volume: anythingllm-storage
Mount: /app/server/storage
```

## Quick Deploy in Dokploy

1. Create new **Compose** service
2. Connect to GitHub repository: `asmaamohamed0264/anythingllm-dokploy`
3. Branch: `main`
4. Deploy!

## Manual Docker Compose Deploy

```bash
docker-compose up -d
```

## Access

After deployment, access the application at:
- **Local**: http://localhost:3001
- **Production**: https://anything-llm.qub3.uk

## Stack

- **Image**: `mintplexlabs/anythingllm:latest`
- **Port**: 3001
- **Storage**: Docker volume (persistent)
- **Restart Policy**: unless-stopped

## Support

- [AnythingLLM Documentation](https://docs.anythingllm.com/)
- [GitHub Repository](https://github.com/Mintplex-Labs/anything-llm)
