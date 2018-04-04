# Total Contributing Organizations

## 1. Description
The total number of organizations contributing over time.

## 2. Use Cases
Identifies organizational support.

## 3. Formula

## 4. Sample Filter and Visualization

## 5. Sample Implementation

### GHTorrent

```SQL
SELECT DISTINCT users.company
FROM project_members, users
WHERE project_members.project_id = :repoid
  AND project_members.user_id = users.id
```

## 6. Known Implementations

## 7. Test Cases (Examples)

## 8. External References (Literature)
