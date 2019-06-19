# Followers

## 1. Description
Number of followers (GitHub).

## 2. Use Cases
May indicate public interest in the project.

## 3. Formula

## 4. Sample Filter and Visualization

## 5. Sample Implementation

### AUGUR

```SQL
SELECT COUNT(user_id)
FROM followers
WHERE follower_id = :repo_id
GROUP BY follower_id
```

## 6. Known Implementations

[AUGUR](https://github.com/CHAOSS/Augur)

## 7. Test Cases (Examples)

## 8. External References (Literature)
