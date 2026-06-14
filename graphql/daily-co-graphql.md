# Daily.co GraphQL Schema

Conceptual GraphQL schema for the [Daily REST API](https://docs.daily.co/reference/rest-api), covering the full surface area of Daily's WebRTC video and audio infrastructure platform.

## Source

- REST API reference: https://docs.daily.co/reference/rest-api
- GitHub: https://github.com/daily-co
- Schema file: [daily-co-schema.graphql](daily-co-schema.graphql)

## Coverage

The schema translates Daily's REST resources into GraphQL types, queries, mutations, and subscriptions. It covers:

**Rooms**
- `Room`, `RoomDetails`, `RoomConfig`, `RoomPrivacy` — room lifecycle and configuration
- `DomainAccess` — domain-level access control applied to rooms
- `RoomToken`, `TokenProperties` — meeting tokens and their JWT claims

**Meetings and Participants**
- `Meeting`, `MeetingDetails`, `MeetingToken` — session management
- `Participant`, `ParticipantDetails`, `ParticipantStatus` — participant lifecycle
- `ParticipantVideo`, `ParticipantAudio`, `ParticipantScreenShare` — per-track media state

**Recordings**
- `Recording`, `RecordingDetails`, `RecordingStatus`, `RecordingType` — cloud and local recordings
- `RecordingLayout`, `RecordingS3Config` — layout presets and S3 storage configuration

**Transcripts**
- `Transcript`, `TranscriptDetails`, `TranscriptSegment`, `TranscriptWord` — word-level transcript data

**Live Streaming**
- `LiveStream`, `LiveStreamDetails`, `LiveStreamConfig` — stream session management
- `Broadcast`, `BroadcastDetails`, `CompositeStream` — output destinations
- `RTMP`, `StreamComposition`, `StreamLayout` — compositing and RTMP push

**SIP / Dial-In**
- `SIPConfig`, `SIPEndpoint`, `SIPCall` — SIP trunk configuration and call state
- `DialInNumber` — PSTN dial-in numbers for rooms

**Media Utilities**
- `Codec`, `Resolution`, `Bandwidth` — media constraint enums and types

**Metrics**
- `MeetingMetrics`, `ParticipantMetrics`, `NetworkMetrics` — quality and engagement data

**Messaging and State**
- `AppMessage` — in-meeting data messages between participants
- `ClientState` — snapshot of a participant's local media state

**Webhooks and Events**
- `Webhook`, `WebhookEvent`, `MeetingEvent`, `WebhookEventType` — event subscriptions and delivery

**Auth**
- `APIKey`, `Token` — domain API keys and short-lived session tokens

## Type Count

The schema defines 55+ named types across enums, object types, and input types.

## Operations

### Queries
Room lookup and listing, meeting session lookup, recordings, transcripts, live streams, SIP configuration, dial-in numbers, webhooks, meeting metrics, API key listing, and domain access retrieval.

### Mutations
Room create/update/delete, meeting token creation, recording start/stop/delete, live stream start/stop, SIP dial-out and hangup, SIP config management, webhook create/update/delete, in-meeting app messages, participant ejection, and API key management.

### Subscriptions
Real-time meeting events, participant state changes, app messages, recording status, live stream status, and webhook delivery events.
