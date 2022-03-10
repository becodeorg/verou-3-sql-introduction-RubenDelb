verou-3-sql-introduction-RubenDelb

# My used MySQL solutions:

### Get all data from the groups:
- SELECT * FROM `groups`

### Get the name and email of the first learner, and alias the name to learner_name:
- SELECT learners.name AS learner_name, learners.email FROM learners LIMIT 1;