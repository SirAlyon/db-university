1.

SELECT count(id) AS `students`, year(`students`.`enrolment_date`) AS `year`
FROM `students`
GROUP BY year(`students`.`enrolment_date`);

____________________________________________________


2.

SELECT COUNT(id) as `teachers`, `office_address`
FROM `teachers`
GROUP BY `office_address`;


____________________________________________________

3.

SELECT AVG(`exam_student` .`vote`) AS `votes_average`, `exam_id`
FROM `exam_student`
GROUP BY `exam_id`;

____________________________________________________

4.

SELECT count(id) as `courses`, `degree_id`
FROM `courses`
GROUP BY `degree_id`;