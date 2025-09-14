# YouLearn AI – Database Schema

```mermaid
erDiagram
    USERS {
        string id PK
        string name
        string email
    }
    PLAYLISTS {
        string id PK
        string user_id FK
        string title
        number progress
    }
    LESSONS {
        string id PK
        string playlist_id FK
        string title
        string url
        number duration
        boolean is_completed
    }
    NOTES {
        string id PK
        string lesson_id FK
        text content
    }
    AI_SUMMARIES {
        string id PK
        string lesson_id FK
        text summary
    }
    COMMENTS {
        string id PK
        string lesson_id FK
        string user_id FK
        text content
    }
