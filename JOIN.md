// 1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia//

SELECT `students`.*,`degrees`.`name` AS `degrees_name`
FROM `students`
JOIN `degrees`
ON  `students`.`degree_id` =`degrees`.`id`
WHERE `degrees`.`name` = 'Corso di Laurea in Economia'

///

// 2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze//

SELECT `degrees`.*, `departments`.`name` AS `name_of_department`
FROM `degrees`
JOIN `departments`
ON `degrees`.`department_id` = `departments`.`id`
WHERE `degrees`.`level` = 'magistrale' AND `departments`.`name` = 'Dipartimento di Neuroscienze'

///

// 3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44) //

FROM `courses`
JOIN `course_teacher` AS `id-teacher`
ON `courses`.`id`= `id-teacher`.`course_id`
JOIN `teachers`
ON `id-teacher`.`teacher_id` = `teachers`.`id`
WHERE `teachers`.`id`= 44

///

// 4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
nome // 

SELECT  `students`.`name` AS `name`, `students`.`surname` AS `surname`, `degrees`.`name` AS `degree`,`departments`.`name` AS `department`
FROM `students`
JOIN `degrees`
ON `students`.`degree_id` = `degrees`.`id`
JOIN `departments`
ON `degrees`.`department_id` = `departments`.`id`
ORDER BY `students`.`name` ASC 

///

// 5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti //



///

// 6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54) //



// 7. BONUS: Selezionare per ogni studente il numero di tentativi sostenuti
per ogni esame, stampando anche il voto massimo. Successivamente,
filtrare i tentativi con voto minimo 18.//



////