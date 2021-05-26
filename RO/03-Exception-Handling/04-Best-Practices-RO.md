# Cele Mai Bune Bractici

[slide hideTitle]

# Utilizarea Blocului Catch

[video src="https://videos.softuni.org/hls/Java/Java-Advanced/05-Exception-Handling/RO/Java-Advanced-Exceptions-and-Error-Handling-23-24-best-practices-using-catch-block-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Blocurile **Catch** trebuie să:

- înceapă cu excepțiile care se află cel mai jos în ierarhie
- continue cu excepțiile mai generale
- în caz contrar, va apărea o eroare de compilare

Fiecare bloc **catch** trebuie să gestioneze numai excepțiile care pot fi generate de cître cod în blocurile **try**:

- Dacă o metodă nu este menită pentru a gestiona o excepție, aceasta nu trebuie tratată

- Gestionarea tuturor excepțiilor fără a lua în considerare tipul lor este o practică proastă
[/slide]

[slide hideTitle]

# Alegerea Tipului de Excepție

[video src="https://videos.softuni.org/hls/Java/Java-Advanced/05-Exception-Handling/RO/Java-Advanced-Exceptions-and-Error-Handling-25-26-choosing-the-exception-type-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

- Când o aplicație încearcă să utilizeze **null** într-un caz în care este necesar un obiect:

| **Tipul de Excepție** | **Când se folosește** |
| --- | --- |
| **NullPointerException** | A fost accesat un indice nevalid într-o colecție. |
| **StringIndexOutOfBoundsException** | Un indice este fie negativ, fie mai mare decât dimensiunea șirului. |
| **NumberFormatException** | Programul încearcă să convertească un șir necorespunzător la unul dintre tipurile numerice. |
| **ArithmeticException** | Excepția este generată când apare o condiție aritmetică excepțională. |
| **ClassCastException** | O metodă a primit un argument nevalid. |

[/slide]

[slide hideTitle]

# Cele Mai Bune Practici

[video src="https://videos.softuni.org/hls/Java/Java-Advanced/05-Exception-Handling/RO/Java-Advanced-Exceptions-and-Error-Handling-27-28-exceptions-best-practices-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

Când generați o excepție, transmiteți întotdeauna constructorului un **mesaj explicativ corespunzător pentru eroarea apărută.**

Mesajul excepției ar trebui să explice ce cauzează problema și cum aceasta poate fi rezolvată.

- **Corect**: "Dimensiunea trebuie să fie un număr întreg în intervalul \[1…15\]"
- **Corect**: "Stare nevalidă. Primul apel Initialize()"
- **Greșit**: "Eroare neașteptată"
- **Greșit**: "Argument nevalid"

Excepțiile pot reduce performanța aplicației.

- Aruncați excepții numai în situații cu adevărat excepționale
- Nu aruncați excepții în fluxul normal de control al programului
- JVM poate arunca excepții în orice moment, fără nicio modalitate de a le prevedea, cum ar fi **StackOverflowError**

[/slide]
