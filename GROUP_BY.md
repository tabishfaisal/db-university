// 1. Contare quanti iscritti ci sono stati ogni anno //

SELECT count(*) AS `enrolment_count`, YEAR(`enrolment_date`) AS `enrolment_year`
FROM `students`
GROUP BY `enrolment_year`

///

// 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio //

SELECT COUNT(*) AS `numero-of-teachers`, `office_number` AS `edificio`
FROM `teachers`
GROUP BY `edificio`

///

// 3. Calcolare la media dei voti di ogni appello d'esame //




// 4. Contare quanti corsi di laurea ci sono per ogni dipartiment //