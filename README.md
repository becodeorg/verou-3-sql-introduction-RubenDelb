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

### Introduce a new field status which can contain a long text indicating the reason for postponing (bonus points if it's a creative one)
- UPDATE `groups` SET status = 'The class has been postponed by 2 months because the coaches are too worried about the heavy snowfall in mid-summer.' WHERE id = 1;


### Delete someone from the learners table:
- DELETE FROM learners WHERE id = 5;