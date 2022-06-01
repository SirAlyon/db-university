1.

SELECT * FROM `students` WHERE YEAR(date_of_birth) = 1990;



2.

SELECT * FROM `courses` WHERE cfu > 10;

Verifico anche tramite count: (479)

SELECT COUNT(id) FROM `courses` WHERE cfu > 10;



3.

SELECT * FROM `students` WHERE year(date_of_birth) < current_date - 30;



4.

SELECT * FROM `courses` WHERE `period` LIKE 'I %' AND `year`= 1;

Verifico anche tramite count: (286)

SELECT COUNT(id) FROM `courses` WHERE `period` LIKE 'I %' AND `year`= 1;