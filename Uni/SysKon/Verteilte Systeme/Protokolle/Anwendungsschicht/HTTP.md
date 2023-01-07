---
tags: uni practical-cs syskon networking protocol
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
  - HTTP
  - Hyper Text Transfer Protocol
linter-yaml-title-alias: HTTP
date-of-creation: 2023-01-07
mod-date: 2023-01-07
---

# HTTP
-> [[HTML]]

## Eigenschaften
- Verwendet [[../TCP|TCP]]-Verbindung, die für weiteren Daten-Austausch offen gelassen werden kann
- Unterstützt seit *HTTP/1.1* mehrere Host pro Server, die jeweils in der Anfrage spezifiziert werden müssen

## Struktur (HTTP/1.1)

### Requests
- request-line: method `SP` request-uri `SP` HTTP-version `CR LF`
- (header-field `CR LF`)\*
	→ Stellt zusätzliche Infos & Parametrierung des Anfrageverhaltens bereit
- `CL RF`
- \[message-body\]
	→ Enthält Ressourcendaten (*MIME*) & kann weggelassen werden

#### Methods
| Method  | Request Semantic          |
| ------- | ------------------------- |
| OPTIONS | Get Communication Options |
| GET     | Request to Website        |
| HEAD    | Get Website Header        |
| POST    | Add data to a resource    |
| PUT     | Save Website on server    |
| DELETE  | Delete Website            |
| TRACE   | Echo received request     |
| CONNECT | Proxy stuff               |
- Frühe Browser modifizieren Standards für Attraktivität
	→ z.B. PATCH, LINK, UNLINK, COPY, MOVE, WRAPPED
- (V.6a, F.16)

### Responses
- status-line: HTTP-version `SP` status-code `SP` reason-phrase `CR LF`
- (header-field `CR LF`)\*
	→ zum Beispiel Accept-Ranges, ETag
- `CR LF`
- \[message-body\]

#### Status Codes
| Code | Description                                                                  |
| ---- | ---------------------------------------------------------------------------- |
| 1xx  | Informative/ ACK/ Continue                                                   |
| 2xx  | Success/ Accepted/ OK                                                        |
| 3xx  | Permanently Moved Request: Further operations needed to succeed with request |
| 4xx  | Client Request Error: Syntax Failure or not succeed-able                     |
| 5xx  | Internal Server Error                                                        |
