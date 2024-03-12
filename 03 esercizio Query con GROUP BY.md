## Esercizio 03 con svolgimento:

Dopo aver creato un nuovo database nel vostro phpMyAdmin e aver importato lo schema allegato, eseguite le query:

1. Contare quanti iscritti ci sono stati ogni anno

   ```
    SELECT COUNT(*) AS `iscritti_per_anno`, YEAR(`enrolment_date`) AS `anno`
    FROM `students`
    GROUP BY YEAR(`enrolment_date`);
   ```

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

   ```
    SELECT COUNT(*) AS `numero_di_insegnanti`, `office_address` AS `indirizzo`
    FROM `teachers`
    GROUP BY `office_address`
    ORDER BY `numero_di_insegnanti` DESC;
   ```

3. Calcolare la media dei voti di ogni appello d'esame

   ```
    SELECT `exam_id` AS `appello`, AVG(`vote`) AS `media_voti`
    FROM `exam_student`
    GROUP BY `exam_id`;
   ```

4. Contare quanti corsi di laurea ci sono per ogni dipartimento

   ```
    SELECT `department_id` AS `dipartimento`, COUNT(`name`) AS `numero_di_corsi`
    FROM `degrees`
    GROUP BY `department_id`;
   ```
