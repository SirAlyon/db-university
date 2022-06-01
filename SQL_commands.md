1.

SELECT * FROM `students` WHERE YEAR(date_of_birth) = 1990;

Verifico anche tramite count: (160)

SELECT count(id) FROM `students` WHERE YEAR(date_of_birth) = 1990;

____________________________________________________________________________


2.

SELECT * FROM `courses` WHERE cfu > 10;

Verifico anche tramite count: (479)

SELECT COUNT(id) FROM `courses` WHERE cfu > 10;

____________________________________________________________________________


3.

SELECT * FROM `students` WHERE year(date_of_birth) < current_date - 30;

____________________________________________________________________________


4.

SELECT * FROM `courses` WHERE `period` LIKE 'I %' AND `year`= 1;

Verifico anche tramite count: (286)

SELECT COUNT(id) FROM `courses` WHERE `period` LIKE 'I %' AND `year`= 1;
____________________________________________________________________________

5.

SELECT * FROM `exams` WHERE `date` = '2020-06-20' AND hour(hour) >= 14;

Verifico anche tramite count: (21)

SELECT COUNT(id) FROM `exams` WHERE `date` = '2020-06-20' AND hour(hour) >= 14;

____________________________________________________________________________

6.

SELECT * FROM `degrees` WHERE `level` = 'magistrale';

Verifico anche tramite count: (21)

SELECT count(id) FROM DEGREES WHERE `level` = 'magistrale';

____________________________________________________________________________


7.

SELECT COUNT(id) FROM `departments`;

____________________________________________________________________________


8.


SELECT COUNT(id) FROM `teachers` WHERE `phone` is null;