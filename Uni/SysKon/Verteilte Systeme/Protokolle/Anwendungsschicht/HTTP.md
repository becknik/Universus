---
tags: uni practical-cs syskon networking protocol
cards-deck: Uni::Courses::SysKon
completed: true
aliases:
    - HTTP
    - Hyper Text Transfer Protocol
linter-yaml-title-alias: HTTP
date-of-creation: 2023-01-07
mod-date: 2023-01-31
---

# HTTP
→ Nicht zu verwechseln mit [[HTML]]

## Eigenschaften
- Wurde von Tim Berners Lee (ein Physiker by SERN) entworfen
- Trennt das Format vom Inhalt für unterschiedlich große Terminals
- Ein weiteres Plain Text Protocol
	→ [[SMTP]]
- Verwendet eine [[../TCP|TCP]]-Verbindung, die für weiteren Daten-Austausch offen gelassen werden sollte
- Unterstützt seit *HTTP/1.1* mehrere Host pro Server, die jeweils in der Anfrage spezifiziert werden müssen

## Struktur (HTTP/1.1)

### Requests
- request-line: method `SP` request-uri `SP` HTTP-version `CR LF`
- (header-field `CR ôLF`)\*
	→ Stellt zusätzliche Infos & Parametrierung des Anfrageverhaltens bereit
- `CL RF`
- \[message-body\]
	→ Enthält Ressourcendaten (*MIME*) & kann weggelassen werden

#### Methods
| Method  | Request Semantic                                                                            |
| ------- | ------------------------------------------------------------------------------------------- |
| GET     | Request for a specified resource; Should only retrieve data                                 |
| HEAD    | Request for Response Header without body                                                    |
| POST    | Submitting an entity of data to the server                                                  |
|         | Might cause a change of state or side effects                                               |
| PUT     | Replace all current representation of a target resource with the "request payload" = Update | 
| DELETE  | Delete specified website resource                                                           |
| CONNECT | Establish tunnel connection to the server identified by the target resource                 |
| OPTIONS | Describe communication options for a target resource                                        |
| TRACE   | Loop-back received request - not implemented in web browsers?                               |
| PATCH   | Partial modifications to a resource                                                         |
- Frühe Browser modifizieren Standards für Attraktivität um weitere Funktionen aus Zwischenentwürfen:
	→ z.B. PATCH, LINK, UNLINK, COPY, MOVE, WRAPPED
- (V.6a, F.16)

### Responses

#### Generelle Struktur
- status-line: HTTP-version `SP` status-code `SP` reason-phrase `CR LF`
- (header-field `CR LF`)\*
	→ zum Beispiel Accept-Ranges, Entitäts-Tag (=ETag)
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
