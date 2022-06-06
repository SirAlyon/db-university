1.

SELECT count(id) AS `students`, year(`students`.`enrolment_date`) AS `year`
FROM `students`
GROUP BY year(`students`.`enrolment_date`);

____________________________________________________


2.

