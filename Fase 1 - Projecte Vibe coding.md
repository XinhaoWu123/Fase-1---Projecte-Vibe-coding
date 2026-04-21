# 📄 01_idea_i_abast.md

## 1. Idea del joc

### 🎯 Objectiu
El jugador ha d’arribar al final del nivell en el menor temps possible, superant obstacles i enemics en un únic mapa.

### 🎮 Rol del jugador
El jugador controla un personatge que es pot moure horitzontalment (esquerra/dreta) i saltar per superar obstacles i enemics.

---

### 📜 Regles i condicions
- El jugador comença amb una vida.
- Si col·lisiona amb un enemic:
  - Perd vida si el toca lateralment.
  - El pot eliminar si hi salta a sobre.
- Si la vida arriba a 0 → derrota.
- Si el jugador arriba a la meta → victòria.
- Hi ha un temps límit per completar el nivell.

---

### 🔁 Bucle de joc
1. Llegir input del jugador (tecles A/D i salt)
2. Actualitzar moviment del jugador
3. Aplicar gravetat i física
4. Moure enemics amb patró repetitiu
5. Detectar col·lisions
6. Aplicar resultats de col·lisions (vida, eliminació enemics)
7. Comprovar condicions de victòria o derrota
8. Repetir mentre el joc estigui actiu

---

### 📊 Estats del joc

- **Vida**: el jugador comença amb 1 vida i pot obtenir-ne més en blocs especials.
- **Posició**: coordenades del jugador dins del mapa (x, y).
- **Puntuació**: augmenta en funció dels enemics eliminats.
- **Temps**: límit per completar el nivell.

**Estat del joc:**
- Jugant  
- Guanyat  
- Perdut  

---

### 🎯 Repte i dificultat
- Coordinació entre moviment i salts.
- Gestió del temps limitat.
- Evitar enemics i obstacles.
- Progressió de dificultat moderada dins d’un únic nivell.

---

### ⚠️ Limitacions
- Només hi haurà un únic mapa.
- No hi haurà múltiples nivells ni progressió entre pantalles.
- Nombre limitat d’enemics.
- Enemics amb comportament simple (moviment repetitiu).
- No hi haurà IA avançada d’enemics.
- No hi haurà sistema de guardat.
- No hi haurà menú complex.
- Gràfics simples (formes bàsiques o sprites senzills).
- Sense animacions avançades.

---

## 2. Riscos tècnics

### 1. Gravetat i física del jugador
- **Risc**: comportament incorrecte en salts i caigudes.  
- **Solució**: aplicar una velocitat vertical amb gravetat constant i detectar col·lisions amb el terra mitjançant rectangles simples.

### 2. Moviment i comportament dels enemics
- **Risc**: inconsistència en el moviment o col·lisions incorrectes.  
- **Solució**: utilitzar moviments lineals o patrons repetitius amb velocitat fixa i sense IA complexa.

### 3. Gestió d’input del jugador
- **Risc**: resposta incorrecta o retard en el control.  
- **Solució**: capturar input per frame i separar la lectura d’input de la lògica de moviment.

---

## 3. Exploració amb IA

### Prompt 1
> "Actua com a desenvolupador de videojocs i genera l’estructura de carpetes i fitxers per a un joc 2D tipus plataforma en JavaScript amb HTML5 Canvas. Inclou separació de codi per jugador, enemics, col·lisions i renderitzat."

**Resultat:** proposta d’estructura modular amb separació de responsabilitats.

### Prompt 2
> "Explica com implementar moviment de jugador amb gravetat, salts i col·lisions en un joc 2D de plataformes utilitzant JavaScript i HTML5 Canvas, amb pseudocodi senzill."

**Resultat:** ús de velocitat vertical, gravetat constant i detecció de col·lisions amb el terra.

---

## 4. Proposta final i viabilitat

### 📌 Proposta final
Joc de plataformes 2D en un únic nivell on el jugador ha d’arribar a la meta evitant enemics i obstacles, amb física bàsica, salts i col·lisions.

### ✅ Viabilitat
- **Temps estimat**: ≤ 10 hores  
- **Complexitat**: baixa-mitjana  
- **Recursos**: mínims (Canvas + JavaScript)  
- **Dependències**: cap llibreria externa  

✔ Projecte completament viable dins del temps disponible.

---

## 5. Pla de treball

### 🧱 Inicialització del projecte
- Configuració de HTML, CSS i JavaScript  
- Estructura de carpetes  

### 🕹️ Moviment del jugador
- Controls amb teclat  
- Moviment esquerra/dreta  

### ⬆️ Sistema de gravetat i salt
- Aplicació de gravetat  
- Implementació del salt  
- Detecció de terra  

### 👾 Implementació d’enemics
- Creació d’enemics simples  
- Moviment amb patró repetitiu  

### 💥 Sistema de col·lisions
- Col·lisions amb terra  
- Col·lisions amb enemics  
- Interaccions (vida i eliminació enemics)  

### 🏁 Objectiu del joc (meta)
- Definició del punt final  
- Condició de victòria  

### 🧪 Testing i poliment
- Proves generals  
- Ajust de dificultat  
- Correcció d’errors  

---

## 6. Eines i tecnologies

### 💻 Llenguatge de programació
- JavaScript, HTML5 i CSS  
- JavaScript per a la lògica del joc  
- HTML per l’estructura  
- CSS per l’estil visual  

### 🛠️ IDE
- Visual Studio Code  
  - Lleuger  
  - Gratuït  
  - Compatible amb JavaScript  
  - Gran ecosistema d’extensions  

### 🤖 Intel·ligència artificial
- Google Gemini  
  - Suport en generació d’idees  
  - Ajuda en dubtes tècnics  
  - Assistència en documentació i exemples  

### 📚 Llibreries
- No s’utilitzaran llibreries externes  
- Desenvolupament amb JavaScript pur (**vanilla JS**) i Canvas  
