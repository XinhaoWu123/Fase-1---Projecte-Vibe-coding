# 05 – Millores i Reflexió Final

**Projecte:** Plataformes v3 · Joc de plataformes en HTML5 Canvas  
**Fitxer principal:** `index.html`
Fitxer del joc:
[Fitxer principal del joc](mario/mario_platformer_game.html)
---

## 1. Millores identificades

A continuació s'enumeren **5 millores identificades** durant la revisió del codi, ordenades per prioritat:

### M1 · Sistema de pausa *(aplicada)*
**Problema:** El joc no tenia cap manera d'aturar-se temporalment. El temporitzador seguia corrent fins i tot si l'usuari havia de fer una altra cosa.

**Solució:** Afegir un botó de pausa i gestionar l'estat `'paused'`, suspenent el bucle principal (`cancelAnimationFrame`) i el temporitzador (`clearInterval`).

---

### M2 · Indicador visual del temps restant (barra de progrés) *(aplicada)*

**Problema:** El temps es mostrava només com a número (`<span id="timer">`). Quan quedaven pocs segons, l'usuari no ho percebia immediatament de manera visual.

**Solució:** Substituir el comptador de text per una barra de progrés de color que va canviant de verd → groc → vermell a mesura que s'acaba el temps.

---

### M3 · Pantalla de Game Over amb puntuació animada *(aplicada)*

**Problema:** La pantalla final mostrava la puntuació de manera estàtica i sense context.

**Solució:** Afegir una animació de puntuació progressiva i informació contextual segons el rendiment.

---

### M4 · Mòbil: control tàctil millorat *(identificada, no aplicada)*

**Problema:** Els botons tàctils podien perdre pulsacions en dispositius ràpids.

**Pla:**
- Afegir `touchstart`
- Afegir `touchend`
- Augmentar la mida dels botons a 48×48 px

---

### M5 · Spawning de partícules fora de pantalla *(identificada, no aplicada)*

**Problema:** Es dibuixen partícules fora del camp visible.

**Pla:**

```javascript
if (p.x - camera.x < -20 || p.x - camera.x > W + 20)
    continue;

