<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Recherche sur l’éruption dentaire — Présentation 3D</title>

  <!-- Reveal.js CDN -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/reveal.css">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/theme/solarized.css" id="theme">

  <style>
    /* --- Styles pour l'effet 3D (cube "dent") --- */
    .scene {
      width: 260px;
      height: 260px;
      perspective: 900px;
      margin: 20px auto;
    }
    .cube {
      width: 100%;
      height: 100%;
      position: relative;
      transform-style: preserve-3d;
      transform: rotateX(-20deg) rotateY(30deg);
      transition: transform 0.8s;
      cursor: grab;
    }
    .cube:active { cursor: grabbing; }

    .cube__face {
      position: absolute;
      width: 260px;
      height: 260px;
      border: 1px solid rgba(0,0,0,0.08);
      display:flex;
      align-items:center;
      justify-content:center;
      font-weight:700;
      color:#333;
      background: linear-gradient(180deg,#fff 0%, #f8f8f8 100%);
      box-shadow: 0 8px 18px rgba(0,0,0,0.12);
      border-radius: 12px;
    }
    .cube__face img { max-width: 70%; max-height:70%; }

    .face-front  { transform: translateZ(130px); }
    .face-back   { transform: rotateY(180deg) translateZ(130px); }
    .face-right  { transform: rotateY(90deg) translateZ(130px); }
    .face-left   { transform: rotateY(-90deg) translateZ(130px); }
    .face-top    { transform: rotateX(90deg) translateZ(130px); }
    .face-bottom { transform: rotateX(-90deg) translateZ(130px); }

    /* Slide layout tweaks */
    .notes { font-size: 0.85em; color: #444; }
    .small { font-size: 0.9em; color: #222; }
    .to-right { display:flex; gap:24px; align-items:center; justify-content:center; flex-wrap:wrap; }

    /* Responsive */
    @media (max-width:900px){
      .scene { width: 200px; height: 200px; }
      .cube__face { width:200px; height:200px; }
    }
  </style>
</head>
<body>

  <div class="reveal">
    <div class="slides">

      <!-- Slide 1: Titre -->
      <section>
        <h1>Recherche sur l’éruption dentaire</h1>
        <h3>Présentation 3D — Aminemyoune13-spec</h3>
        <p class="small">Plan: 1) Définition et classification  2) Types de dents  3) Âge d’éruption  4) Rôle des dents</p>
        <aside class="notes">Introduction courte : définir l’objectif de la recherche et expliquer que des éléments 3D seront utilisés pour mieux visualiser.</aside>
      </section>

      <!-- Slide 2: Définition et classification -->
      <section>
        <h2>1. Définition et classification de la dentition</h2>
        <div class="to-right">
          <div style="max-width:520px;">
            <ul>
              <li><strong>Éruption dentaire :</strong> processus par lequel une dent perce la gencive et devient visible dans la cavité buccale.</li>
              <li><strong>Phases :</strong> formation, calcification, migration, pénétration.</li>
              <li><strong>Classification de la dentition :</strong>
                <ul>
                  <li>Déciduelle (dents temporaires, « bébé »)</li>
                  <li>Mixte (période de transition)</li>
                  <li>Définitive (dents permanentes)</li>
                </ul>
              </li>
            </ul>
          </div>

          <!-- 3D cube (illustratif) -->
          <div class="scene" id="scene-1">
            <div class="cube" id="cube-1">
              <div class="cube__face face-front"><img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/Tooth_icon.svg" alt="dent front"></div>
              <div class="cube__face face-back">Dentition</div>
              <div class="cube__face face-right">Déciduelle</div>
              <div class="cube__face face-left">Mixte</div>
              <div class="cube__face face-top">Définitive</div>
              <div class="cube__face face-bottom">Éruption</div>
            </div>
          </div>
        </div>
        <aside class="notes">Expliquer la différence entre les trois types de dentition et l'importance clinique de connaître ces phases.</aside>
      </section>

      <!-- Slide 3: Types de dents -->
      <section>
        <h2>2. Types des dents</h2>
        <div class="to-right">
          <div style="max-width:520px;">
            <ol>
              <li><strong>Incisives :</strong> bord tranchant — coupe les aliments.</li>
              <li><strong>Canines :</strong> pointues — déchirent et maintiennent.</li>
              <li><strong>Prémolaires :</strong> surface occlusale — écrasent et broient.</li>
              <li><strong>Molares :</strong> grandes surfaces — mastication et broyage.</li>
            </ol>
          </div>

          <!-- 3D cube with labels -->
          <div class="scene" id="scene-2">
            <div class="cube" id="cube-2">
              <div class="cube__face face-front">Incisives</div>
              <div class="cube__face face-back">Canines</div>
              <div class="cube__face face-right">Prémolaires</div>
              <div class="cube__face face-left">Molaires</div>
              <div class="cube__face face-top">Fonctions</div>
              <div class="cube__face face-bottom">Âge</div>
            </div>
          </div>
        </div>
        <aside class="notes">Donner exemples cliniques et montrer images radiographiques si disponibles.</aside>
      </section>

      <!-- Slide 4: L'âge d'éruption -->
      <section>
        <h2>3. L’âge de chaque type de dents (éruption moyenne)</h2>
        <div style="max-width:900px; margin: 0 auto;">
          <table style="width:100%; border-collapse:collapse;">
            <tr style="background:#efefef;">
              <th style="padding:8px; text-align:left">Type</th>
              <th style="padding:8px; text-align:left">Dents déciduelles (bébé)</th>
              <th style="padding:8px; text-align:left">Dents permanentes (approx.)</th>
            </tr>
            <tr>
              <td style="padding:8px">Incisives centrales</td>
              <td style="padding:8px">6-10 mois</td>
              <td style="padding:8px">7-8 ans</td>
            </tr>
            <tr>
              <td style="padding:8px">Incisives latérales</td>
              <td style="padding:8px">8-12 mois</td>
              <td style="padding:8px">8-9 ans</td>
            </tr>
            <tr>
              <td style="padding:8px">Canines</td>
              <td style="padding:8px">16-20 mois</td>
              <td style="padding:8px">11-12 ans</td>
            </tr>
            <tr>
              <td style="padding:8px">Prémolaires</td>
              <td style="padding:8px">— (absentes chez bébé)</td>
              <td style="padding:8px">10-12 ans</td>
            </tr>
            <tr>
              <td style="padding:8px">Molaires</td>
              <td style="padding:8px">12-16 mois (1ère molaires déciduelles)</td>
              <td style="padding:8px">6-7 ans (1ères molaires permanentes); 12-13 ans (2èmes molaires)</td>
            </tr>
            <tr>
              <td style="padding:8px">Dents de sagesse (3èmes molaires)</td>
              <td style="padding:8px">—</td>
              <td style="padding:8px">17-25 ans (variable)</td>
            </tr>
          </table>
        </div>
        <aside class="notes">Préciser que les âges sont des moyennes et varient selon l'individu, le sexe et l'ethnie.</aside>
      </section>

      <!-- Slide 5: Rôle de chaque type de dent -->
      <section>
        <h2>4. Le rôle de chaque type de dent</h2>
        <div class="to-right">
          <div style="max-width:520px;">
            <ul>
              <li><strong>Incisives :</strong> coupe et aide à la phonation (sons).</li>
              <li><strong>Canines :</strong> maintien de l'alignement, rôle esthétique, transmission des forces.</li>
              <li><strong>Prémolaires :</strong> traduit la transition entre canines et molaires, mastication fine.</li>
              <li><strong>Molares :</strong> broyage, surface occlusale pour la digestion mécanique.</li>
              <li><strong>Fonctions additionnelles :</strong> phonétique, esthétique, maintien de la hauteur verticale, protection des tissus mous.</li>
            </ul>
          </div>

          <div style="max-width:320px; text-align:center;">
            <img src="https://upload.wikimedia.org/wikipedia/commons/9/9b/Adult_dentition_plan.svg" alt="schéma dentition" style="max-width:100%; border-radius:8px; box-shadow:0 6px 16px rgba(0,0,0,0.12);">
            <p class="small">Schéma: dentition permanente (vue simplifiée)</p>
          </div>
        </div>
        <aside class="notes">Donner exemples cliniques : dysfonction masticatoire, troubles de la parole associés à perte de certaines dents.</aside>
      </section>

      <!-- Slide 6: Conséquences cliniques et prévention -->
      <section>
        <h2>Conséquences cliniques et recommandations</h2>
        <ul>
          <li>Retard d’éruption: rechercher causes systémiques ou locales.</li>
          <li>Surveillance de l’ordre d’éruption: permet détection précoce d’anomalies (agénésie, inclusion).</li>
          <li>Prévention: hygiène, fluor, visites régulières chez le dentiste pédiatrique.</li>
        </ul>
        <aside class="notes">Rappeler l'importance du suivi pédiatrique et expliquer quand référer à un spécialiste (orthodontiste, chirurgie).</aside>
      </section>

      <!-- Slide 7: Ressources et références -->
      <section>
        <h2>Ressources & Références</h2>
        <ol>
          <li>Textbook de dentisterie pédiatrique (ex. - Stewart / Pinkham).</li>
          <li>Articles cliniques sur les âges d’éruption (revues odontologiques).</li>
          <li>Sites: OMS, recommandations nationales.</li>
        </ol>
        <p class="small">Images libres de droits: Wikimedia Commons (liens intégrés dans la présentation).</p>
        <aside class="notes">Proposer des lectures complémentaires et indiquer les sources exactes si la présentation est utilisée académiquement.</aside>
      </section>

      <!-- Slide 8: Remerciements / Q&A -->
      <section>
        <h2>Merci — Questions ?</h2>
        <p>Présenté par: aminemyoune13-spec</p>
        <p class="small">Contact / notes: préparer démonstrations 3D supplémentaires si nécessaire.</p>
      </section>

    </div>
  </div>

  <!-- Reveal.js -->
  <script src="https://cdn.jsdelivr.net/npm/reveal.js@4.5.0/dist/reveal.js"></script>

  <script>
    // Initialiser Reveal
    Reveal.initialize({
      controls: true,
      progress: true,
      center: true,
      hash: true,
      slideNumber: true,
      transition: 'convex',
      dependencies: []
    });

    // Interaction simple pour faire tourner les cubes avec la souris (drag)
    function makeCubeInteractive(cubeId) {
      const cube = document.getElementById(cubeId);
      if (!cube) return;
      let dragging = false, startX=0, startY=0, rotX=-20, rotY=30;

      cube.addEventListener('mousedown', (e) => { dragging = true; startX = e.clientX; startY = e.clientY; });
      document.addEventListener('mousemove', (e) => {
        if (!dragging) return;
        const dx = e.clientX - startX;
        const dy = e.clientY - startY;
        const newY = rotY + dx * 0.3;
        const newX = rotX - dy * 0.3;
        cube.style.transform = `rotateX(${newX}deg) rotateY(${newY}deg)`;
      });
      document.addEventListener('mouseup', (e) => {
        if (!dragging) return;
        const dx = e.clientX - startX;
        const dy = e.clientY - startY;
        rotY += dx * 0.3;
        rotX -= dy * 0.3;
        dragging = false;
      });
    }

    makeCubeInteractive('cube-1');
    makeCubeInteractive('cube-2');

    // Astuce: appuyer sur 's' pour activer le mode speaker notes (Reveal a des plugins si besoin).
  </script>
</body>
</html>
