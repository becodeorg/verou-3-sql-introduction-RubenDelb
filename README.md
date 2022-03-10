verou-3-sql-introduction-RubenDelb

# My used MySQL solutions:

### Get all data from the groups:
- SELECT * FROM `groups`

### Get the name and email of the first learner, and alias the name to learner_name:
- SELECT learners.name AS learner_name, learners.email FROM learners LIMIT 1;

### Update the start date of the first_group (make it two months later):
- UPDATE `groups` 
SET 
    start_date = DATE_ADD(start_date, INTERVAL 2 MONTH)
WHERE
    groups.name = 'verou-1';