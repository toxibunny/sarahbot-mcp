# MCP Specification for Sarahbot

## Message Format
All MCP messages are JSON objects with the following structure:

```json
{
  "header": {
    "protocol": "MCP/1.0",
    "message_type": "command|event|response",
    "timestamp": "ISO_8601"
  },
  "body": {
    "action": "move/forward|audio/play|...",
    "params": {}
  }
}
```

## Example Messages

### 1. Move Forward
```json
{
  "header": {
    "protocol": "MCP/1.0",
    "message_type": "command",
    "timestamp": "2025-11-07T12:00:00Z"
  },
  "body": {
    "action": "move/forward",
    "params": {"power": 100, "duration": 1}
  }
}
```

### 2. Play Audio
```json
{
  "header": {
    "protocol": "MCP/1.0",
    "message_type": "command",
    "timestamp": "2025-11-07T12:00:00Z"
  },
  "body": {
    "action": "audio/play",
    "params": {"file": "never_gonna.mp3", "volume": 80}
  }
}
```

### 3. Touch Sensor Event
```json
{
  "header": {
    "protocol": "MCP/1.0",
    "message_type": "event",
    "timestamp": "2025-11-07T12:00:00Z"
  },
  "body": {
    "action": "sensor/touch",
    "params": {"state": "activated"}
  }
}
```

---
**Extending MCP:**
- Add new `action` types as needed.
- Use `message_type` to distinguish commands, events, and responses.
