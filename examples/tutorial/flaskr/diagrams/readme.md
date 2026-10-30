# Tasca 2.2: Diagrames del Login
Alumne: Shafaq Majid

Aquí deixo els diagrames de seqüència UML de la pràctica de l'autenticació del blog Flaskr.

### 1. Happy Path (Login correcte)
L'usuari entra les seves dades reals, Flask busca a la base de dades sqlite, valida el hash de la contrasenya i inicia la sessió correctament obrint la pàgina del blog.

![Happy Path](diagrams/Diagrama%20de%20seq%C3%BC%C3%A8ncia%20flux%20principal(Happy%20Path).png)

---

### 2. Flux alternatiu 1: Credencials invàlides
L'usuari posa un password o username malament. Flask comprova que les dades no coincideixen i utilitza la funció flash() per carregar un missatge d'error i recarregar el formulari de login sense iniciar sessió.

![Credencials Invalides](diagrams/Escenari%20Credencials%20inv%C3%A0lides%20.png)

---

### 3. Flux alternatiu 2: Sistema no accessible
Hi ha un problema de connexió, el servidor està caigut o la base de dades sqlite està bloquejada. El codi intercepta aquesta fallada de connexió i retorna una pantalla amb un codi d'error 500 a l'usuari.

![Sistema No Accessible](diagrams/EscenariSistema%20no%20accessible%20.png)

---

### 4. Flux alternatiu 3: Format de correu incorrecte
L'usuari s'oblida d'escriure l'arrova (@) al camp del correu. La validació és nativa de l'HTML5 del navegador (front-end), de manera que el formulari es bloqueja abans d'enviar cap dada al servidor.

![Format Correu Incorrecte](diagrams/EscenariFormat%20del%20correu%20incorrecte%20.png)
