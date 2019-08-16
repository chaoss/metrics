# Merged Pull Requests

## 1. Description
The number of merged pull requests

## 2. Use Cases

## 3. Formula

`number of merged pull requests` = `number of total pull requests` - `number of rejected pull requests` - `number of open pull requests`

## 4. Sample Filter and Visualization

## 5. Sample Implementation

### AUGUR
Counting weekly pull requests merged into Ruby on Rails on GitHub, using GHTorrent:
```SQL
SELECT SUBDATE(DATE(created_at), WEEKDAY(DATE(created_at))) AS "date", count(*) as merged	
FROM pull_request_history
WHERE action = 'merged'
AND pull_request_id IN (SELECT id FROM pull_requests WHERE base_repo_id = 1334)
GROUP BY SUBDATE(DATE(created_at), WEEKDAY(DATE(created_at)))
```

## 6. Known Implementations

[AUGUR](https://github.com/CHAOSS/Augur)

## 7. Test Cases (Examples)

## 8. External References (Literature)
