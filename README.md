ER図

```mermaid
erDiagram
    User {
        string UUID
        number currentLevel
        number currentXp
        number nextLevelXp
    }

    AchievementSheet {
        string achievementSheetID
        string activity
        string date
        string goal
        string progress
        number progress_percentage
        string student_name
        string teacher
        string teacher_comment
        number xp_earned
    }

    Rating {
        string skill
        number value
    }

    User ||--o{ AchievementSheet : "has"
    AchievementSheet ||--o{ Rating : "has"
