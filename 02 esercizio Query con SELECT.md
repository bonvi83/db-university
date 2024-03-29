## Esercizio 02 con svolgimento:

Dopo aver creato un nuovo database nel vostro phpMyAdmin e aver importato lo schema allegato, eseguite le query:

1.  Selezionare tutti gli studenti nati nel 1990 (160)

    ```
    SELECT *
    FROM `students`
    WHERE YEAR(`date_of_birth`) = '1990';
    ```

2.  Selezionare tutti i corsi che valgono più di 10 crediti (479)

    ```
    SELECT *
    FROM `courses`
    WHERE `cfu` > 10;
    ```

3.  Selezionare tutti gli studenti che hanno più di 30 anni

    ```
    SELECT * FROM `students`
    WHERE YEAR(`date_of_birth`) >= '1993';
    ```

4.  Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)

    ```
    SELECT `name` AS "1^_semestre_1^anno"
    FROM `courses`
    WHERE `period` = "I semestre" AND `year` = "1";
    ```

5.  Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)

    ```
    SELECT *
    FROM `exams`
    WHERE DATE(`date`) = '2020-06-20' AND TIME(`hour`) > '14:00';
    ```

6.  Selezionare tutti i corsi di laurea magistrale (38)

    ```
    SELECT *
    FROM `degrees`
    WHERE `level` = 'magistrale';
    ```

7.  Da quanti dipartimenti è composta l'università? (12)

    questo è il numero:

    ```
    SELECT COUNT(id)
    FROM `departments`;
    ```

    questa è la lista:

    ```
    SELECT *
    FROM `departments`;
    ```

8.  Quanti sono gli insegnanti che non hanno un numero di telefono? (50)

    questo è il numero:

    ```
    SELECT COUNT(id)
    FROM `teachers`
    WHERE `phone` IS NULL;
    ```

    questa è la lista:

    ```
    SELECT *
    FROM `teachers`
    WHERE `phone` IS NULL;
    ```
