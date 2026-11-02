# Incident Data Format

This document defines the shared incident data schema used across the Reporter and Dispatcher modules.

## Incident Schema

| Field | Type | Description |
| :--- | :--- | :--- |
| `id` | `string` | Unique identifier for the incident report. |
| `lat` | `number` | Latitude coordinate of the incident location. |
| `lng` | `number` | Longitude coordinate of the incident location. |
| `timestamp` | `string` / `number` | Timestamp when the incident occurred or was reported (e.g., ISO 8601 string or epoch milliseconds). |
| `photo_url` | `string` | URL or file path pointing to the captured photo of the incident scene. |
| `ai_summary` | `string` | AI-generated assessment summarizing the accident scene, severity, and potential casualties. |
| `status` | `string` | Current handling status of the incident (e.g., `reported`, `dispatching`, `resolved`). |
| `hospital_suggestion` | `string` / `object` | Suggested hospital recommendation based on proximity, facility capabilities, and severity. |

## Example JSON

```json
{
  "id": "inc-20261102-001",
  "lat": 37.774929,
  "lng": -122.419418,
  "timestamp": "2026-11-02T11:25:00Z",
  "photo_url": "https://storage.example.com/incidents/inc-20261102-001.jpg",
  "ai_summary": "Two-vehicle collision with moderate frontal damage. Airbags deployed. Potential minor injuries reported.",
  "status": "reported",
  "hospital_suggestion": "City General Emergency Hospital (1.8 km away, Level 1 Trauma Center)"
}
```
