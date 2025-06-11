# Authentication Guide

This guide provides detailed instructions for obtaining and configuring API keys and credentials for all services used in the AI YouTube channel project.

## Make.com

### API Key
1. Log in to your Make.com account
2. Go to https://www.make.com/en/account/api-keys
3. Click "Create a new API key"
4. Give it a descriptive name (e.g., "AI YouTube Channel")
5. Copy the generated API key
6. Add to `.env` as `MAKE_COM_API_KEY`

### Webhook URL
1. In your Make.com scenario
2. Add a "Webhook" module
3. Configure the webhook settings
4. Copy the generated webhook URL
5. Add to `.env` as `MAKE_COM_WEBHOOK_URL`

## Airtable

### Personal Access Token
1. Go to https://airtable.com/create/tokens
2. Click "Create a new token"
3. Give it a name (e.g., "AI YouTube Channel")
4. Set appropriate scopes:
   - `data.records:read`
   - `data.records:write`
   - `schema.bases:read`
5. Copy the generated token
6. Add to `.env` as `AIRTABLE_API_KEY`

### Base ID
1. Open your Airtable base
2. Go to Help > API Documentation
3. Find the "Base ID" in the API documentation
4. Add to `.env` as `AIRTABLE_BASE_ID`

## RSS.app

### API Key
1. Log in to your RSS.app account
2. Go to https://rss.app/account/api
3. Click "Generate New API Key"
4. Give it a name (e.g., "AI YouTube Channel")
5. Copy the generated API key
6. Add to `.env` as `RSS_APP_API_KEY`

## Google Gemini

### API Key
1. Go to https://makersuite.google.com/app/apikey
2. Click "Create API Key"
3. Give it a name (e.g., "AI YouTube Channel")
4. Copy the generated API key
5. Add to `.env` as `GEMINI_API_KEY`

## YouTube

### API Key
1. Go to Google Cloud Console
2. Create a new project or select existing
3. Enable YouTube Data API v3
4. Go to Credentials
5. Create API Key
6. Restrict the key to YouTube Data API
7. Add to `.env` as `YOUTUBE_API_KEY`

### OAuth 2.0 Credentials
1. In Google Cloud Console
2. Go to Credentials
3. Create OAuth 2.0 Client ID
4. Set application type as "Web application"
5. Add authorized redirect URIs
6. Download the client credentials
7. Add to `.env`:
   - `YOUTUBE_CLIENT_ID`
   - `YOUTUBE_CLIENT_SECRET`
   - `YOUTUBE_REFRESH_TOKEN`

## D-ID

### API Key
1. Go to https://cloud.d-id.com/
2. Sign up or log in
3. Go to API Keys section
4. Create new API key
5. Copy the generated key
6. Add to `.env` as `DID_API_KEY`

## Creatomate

### API Key
1. Log in to Creatomate
2. Go to Account > API Keys
3. Create new API key
4. Copy the generated key
5. Add to `.env` as `CREATOMATE_API_KEY`

## Buffer

### API Key
1. Log in to Buffer
2. Go to https://buffer.com/developers/api
3. Create new application
4. Get API key
5. Add to `.env` as `BUFFER_API_KEY`

## AWS (for Storage)

### Access Keys
1. Log in to AWS Console
2. Go to IAM
3. Create new IAM user
4. Attach appropriate policies (S3 access)
5. Create access key
6. Add to `.env`:
   - `AWS_ACCESS_KEY_ID`
   - `AWS_SECRET_ACCESS_KEY`
   - `AWS_BUCKET_NAME`
   - `AWS_REGION`

## Security Best Practices

1. **Never commit `.env` files** to version control
2. Use strong, unique passwords for each service
3. Regularly rotate API keys
4. Use the principle of least privilege
5. Enable 2FA where available
6. Monitor API usage and set up alerts
7. Keep documentation of key rotation dates

## Key Rotation Schedule

| Service | Rotation Period | Last Rotated |
|---------|----------------|--------------|
| Make.com | 90 days | - |
| Airtable | 90 days | - |
| RSS.app | 90 days | - |
| Gemini | 90 days | - |
| YouTube | 90 days | - |
| D-ID | 90 days | - |
| Creatomate | 90 days | - |
| Buffer | 90 days | - |
| AWS | 90 days | - |

## Troubleshooting

### Common Issues

1. **API Key Not Working**
   - Verify the key is correctly copied
   - Check if the key has expired
   - Verify the key has correct permissions

2. **Rate Limiting**
   - Check service status pages
   - Implement exponential backoff
   - Consider upgrading plan if needed

3. **Authentication Errors**
   - Verify credentials are correct
   - Check if service is down
   - Verify IP restrictions

### Support Resources

- Make.com: https://www.make.com/en/help
- Airtable: https://airtable.com/support
- RSS.app: https://rss.app/support
- Google Cloud: https://cloud.google.com/support
- D-ID: https://cloud.d-id.com/docs
- Creatomate: https://creatomate.com/docs
- Buffer: https://buffer.com/developers/api
- AWS: https://aws.amazon.com/support 