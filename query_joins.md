1.


SELECT `students` .`name`, `students` .`surname`
FROM `degrees`
JOIN `students` ON `degrees` .`id` = `students` .`degree_id`
WHERE `degrees` .`name` = 'Corso di Laurea in Economia';


_________________________________________________________


2.

SELECT `degrees` .`name`, `departments` .`name`
FROM `degrees`
JOIN `departments` ON `degrees` .`department_id` = `departments` .`id`
WHERE `departments` .`name` = 'Dipartimento di Neuroscienze' AND `degrees`.`level`= 'magistrale';

_________________________________________________________

3.

select `teachers`.`name`, `teachers`.`surname`, `courses`.`name`
FROM `teachers`
JOIN `course_teacher` ON `course_teacher` .`teacher_id` = `teachers` .`id`
JOIN `courses` ON `course_teacher` .`course_id` = `courses` .`id`
WHERE `teachers` .`id` = 44;

_________________________________________________________


4.

SELECT `students` .`name`, `students` .`surname`, `degrees` .`name`, `departments` .`name`
FROM `students`
JOIN `degrees` ON `students` .`degree_id` = `degrees`.`id`
JOIN `departments` ON `departments` .`id` = `degrees` .`department_id`
ORDER BY `students` .`surname`, `students` .`name`;