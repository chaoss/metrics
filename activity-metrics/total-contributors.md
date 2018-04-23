# Total Contributors

## 1. Description
The total number of contributors over time on any platform.

## 2. Use Cases

## 3. Formula

## 4. Sample Filter and Visualization

### GHData
Shows a line graph of the number of contributers by month

## 5. Sample Implementation

### GHTorrent

```SQL
SELECT total_committers.created_at AS "date", MAX(@number_of_committers:=@number_of_committers+1) total_total_committers
FROM (
    SELECT author_id, MIN(DATE(created_at)) created_at
    FROM commits
    WHERE project_id = :repoid
    GROUP BY author_id
    ORDER BY created_at ASC) AS total_committers,
(SELECT @number_of_committers:= 0) AS number_of_committers
GROUP BY DATE(total_committers.created_at)
```

## 6. Known Implementations
[GHData](https://github.com/OSSHealth/ghdata)

## 7. Test Cases (Examples)

## 8. External References (Literature)
