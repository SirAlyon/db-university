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

_________________________________________________________


5.

SELECT `degrees` .`name`, `courses` .`name`, `teachers` .`name`, `teachers` .`surname`
FROM `degrees` 
JOIN `courses` ON `courses` .`degree_id` = `degrees` .`id`
JOIN `course_teacher` ON `course_teacher` .`course_id` = `courses` .`id`
JOIN `teachers` ON `teachers`.`id` = `course_teacher` .`teacher_id`
ORDER BY `degrees` .`name`;

_________________________________________________________


6.

SELECT `teachers` .`name`, `teachers` .`surname`, `courses`.`name`, `degrees`.`name`
FROM `teachers`
JOIN `course_teacher` ON `course_teacher` .`teacher_id` = `teachers` .`id`
JOIN `courses` ON `course_teacher` .`course_id` = `courses` .`id`
JOIN `degrees` ON `degrees` .`id` = `courses` .`degree_id`
JOIN `departments` ON `departments`.`id` = `degrees` .`department_id`
WHERE `departments` .`name` = 'Dipartimento di Matematica'
ORDER BY `teachers` .`surname`;

_________________________________________________________



7.

SELECT `students` .`name` as `student_name`,`students` .`surname` as `students_surname`, `courses`.`name` as `course_name`, COUNT(`exam_student`.`exam_id`) as `attempts`
FROM `exam_student`
JOIN `students` ON `students`.`id` = `exam_student`.`student_id`
JOIN `exams` ON `exams` .`id` = `exam_student` .`exam_id`
JOIN `courses` ON `exams` .`course_id` = `courses` .`id`
GROUP BY `students`.`id`, `exams`.`course_id`
HAVING max(`exam_student`.`vote`) >= 18
ORDER BY `students` .`id`;