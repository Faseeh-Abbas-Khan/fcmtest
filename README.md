# Firebase Notification Server

Simple Node.js server for sending Firebase Cloud Messages (FCM) to mobile devices.

## Quick Start

1. **Install dependencies**
   ```
   npm install
   ```

2. **Add Firebase credentials**
   - Download `serviceAccountKey.json` from Firebase Console > Project Settings > Service Accounts
   - Place in project root

3. **Start server**
   ```
   npm run dev
   ```

## API Usage

**Send notification**
```
POST /send-notification
{
  "topic": "general",
  "title": "Hello",
  "body": "This is a test notification",
  "data": { "key": "value" }
}
```

## Test with curl
```
curl -X POST http://localhost:3000/send-notification \
  -H "Content-Type: application/json" \
  -d '{"topic":"general","title":"Test","body":"Message"}'
```
