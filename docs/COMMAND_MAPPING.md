# Command Mapping: Raw → MCP

| **Raw Command**       | **MCP Action**       | **Example MCP Payload**                          |
|-----------------------|-----------------------|-------------------------------------------------|
| `forward 100 1`       | `move/forward`        | `{"power": 100, "duration": 1, "unit": "s"}` |
| `turn left 50 2`      | `move/turn`           | `{"direction": "left", "power": 50, "duration": 2}` |
| `play song.mp3`       | `audio/play`          | `{"file": "song.mp3", "volume": 80}`       |
| `HIGH` (touch)        | `sensor/touch`        | `{"state": "activated", "timestamp": "2025-11-07T12:00:00Z"}` |
| `speak "Hello"`      | `audio/speak`         | `{"text": "Hello", "language": "en"}`     |
| `listen`              | `audio/listen`        | `{"timeout": 5}`                              |
| `look forward`        | `vision/look`         | `{"direction": "forward"}`                   |
| `wake` (wakeword)     | `sensor/wakeword`     | `{"word": "Hey Sarahbot", "detected": true}` |

---
**Notes:**
- Add your custom commands here!
- MCP actions are JSON-serialized for compatibility.
