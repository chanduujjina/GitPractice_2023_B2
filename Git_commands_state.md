stateDiagram-v2
    [*] --> Unstaged

    Unstaged --> Staged : git add <file>
    Staged --> Commit : git commit -m "message"

    Commit --> Unstaged : edit file (working directory change)
    Staged --> Unstaged : git reset <file>
    Commit --> Staged : git reset --soft HEAD~1
    Commit --> Unstaged : git reset --mixed HEAD~1
    Commit --> [*]

    note right of Unstaged
      Files are modified but not yet staged
    end

    note right of Staged
      Files added to index, ready to commit
    end

    note right of Commit
      Changes permanently saved to local repo
    end
