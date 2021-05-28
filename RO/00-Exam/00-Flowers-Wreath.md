[slide hideTitle]
# Problemă: Flower Wreaths
[code-task title="Flower Wreaths" taskId="java-advanced-exam-Flower-Wreaths" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Scrieți codul dvs. aici
    }
}
```
[/code-editor]
[task-description]
# Descriere

Vreți să participați la un concurs de coroane de flori, dar pentru a participa trebuie să faceși cel puțin 5 coroane de flori.

Vi se vor oferi **două secvențe de numere întregi**, **reprezentând trandafiri și crini**.

Trebuie să începeți să faceți coroane, **știind că o coroană are nevoie de 15 flori**.

Scopul vostru este să faceți **cel puțin 5 coroane de flori**.

Veți începe să confecționați coroanele din **ultimii crini** și **primii trandafiri**.

Dacă suma valorilor lor este **egală** cu **15** - **confecționați o coroană** și **eliminați florile utilizate**.

Dacă suma lor este **mai mare de 15**, **micșorați** valoarea **crinilor cu 2**.
 
Dacă suma lor este **mai mică de 15, trebuie să le stocați pentru mai târziu și să le eliminați**.
 
Trebuie să vă opriți din confecționat atunci când nu mai aveți **trandafiri sau crini**.

În cele din urmă, dacă aveți **flori stocate, trebuie să faceți cât mai multe coroane de flori cu ele**.

## Intrare

- Pe **prima linie**, veți primi numere întregi care reprezintă **crinii**, **separați** prin **", "**

- Pe **a doua linie**, veți primi numere întregi reprezentând **trandafirii**, **separați** prin **", "**

## Ieșire

- Imprimați dacă ați reușit să faceți **cel puțin 5 coroane de flori**:
  - **"You made it, you are going to the competition with** \{**count of wreaths**\} **wreaths!"**
  - **"You didn't make it, you need** \{**wreaths needed**\} **wreaths more!"**

## Constrângeri

- Toate numerele date vor fi numere întregi valide în intervalul \[0, 120\]

- Nu aveți situație cu număr negativ

## Exemple

|**Intrare**|**Ieșire**|
|---|---|
|10, 15, 2, 7, 9, 13|You made it, you are going to the competition with 5 wreaths!|
|2, 10, 8, 12, 0, 5||

## Comentariu

- Începem cu ultimii crini (13) și primii trandafiri (2) -> 13 + 2 = 15 -> 15 = 15, ceea ce înseamnă că vom crea o coroană de flori și vom elimina ambele valori.

- Apoi avem 9 + 10 = 19 -> 19> 15, deci micșorăm numărul de crini cu 2 -> 7 + 10 = 17; micșorăm din nou numărul de crini cu 2 -> 5 + 10 = 15, creăm încă o coroană de flori și eliminăm valorile.

- Apoi, avem 7 + 8 = 15; creăm încă o coroană de flori și eliminăm valorile.

- Apoi, avem 2 + 12 = 14 -> 14 < 15, deci trebuie să stocăm florile pentru mai târziu și să eliminăm valorile.

- Apoi, avem 15 + 0 = 15, deci creăm încă o coroană de flori.

- Și, în sfârșit, avem 10 + 5 = 15, creăm încă o coroană de flori și ne oprim din confecționat coroane pentru că nu mai sunt flori rămase.

- Acum avem un total de 5 coroane de flori și mai avem 14 flori rămase, dar nu mai putem crea coroane de flori pentru că 14 < 15.

|**Intrare**|**Ieșire**|
|---|---|
|10, 5, 3, 7, 8|You didn't make, you need 1 wreaths more!|
|5, 10, 8, 7, 6||


[hints]
[hint]
Începem cu ultimii crini (**8**) și primii trandafiri (**5**):
**8** + **5** este egal cu **13**.
13 este **mai mic** decât 15, ceea ce înseamnă că trebuie să le **stocăm** suma pentru mai târziu și să le **eliminăm**.
[/hint] 
[hint]
Apoi, avem `7 + 10 = 17„

**Micșorăm** crinii cu **2**:
`5 + 10 = 15`

15 este **egal** cu 15 și creăm **o coroană de flori**.
[/hint] 
[hint]
Al treilea, avem `3 + 8 = 11`
**11** < **15** -\> le stocăm suma pentru mai târziu și le eliminăm.
[/hint] 
[hint]
Al patrulea, avem `5 + 7 = 12`
Le stocăm suma pentru mai târziu și le eliminăm.
[/hint] 
[hint]
Apoi, avem `10 + 6 = 16` -\> 16 \> 15
**Micșorăm** crinii cu **2** -\> `8 + 6 = 14`
Deoarece 14 este mai mic de 15, le **stocăm** suma pentru mai târziu și le eliminăm.
[/hint] 
[hint]
Și, în sfârșit, avem `10 + 5 = 15`, creăm încă o coroană de flori și nu mai amestecăm pentru că nu ne mai rămân flori.
[/hint] 
[hint]
Încetăm să mai creăm pentru că nu ne mai rămân flori.
Avem 1 coroană de flori și 50 de flori depozitate. 
Creăm încă 3 coroane de flori, deoarece `3 * 15 = 45` -> `50 - 45 = 5` -\> **5** \< **15**.
[/hint] 
[/hints] 

[/task-description]
[code-io /]
[tests]
[test open]
[input]
10, 15, 2, 7, 9, 13
2, 10, 8, 12, 0, 5
[/input]
[output]
You made it, you are going to the competition with 5 wreaths!
[/output]
[/test]
[test open]
[input]
10, 5, 3, 7, 8
5, 10, 8, 7, 6
[/input]
[output]
You didn't make it, you need 1 wreaths more!
[/output]
[/test]
[test]
[input]
10, 5, 7, 8, 15, 14
8, 7, 5, 10, 9
[/input]
[output]
You didn't make it, you need 1 wreaths more!
[/output]
[/test]
[test]
[input]
15, 20, 14, 8, 5
0, 0, 5, 6, 3
[/input]
[output]
You didn't make it, you need 2 wreaths more!
[/output]
[/test]
[test]
[input]
14, 14, 14, 14, 14
1, 1, 1, 1, 1
[/input]
[output]
You made it, you are going to the competition with 5 wreaths!
[/output]
[/test]
[test]
[input]
5, 6, 7, 8
1, 2, 3, 4
[/input]
[output]
You didn't make it, you need 3 wreaths more!
[/output]
[/test]
[test]
[input]
15, 15, 15, 15, 15
0, 0, 0, 0, 0
[/input]
[output]
You made it, you are going to the competition with 5 wreaths!
[/output]
[/test]
[test]
[input]
10, 5, 8, 6, 3
2, 3, 6, 4
[/input]
[output]
You didn't make it, you need 3 wreaths more!
[/output]
[/test]
[test]
[input]
0, 0, 0, 0, 0
0, 0, 0, 0, 0
[/input]
[output]
You didn't make it, you need 5 wreaths more!
[/output]
[/test]
[test]
[input]
14, 5, 7
1, 5, 4
[/input]
[output]
You didn't make it, you need 3 wreaths more!
[/output]
[/test]
[/tests]
[/code-task]
[/slide]
