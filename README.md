[fiche-accueil-eeem-fes.html](https://github.com/user-attachments/files/26509092/fiche-accueil-eeem-fes.html)
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fiche d'Accueil — EEEM Fès</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --gold:#C9A84C;--gold-light:#E8D5A3;--gold-dim:rgba(201,168,76,0.18);
  --navy:#0A1628;--navy-mid:#122040;--navy-card:#162848;--navy-input:#0E1C36;
  --text-light:#E8EAF0;--text-muted:#8A9BBF;
  --radius:10px;--error:#E05252;--success:#4CAF8A;
}
*{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
body{font-family:'Jost',sans-serif;background:var(--navy);min-height:100vh;color:var(--text-light);padding-top:56px;}
body::before{content:'';position:fixed;inset:0;background:radial-gradient(ellipse 60% 40% at 10% 0%,rgba(201,168,76,0.09) 0%,transparent 70%),radial-gradient(ellipse 50% 50% at 90% 100%,rgba(42,65,112,0.6) 0%,transparent 70%);pointer-events:none;z-index:0;}

/* LANG BAR */
#lang-bar{position:fixed;top:0;left:0;right:0;height:56px;background:rgba(10,22,40,0.97);border-bottom:1px solid var(--gold-dim);display:flex;align-items:center;justify-content:center;padding:0 12px;gap:5px;z-index:200;backdrop-filter:blur(12px);flex-wrap:wrap;}
.lang-btn{background:none;border:1px solid rgba(201,168,76,0.3);color:var(--gold-light);font-family:'Jost',sans-serif;font-size:10px;font-weight:500;letter-spacing:.06em;padding:4px 10px;border-radius:20px;cursor:pointer;transition:all .2s;}
.lang-btn:hover,.lang-btn.active{background:var(--gold);color:var(--navy);border-color:var(--gold);}

/* WRAPPER */
.wrapper{position:relative;z-index:1;max-width:640px;margin:0 auto;padding:28px 16px 80px;}

/* HEADER */
.header-card{background:linear-gradient(135deg,var(--navy-card) 0%,var(--navy-mid) 100%);border:1px solid var(--gold-dim);border-radius:16px;padding:32px 28px 24px;text-align:center;margin-bottom:24px;position:relative;overflow:hidden;animation:fadeUp .6s ease both;}
.header-card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,transparent,var(--gold),transparent);}
.logo-circle{width:90px;height:90px;border-radius:50%;background:rgba(201,168,76,0.12);border:2px solid var(--gold-dim);display:flex;align-items:center;justify-content:center;margin:0 auto 16px;font-size:36px;}
.church-name{font-family:'Cormorant Garamond',serif;font-size:21px;font-weight:600;color:var(--gold);letter-spacing:.03em;line-height:1.3;margin-bottom:5px;}
.church-sub{font-size:12px;color:var(--text-muted);font-weight:300;letter-spacing:.05em;margin-bottom:14px;}
.church-tel{font-size:13px;color:var(--gold-light);font-weight:400;margin-bottom:14px;letter-spacing:.04em;}
.welcome-text{font-size:13.5px;color:var(--text-light);line-height:1.7;font-weight:300;border-top:1px solid var(--gold-dim);padding-top:14px;font-style:italic;font-family:'Cormorant Garamond',serif;}

/* DATE ROW */
.date-row{margin-bottom:20px;animation:fadeUp .6s .1s ease both;}

/* SECTION */
.section{background:var(--navy-card);border:1px solid rgba(201,168,76,0.12);border-radius:var(--radius);padding:22px 20px 18px;margin-bottom:16px;animation:fadeUp .6s ease both;}
.section-title{font-size:10px;font-weight:600;letter-spacing:.15em;text-transform:uppercase;color:var(--gold);margin-bottom:16px;display:flex;align-items:center;gap:8px;}
.section-title::after{content:'';flex:1;height:1px;background:linear-gradient(90deg,var(--gold-dim),transparent);}

/* FIELDS */
.field{margin-bottom:14px;}
.field:last-child{margin-bottom:0;}
label{display:block;font-size:11.5px;font-weight:500;color:var(--gold-light);letter-spacing:.05em;margin-bottom:5px;}
label .req{color:var(--gold);margin-left:2px;}
input[type=text],input[type=tel],input[type=date],select,textarea{width:100%;background:var(--navy-input);border:1px solid rgba(201,168,76,0.2);border-radius:8px;color:var(--text-light);font-family:'Jost',sans-serif;font-size:14px;font-weight:300;padding:10px 13px;transition:border-color .2s,box-shadow .2s;outline:none;-webkit-appearance:none;appearance:none;}
input:focus,select:focus,textarea:focus{border-color:var(--gold);box-shadow:0 0 0 3px rgba(201,168,76,0.1);}
select{background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath d='M1 1l5 5 5-5' stroke='%23C9A84C' stroke-width='1.5' fill='none' stroke-linecap='round'/%3E%3C/svg%3E");background-repeat:no-repeat;background-position:right 13px center;padding-right:34px;}
select option{background:var(--navy-mid);color:var(--text-light);}
textarea{resize:vertical;min-height:72px;}
input::placeholder,textarea::placeholder{color:var(--text-muted);font-weight:300;}
.grid-2{display:grid;grid-template-columns:1fr 1fr;gap:12px;}

/* RADIO */
.radio-group{display:flex;flex-wrap:wrap;gap:8px;margin-top:2px;}
.radio-label{display:flex;align-items:center;gap:7px;background:var(--navy-input);border:1px solid rgba(201,168,76,0.2);border-radius:8px;padding:8px 13px;cursor:pointer;transition:all .2s;font-size:13px;color:var(--text-light);font-weight:400;}
.radio-label:hover{border-color:var(--gold);background:rgba(201,168,76,0.05);}
.radio-label input{display:none;}
.radio-label.selected{border-color:var(--gold);background:rgba(201,168,76,0.12);color:var(--gold-light);}
.radio-dot{width:15px;height:15px;border-radius:50%;border:1.5px solid rgba(201,168,76,0.4);background:transparent;transition:all .2s;flex-shrink:0;}
.radio-label.selected .radio-dot{background:var(--gold);border-color:var(--gold);box-shadow:0 0 0 3px rgba(201,168,76,0.15);}

/* CONDITIONAL */
.conditional{display:none;margin-top:12px;padding:12px;background:rgba(201,168,76,0.04);border:1px solid var(--gold-dim);border-radius:8px;}
.conditional.show{display:block;animation:fadeIn .3s ease;}

/* ERRORS */
.field-error{font-size:11px;color:var(--error);margin-top:4px;display:none;}
.field.invalid input,.field.invalid select,.field.invalid textarea{border-color:var(--error);}
.field.invalid .field-error{display:block;}

/* SUBMIT */
.submit-btn{width:100%;background:linear-gradient(135deg,var(--gold) 0%,#A07830 100%);color:var(--navy);font-family:'Jost',sans-serif;font-size:14px;font-weight:600;letter-spacing:.12em;text-transform:uppercase;border:none;border-radius:10px;padding:15px 32px;cursor:pointer;transition:all .25s;margin-top:8px;box-shadow:0 4px 20px rgba(201,168,76,0.25);}
.submit-btn:hover{transform:translateY(-1px);box-shadow:0 8px 30px rgba(201,168,76,0.35);}
.submit-btn:active{transform:translateY(0);}
.submit-btn.loading{opacity:.7;pointer-events:none;}

/* SUCCESS */
#success-screen{display:none;position:fixed;inset:0;z-index:300;background:var(--navy);flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:40px;}
#success-screen.show{display:flex;}
.success-icon{width:72px;height:72px;border-radius:50%;background:rgba(76,175,138,0.15);border:2px solid var(--success);display:flex;align-items:center;justify-content:center;font-size:32px;margin-bottom:24px;animation:popIn .4s cubic-bezier(0.34,1.56,0.64,1);}
.success-title{font-family:'Cormorant Garamond',serif;font-size:28px;color:var(--gold);margin-bottom:12px;}
.success-sub{font-size:15px;color:var(--text-muted);line-height:1.7;max-width:320px;}
.success-btn{margin-top:24px;background:none;border:1px solid var(--gold-dim);color:var(--gold-light);font-family:'Jost',sans-serif;font-size:13px;padding:10px 24px;border-radius:20px;cursor:pointer;transition:all .2s;}
.success-btn:hover{background:var(--gold);color:var(--navy);}

@keyframes fadeUp{from{opacity:0;transform:translateY(16px);}to{opacity:1;transform:translateY(0);}}
@keyframes fadeIn{from{opacity:0;}to{opacity:1;}}
@keyframes popIn{from{transform:scale(0.5);opacity:0;}to{transform:scale(1);opacity:1;}}
.section:nth-child(1){animation-delay:.05s;}.section:nth-child(2){animation-delay:.10s;}.section:nth-child(3){animation-delay:.15s;}.section:nth-child(4){animation-delay:.20s;}
@media(max-width:500px){.grid-2{grid-template-columns:1fr;}.header-card{padding:24px 14px 18px;}.section{padding:18px 14px 14px;}}
</style>
</head>
<body>

<!-- LANG BAR -->
<div id="lang-bar">
  <button class="lang-btn active" onclick="setLang('fr')">FR</button>
  <button class="lang-btn" onclick="setLang('en')">EN</button>
  <button class="lang-btn" onclick="setLang('es')">ES</button>
  <button class="lang-btn" onclick="setLang('pt')">PT</button>
  <button class="lang-btn" onclick="setLang('ar')">عربية</button>
  <button class="lang-btn" onclick="setLang('ln')">Lingala</button>
</div>

<!-- SUCCESS -->
<div id="success-screen">
  <div class="success-icon">✓</div>
  <div class="success-title" id="success-title">Merci !</div>
  <div class="success-sub" id="success-sub">Votre fiche a bien été enregistrée.<br>Bienvenue parmi nous 🙏</div>
  <button class="success-btn" onclick="resetForm()" id="btn-new">Remplir une nouvelle fiche</button>
</div>

<div class="wrapper">

  <!-- HEADER -->
  <div class="header-card">
    <div class="logo-circle">✝</div>
    <div class="church-name" id="txt-name">Église Évangélique au Maroc</div>
    <div class="church-sub" id="txt-sub">Paroisse de Fès</div>
    <div class="church-tel">📞 +212 75 464 6086</div>
    <div class="welcome-text" id="txt-welcome">L'Église Évangélique au Maroc, Paroisse de Fès, vous accueille chaleureusement.<br>Pour mieux vous servir et vous accompagner dans votre croissance spirituelle,<br>merci de remplir cette fiche.</div>
  </div>

  <form id="main-form" novalidate>

    <!-- DATE -->
    <div class="date-row">
      <div class="field" id="f-date">
        <label id="lbl-date">Date du jour <span class="req">*</span></label>
        <input type="date" name="date" id="inp-date" required>
        <div class="field-error" id="err-date">Champ requis</div>
      </div>
    </div>

    <!-- IDENTITÉ -->
    <div class="section">
      <div class="section-title" id="ttl-identity">Identité</div>

      <div class="grid-2">
        <div class="field" id="f-nom">
          <label id="lbl-nom">Nom <span class="req">*</span></label>
          <input type="text" name="nom" id="inp-nom" placeholder="Nom de famille" required>
          <div class="field-error" id="err-nom">Requis</div>
        </div>
        <div class="field" id="f-prenom">
          <label id="lbl-prenom">Prénom <span class="req">*</span></label>
          <input type="text" name="prenom" id="inp-prenom" placeholder="Prénom" required>
          <div class="field-error" id="err-prenom">Requis</div>
        </div>
      </div>

      <div class="grid-2">
        <div class="field" id="f-sexe">
          <label id="lbl-sexe">Sexe <span class="req">*</span></label>
          <select name="sexe" id="inp-sexe" required>
            <option value="" id="o-sx0">— Choisir —</option>
            <option value="homme" id="o-sx1">Homme</option>
            <option value="femme" id="o-sx2">Femme</option>
          </select>
          <div class="field-error" id="err-sexe">Requis</div>
        </div>
        <div class="field" id="f-nationalite">
          <label id="lbl-nationalite">Nationalité <span class="req">*</span></label>
          <input type="text" name="nationalite" id="inp-nationalite" placeholder="ex: Ivoirienne" required>
          <div class="field-error" id="err-nationalite">Requis</div>
        </div>
      </div>

      <div class="grid-2">
        <div class="field" id="f-tel">
          <label id="lbl-tel">Téléphone <span class="req">*</span></label>
          <input type="tel" name="telephone" id="inp-tel" placeholder="+212 6xx xxx xxx" required>
          <div class="field-error" id="err-tel">Requis</div>
        </div>
        <div class="field" id="f-quartier">
          <label id="lbl-quartier">Quartier</label>
          <input type="text" name="quartier" id="inp-quartier" placeholder="Quartier / Zone">
        </div>
      </div>
    </div>

    <!-- SPIRITUEL -->
    <div class="section">
      <div class="section-title" id="ttl-spiritual">Parcours spirituel</div>

      <div class="field" id="f-baptise">
        <label id="lbl-baptise">Êtes-vous déjà baptisé(e) ? <span class="req">*</span></label>
        <div class="radio-group" id="rg-baptise">
          <label class="radio-label" onclick="sel(this,'baptise')">
            <input type="radio" name="baptise" value="oui"><div class="radio-dot"></div><span id="o-bap-y">Oui</span>
          </label>
          <label class="radio-label" onclick="sel(this,'baptise')">
            <input type="radio" name="baptise" value="non"><div class="radio-dot"></div><span id="o-bap-n">Non</span>
          </label>
        </div>
        <div class="field-error" id="err-baptise">Veuillez répondre</div>
      </div>

      <div class="field" style="margin-top:16px;" id="f-service">
        <label id="lbl-service">Servez-vous déjà dans votre pays ou au Maroc ? <span class="req">*</span></label>
        <div class="radio-group" id="rg-service">
          <label class="radio-label" onclick="sel(this,'service');show('cond-service')">
            <input type="radio" name="service" value="oui"><div class="radio-dot"></div><span id="o-srv-y">Oui</span>
          </label>
          <label class="radio-label" onclick="sel(this,'service');hide('cond-service')">
            <input type="radio" name="service" value="non"><div class="radio-dot"></div><span id="o-srv-n">Non</span>
          </label>
        </div>
        <div class="field-error" id="err-service">Veuillez répondre</div>
        <div class="conditional" id="cond-service">
          <label id="lbl-serviceLequel">Si oui, lequel ?</label>
          <input type="text" name="serviceLequel" id="inp-serviceLequel" placeholder="ex: Chorale, Enseignement, Intercession...">
        </div>
      </div>
    </div>

    <!-- SÉJOUR -->
    <div class="section">
      <div class="section-title" id="ttl-sejour">Séjour au Maroc</div>

      <div class="field" id="f-duree">
        <label id="lbl-duree">Combien de temps pensez-vous rester au Maroc ? <span class="req">*</span></label>
        <div class="radio-group" id="rg-duree">
          <label class="radio-label" onclick="sel(this,'duree');hide('cond-duree-autre')">
            <input type="radio" name="duree" value="3ans"><div class="radio-dot"></div><span id="o-dur-3">3 ans</span>
          </label>
          <label class="radio-label" onclick="sel(this,'duree');hide('cond-duree-autre')">
            <input type="radio" name="duree" value="5ans"><div class="radio-dot"></div><span id="o-dur-5">5 ans</span>
          </label>
          <label class="radio-label" onclick="sel(this,'duree');show('cond-duree-autre')">
            <input type="radio" name="duree" value="autre"><div class="radio-dot"></div><span id="o-dur-a">Autre</span>
          </label>
        </div>
        <div class="field-error" id="err-duree">Veuillez répondre</div>
        <div class="conditional" id="cond-duree-autre">
          <label id="lbl-dureeAutre">Précisez la durée</label>
          <input type="text" name="dureeAutre" id="inp-dureeAutre" placeholder="ex: 6 mois, 1 an...">
        </div>
      </div>

      <div class="field" style="margin-top:16px;" id="f-raison">
        <label id="lbl-raison">Raison de votre arrivée au Maroc <span class="req">*</span></label>
        <div class="radio-group" id="rg-raison">
          <label class="radio-label" onclick="sel(this,'raison');show('cond-etudes');hide('cond-autre-raison')">
            <input type="radio" name="raison" value="etudes"><div class="radio-dot"></div><span id="o-r-et">Études</span>
          </label>
          <label class="radio-label" onclick="sel(this,'raison');hide('cond-etudes');hide('cond-autre-raison')">
            <input type="radio" name="raison" value="travail"><div class="radio-dot"></div><span id="o-r-tr">Travail</span>
          </label>
          <label class="radio-label" onclick="sel(this,'raison');hide('cond-etudes');hide('cond-autre-raison')">
            <input type="radio" name="raison" value="entrepreneuriat"><div class="radio-dot"></div><span id="o-r-en">Entrepreneuriat</span>
          </label>
          <label class="radio-label" onclick="sel(this,'raison');hide('cond-etudes');show('cond-autre-raison')">
            <input type="radio" name="raison" value="autre"><div class="radio-dot"></div><span id="o-r-au">Autre</span>
          </label>
        </div>
        <div class="field-error" id="err-raison">Veuillez répondre</div>
        <div class="conditional" id="cond-etudes">
          <label id="lbl-ecole">Quelle école / université ?</label>
          <input type="text" name="ecole" id="inp-ecole" placeholder="Nom de l'établissement">
        </div>
        <div class="conditional" id="cond-autre-raison">
          <label id="lbl-autreRaison">Précisez</label>
          <input type="text" name="autreRaison" id="inp-autreRaison" placeholder="Votre raison...">
        </div>
      </div>
    </div>

    <!-- NOTES -->
    <div class="section">
      <div class="section-title" id="ttl-notes">Notes</div>
      <div class="field">
        <label id="lbl-notes">Besoins de prière / Message pour l'équipe pastorale</label>
        <textarea name="notes" id="inp-notes" placeholder="Partagez librement..."></textarea>
      </div>
    </div>

    <button type="submit" class="submit-btn" id="btn-submit">✦ <span id="btn-txt">Enregistrer ma fiche</span></button>

  </form>
</div>

<script>
// ── TRADUCTIONS ──
const T = {
  fr:{
    name:'Église Évangélique au Maroc',sub:'Paroisse de Fès',
    welcome:"L'Église Évangélique au Maroc, Paroisse de Fès, vous accueille chaleureusement.\nPour mieux vous servir et vous accompagner dans votre croissance spirituelle,\nmerci de remplir cette fiche.",
    date:'Date du jour',identity:'Identité',nom:'Nom',prenom:'Prénom',
    sexe:'Sexe',sx0:'— Choisir —',sx1:'Homme',sx2:'Femme',
    nationalite:'Nationalité',natph:'ex: Ivoirienne',
    tel:'Téléphone',telph:'+212 6xx xxx xxx',quartier:'Quartier',quartph:'Quartier / Zone',
    spiritual:'Parcours spirituel',
    baptise:'Êtes-vous déjà baptisé(e) ?',bapY:'Oui',bapN:'Non',
    service:'Servez-vous déjà dans votre pays ou au Maroc ?',srvY:'Oui',srvN:'Non',
    serviceLequel:'Si oui, lequel ?',servicePh:'ex: Chorale, Enseignement, Intercession...',
    sejour:'Séjour au Maroc',
    duree:'Combien de temps pensez-vous rester au Maroc ?',dur3:'3 ans',dur5:'5 ans',durA:'Autre',
    dureeAutre:'Précisez la durée',dureePh:'ex: 6 mois, 1 an...',
    raison:'Raison de votre arrivée au Maroc',rEt:'Études',rTr:'Travail',rEn:'Entrepreneuriat',rAu:'Autre',
    ecole:'Quelle école / université ?',ecolePh:"Nom de l'établissement",
    autreRaison:'Précisez',autreRaisonPh:'Votre raison...',
    notes:'Notes',notesPh:'Partagez librement...',notesLabel:'Besoins de prière / Message pour l\'équipe pastorale',
    submit:'Enregistrer ma fiche',
    req:'Champ requis',reqS:'Veuillez répondre',
    successTitle:'Merci !',successSub:'Votre fiche a bien été enregistrée.\nBienvenue parmi nous 🙏',
    newForm:'Remplir une nouvelle fiche'
  },
  en:{
    name:'Evangelical Church in Morocco',sub:'Parish of Fès',
    welcome:"The Evangelical Church in Morocco, Parish of Fès, warmly welcomes you.\nTo better serve you and accompany you in your spiritual growth,\nplease fill in this form.",
    date:'Today\'s date',identity:'Identity',nom:'Last Name',prenom:'First Name',
    sexe:'Gender',sx0:'— Choose —',sx1:'Male',sx2:'Female',
    nationalite:'Nationality',natph:'e.g. Nigerian',
    tel:'Phone',telph:'+212 6xx xxx xxx',quartier:'Neighborhood',quartph:'Area / District',
    spiritual:'Spiritual journey',
    baptise:'Have you already been baptized?',bapY:'Yes',bapN:'No',
    service:'Are you already serving in your country or in Morocco?',srvY:'Yes',srvN:'No',
    serviceLequel:'If yes, which one?',servicePh:'e.g. Choir, Teaching, Intercession...',
    sejour:'Stay in Morocco',
    duree:'How long do you plan to stay in Morocco?',dur3:'3 years',dur5:'5 years',durA:'Other',
    dureeAutre:'Specify the duration',dureePh:'e.g. 6 months, 1 year...',
    raison:'Reason for coming to Morocco',rEt:'Studies',rTr:'Work',rEn:'Entrepreneurship',rAu:'Other',
    ecole:'Which school / university?',ecolePh:'Name of institution',
    autreRaison:'Specify',autreRaisonPh:'Your reason...',
    notes:'Notes',notesPh:'Share freely...',notesLabel:'Prayer needs / Message for the pastoral team',
    submit:'Submit my form',
    req:'Required field',reqS:'Please respond',
    successTitle:'Thank you!',successSub:'Your form has been recorded.\nWelcome among us 🙏',
    newForm:'Fill in a new form'
  },
  es:{
    name:'Iglesia Evangélica en Marruecos',sub:'Parroquia de Fez',
    welcome:"La Iglesia Evangélica en Marruecos, Parroquia de Fez, te da la bienvenida calurosamente.\nPara servirte mejor y acompañarte en tu crecimiento espiritual,\npor favor rellena esta ficha.",
    date:'Fecha de hoy',identity:'Identidad',nom:'Apellido',prenom:'Nombre',
    sexe:'Sexo',sx0:'— Elegir —',sx1:'Hombre',sx2:'Mujer',
    nationalite:'Nacionalidad',natph:'ej: Colombiana',
    tel:'Teléfono',telph:'+212 6xx xxx xxx',quartier:'Barrio',quartph:'Barrio / Zona',
    spiritual:'Recorrido espiritual',
    baptise:'¿Ya está bautizado(a)?',bapY:'Sí',bapN:'No',
    service:'¿Ya sirve en su país o en Marruecos?',srvY:'Sí',srvN:'No',
    serviceLequel:'Si es así, ¿cuál?',servicePh:'ej: Coro, Enseñanza, Intercesión...',
    sejour:'Estancia en Marruecos',
    duree:'¿Cuánto tiempo piensa quedarse en Marruecos?',dur3:'3 años',dur5:'5 años',durA:'Otro',
    dureeAutre:'Especifique la duración',dureePh:'ej: 6 meses, 1 año...',
    raison:'Razón de su llegada a Marruecos',rEt:'Estudios',rTr:'Trabajo',rEn:'Emprendimiento',rAu:'Otro',
    ecole:'¿Qué escuela / universidad?',ecolePh:'Nombre del establecimiento',
    autreRaison:'Especifique',autreRaisonPh:'Su razón...',
    notes:'Notas',notesPh:'Comparte libremente...',notesLabel:'Necesidades de oración / Mensaje para el equipo pastoral',
    submit:'Guardar mi ficha',
    req:'Campo requerido',reqS:'Por favor responda',
    successTitle:'¡Gracias!',successSub:'Su ficha ha sido registrada.\nBienvenido entre nosotros 🙏',
    newForm:'Llenar una nueva ficha'
  },
  pt:{
    name:'Igreja Evangélica em Marrocos',sub:'Paróquia de Fez',
    welcome:"A Igreja Evangélica em Marrocos, Paróquia de Fez, acolhe-o calorosamente.\nPara melhor servi-lo e acompanhá-lo no seu crescimento espiritual,\npor favor preencha esta ficha.",
    date:'Data de hoje',identity:'Identidade',nom:'Apelido',prenom:'Nome próprio',
    sexe:'Sexo',sx0:'— Escolher —',sx1:'Homem',sx2:'Mulher',
    nationalite:'Nacionalidade',natph:'ex: Angolana',
    tel:'Telefone',telph:'+212 6xx xxx xxx',quartier:'Bairro',quartph:'Bairro / Zona',
    spiritual:'Percurso espiritual',
    baptise:'Já foi batizado(a)?',bapY:'Sim',bapN:'Não',
    service:'Já serve no seu país ou em Marrocos?',srvY:'Sim',srvN:'Não',
    serviceLequel:'Se sim, qual?',servicePh:'ex: Coral, Ensino, Intercessão...',
    sejour:'Estadia em Marrocos',
    duree:'Quanto tempo pensa ficar em Marrocos?',dur3:'3 anos',dur5:'5 anos',durA:'Outro',
    dureeAutre:'Especifique a duração',dureePh:'ex: 6 meses, 1 ano...',
    raison:'Razão da sua chegada a Marrocos',rEt:'Estudos',rTr:'Trabalho',rEn:'Empreendedorismo',rAu:'Outro',
    ecole:'Qual escola / universidade?',ecolePh:'Nome do estabelecimento',
    autreRaison:'Especifique',autreRaisonPh:'A sua razão...',
    notes:'Notas',notesPh:'Partilhe livremente...',notesLabel:'Pedidos de oração / Mensagem para a equipa pastoral',
    submit:'Guardar a minha ficha',
    req:'Campo obrigatório',reqS:'Por favor responda',
    successTitle:'Obrigado!',successSub:'A sua ficha foi registada.\nBem-vindo entre nós 🙏',
    newForm:'Preencher uma nova ficha'
  },
  ar:{
    name:'الكنيسة الإنجيلية في المغرب',sub:'رعية فاس',
    welcome:"الكنيسة الإنجيلية في المغرب، رعية فاس، ترحب بكم بحرارة.\nلخدمتكم بشكل أفضل ومرافقتكم في نموكم الروحي،\nيرجى ملء هذه البطاقة.",
    date:'تاريخ اليوم',identity:'الهوية',nom:'اللقب',prenom:'الاسم',
    sexe:'الجنس',sx0:'— اختر —',sx1:'ذكر',sx2:'أنثى',
    nationalite:'الجنسية',natph:'مثال: سنغالية',
    tel:'الهاتف',telph:'+212 6xx xxx xxx',quartier:'الحي',quartph:'الحي / المنطقة',
    spiritual:'المسار الروحي',
    baptise:'هل تعمدت من قبل؟',bapY:'نعم',bapN:'لا',
    service:'هل تخدم في بلدك أو في المغرب؟',srvY:'نعم',srvN:'لا',
    serviceLequel:'إذا نعم، في ماذا؟',servicePh:'مثال: الجوقة، التعليم، الشفاعة...',
    sejour:'الإقامة في المغرب',
    duree:'كم من الوقت تنوي البقاء في المغرب؟',dur3:'3 سنوات',dur5:'5 سنوات',durA:'أخرى',
    dureeAutre:'حدد المدة',dureePh:'مثال: 6 أشهر، سنة...',
    raison:'سبب قدومك إلى المغرب',rEt:'الدراسة',rTr:'العمل',rEn:'ريادة الأعمال',rAu:'أخرى',
    ecole:'في أي مدرسة / جامعة؟',ecolePh:'اسم المؤسسة',
    autreRaison:'حدد',autreRaisonPh:'سببك...',
    notes:'ملاحظات',notesPh:'شارك بحرية...',notesLabel:'طلبات صلاة / رسالة للفريق الرعوي',
    submit:'تسجيل بطاقتي',
    req:'حقل مطلوب',reqS:'يرجى الإجابة',
    successTitle:'شكراً!',successSub:'تم تسجيل بطاقتك.\nمرحباً بك بيننا 🙏',
    newForm:'ملء بطاقة جديدة'
  },
  ln:{
    name:'Lingomba ya Évangile na Maroc',sub:'Paroisse ya Fès',
    welcome:"Lingomba ya Évangile na Maroc, Paroisse ya Fès, eyamboli yo na motema nyonso.\nMpo na kosalela yo malamu mpenza na kokamba yo na bokoli ya molimo,\nsambelaká carte oyo.",
    date:'Mokolo ya lelo',identity:'Kombo na yo',nom:'Nkombo ya libota',prenom:'Nkombo na yo',
    sexe:'Ndenge',sx0:'— Pona —',sx1:'Mobali',sx2:'Mwasi',
    nationalite:'Mboka ya yo',natph:'ndakisa: Congolaise',
    tel:'Telefone',telph:'+212 6xx xxx xxx',quartier:'Quartier',quartph:'Quartier / Zone',
    spiritual:'Nzela ya molimo',
    baptise:'Ozwa bateme nanu?',bapY:'Iyo',bapN:'Te',
    service:'Osalela nanu na mboka na yo to na Maroc?',srvY:'Iyo',srvN:'Te',
    serviceLequel:'Soki iyo, nini?',servicePh:'ndakisa: Chorale, Mateya, Bosenga...',
    sejour:'Kovanda na Maroc',
    duree:'Ntango nini okanisi kovanda na Maroc?',dur3:'Bambula 3',dur5:'Bambula 5',durA:'Mosusu',
    dureeAutre:'Lobá ntango yango',dureePh:'ndakisa: Sanza 6, Mbula moko...',
    raison:'Likambo ya koya na Maroc',rEt:'Koyekola',rTr:'Mosala',rEn:'Bizinesi',rAu:'Mosusu',
    ecole:'Kelasi / université nini?',ecolePh:'Nkombo ya kelasi',
    autreRaison:'Lobá mpenza',autreRaisonPh:'Likambo na yo...',
    notes:'Makanisi',notesPh:'Lobá na motema oyo...',notesLabel:'Bosenga ya libondeli / Sango mpo na bato ya mposo',
    submit:'Bomba carte na ngai',
    req:'Esengeli',reqS:'Jafu, tika eyano',
    successTitle:'Matondo!',successSub:'Carte na yo ezwami malamu.\nBoyei malamu kati na biso 🙏',
    newForm:'Samba carte mopé'
  }
};

let lang = 'fr';

function setLang(l) {
  lang = l;
  document.querySelectorAll('.lang-btn').forEach(b => b.classList.remove('active'));
  event.target.classList.add('active');
  const t = T[l];
  const isAr = l === 'ar';
  document.documentElement.lang = l;
  document.documentElement.dir = isAr ? 'rtl' : 'ltr';

  // Header
  document.getElementById('txt-name').textContent = t.name;
  document.getElementById('txt-sub').textContent = t.sub;
  document.getElementById('txt-welcome').innerHTML = t.welcome.replace(/\n/g,'<br>');

  // Labels
  document.getElementById('lbl-date').innerHTML = t.date + ' <span class="req">*</span>';
  document.getElementById('ttl-identity').textContent = t.identity;
  document.getElementById('lbl-nom').innerHTML = t.nom + ' <span class="req">*</span>';
  document.getElementById('lbl-prenom').innerHTML = t.prenom + ' <span class="req">*</span>';
  document.getElementById('lbl-sexe').innerHTML = t.sexe + ' <span class="req">*</span>';
  document.getElementById('o-sx0').textContent = t.sx0;
  document.getElementById('o-sx1').textContent = t.sx1;
  document.getElementById('o-sx2').textContent = t.sx2;
  document.getElementById('lbl-nationalite').innerHTML = t.nationalite + ' <span class="req">*</span>';
  document.getElementById('inp-nationalite').placeholder = t.natph;
  document.getElementById('lbl-tel').innerHTML = t.tel + ' <span class="req">*</span>';
  document.getElementById('inp-tel').placeholder = t.telph;
  document.getElementById('lbl-quartier').textContent = t.quartier;
  document.getElementById('inp-quartier').placeholder = t.quartph;
  document.getElementById('inp-nom').placeholder = t.nom;
  document.getElementById('inp-prenom').placeholder = t.prenom;

  // Spiritual
  document.getElementById('ttl-spiritual').textContent = t.spiritual;
  document.getElementById('lbl-baptise').innerHTML = t.baptise + ' <span class="req">*</span>';
  document.getElementById('o-bap-y').textContent = t.bapY;
  document.getElementById('o-bap-n').textContent = t.bapN;
  document.getElementById('lbl-service').innerHTML = t.service + ' <span class="req">*</span>';
  document.getElementById('o-srv-y').textContent = t.srvY;
  document.getElementById('o-srv-n').textContent = t.srvN;
  document.getElementById('lbl-serviceLequel').textContent = t.serviceLequel;
  document.getElementById('inp-serviceLequel').placeholder = t.servicePh;

  // Séjour
  document.getElementById('ttl-sejour').textContent = t.sejour;
  document.getElementById('lbl-duree').innerHTML = t.duree + ' <span class="req">*</span>';
  document.getElementById('o-dur-3').textContent = t.dur3;
  document.getElementById('o-dur-5').textContent = t.dur5;
  document.getElementById('o-dur-a').textContent = t.durA;
  document.getElementById('lbl-dureeAutre').textContent = t.dureeAutre;
  document.getElementById('inp-dureeAutre').placeholder = t.dureePh;
  document.getElementById('lbl-raison').innerHTML = t.raison + ' <span class="req">*</span>';
  document.getElementById('o-r-et').textContent = t.rEt;
  document.getElementById('o-r-tr').textContent = t.rTr;
  document.getElementById('o-r-en').textContent = t.rEn;
  document.getElementById('o-r-au').textContent = t.rAu;
  document.getElementById('lbl-ecole').textContent = t.ecole;
  document.getElementById('inp-ecole').placeholder = t.ecolePh;
  document.getElementById('lbl-autreRaison').textContent = t.autreRaison;
  document.getElementById('inp-autreRaison').placeholder = t.autreRaisonPh;

  // Notes
  document.getElementById('ttl-notes').textContent = t.notes;
  document.getElementById('lbl-notes').textContent = t.notesLabel;
  document.getElementById('inp-notes').placeholder = t.notesPh;

  // Submit
  document.getElementById('btn-txt').textContent = t.submit;

  // Errors
  document.getElementById('err-date').textContent = t.req;
  document.getElementById('err-nom').textContent = t.req;
  document.getElementById('err-prenom').textContent = t.req;
  document.getElementById('err-sexe').textContent = t.req;
  document.getElementById('err-nationalite').textContent = t.req;
  document.getElementById('err-tel').textContent = t.req;
  document.getElementById('err-baptise').textContent = t.reqS;
  document.getElementById('err-service').textContent = t.reqS;
  document.getElementById('err-duree').textContent = t.reqS;
  document.getElementById('err-raison').textContent = t.reqS;

  // Success
  document.getElementById('success-title').textContent = t.successTitle;
  document.getElementById('success-sub').innerHTML = t.successSub.replace(/\n/g,'<br>');
  document.getElementById('btn-new').textContent = t.newForm;
}

// ── SET TODAY ──
(function(){
  const today = new Date();
  const y = today.getFullYear();
  const m = String(today.getMonth()+1).padStart(2,'0');
  const d = String(today.getDate()).padStart(2,'0');
  document.getElementById('inp-date').value = y+'-'+m+'-'+d;
})();

// ── RADIO SELECT ──
function sel(el, name) {
  document.querySelectorAll('[name="'+name+'"]').forEach(r => {
    r.closest('.radio-label').classList.remove('selected');
  });
  el.classList.add('selected');
  el.querySelector('input').checked = true;
  // clear validation error
  const f = document.getElementById('f-'+name) || document.getElementById('f-'+name.replace(/([A-Z])/g,'-$1').toLowerCase());
  if(f) f.classList.remove('invalid');
}

// ── SHOW/HIDE CONDITIONAL ──
function show(id){ document.getElementById(id).classList.add('show'); }
function hide(id){ document.getElementById(id).classList.remove('show'); }

// ── VALIDATION ──
function validate() {
  let ok = true;
  const t = T[lang];

  function req(fieldId, inputId) {
    const f = document.getElementById(fieldId);
    const v = document.getElementById(inputId).value.trim();
    if(!v){ f.classList.add('invalid'); ok = false; }
    else { f.classList.remove('invalid'); }
  }

  function reqRadio(fieldId, name) {
    const f = document.getElementById(fieldId);
    const checked = document.querySelector('[name="'+name+'"]:checked');
    if(!checked){ f.classList.add('invalid'); ok = false; }
    else { f.classList.remove('invalid'); }
  }

  req('f-date','inp-date');
  req('f-nom','inp-nom');
  req('f-prenom','inp-prenom');
  req('f-sexe','inp-sexe');
  req('f-nationalite','inp-nationalite');
  req('f-tel','inp-tel');
  reqRadio('f-baptise','baptise');
  reqRadio('f-service','service');
  reqRadio('f-duree','duree');
  reqRadio('f-raison','raison');

  return ok;
}

// ── SUBMIT ──
document.getElementById('main-form').addEventListener('submit', function(e){
  e.preventDefault();
  if(!validate()) {
    // Scroll to first error
    const firstErr = document.querySelector('.field.invalid');
    if(firstErr) firstErr.scrollIntoView({behavior:'smooth', block:'center'});
    return;
  }

  const btn = document.getElementById('btn-submit');
  btn.classList.add('loading');
  document.getElementById('btn-txt').textContent = '...';

  // Collect data
  const data = {
    langue: lang,
    date: document.getElementById('inp-date').value,
    nom: document.getElementById('inp-nom').value.trim(),
    prenom: document.getElementById('inp-prenom').value.trim(),
    sexe: document.getElementById('inp-sexe').value,
    nationalite: document.getElementById('inp-nationalite').value.trim(),
    telephone: document.getElementById('inp-tel').value.trim(),
    quartier: document.getElementById('inp-quartier').value.trim(),
    baptise: document.querySelector('[name="baptise"]:checked')?.value || '',
    service: document.querySelector('[name="service"]:checked')?.value || '',
    serviceLequel: document.getElementById('inp-serviceLequel').value.trim(),
    duree: document.querySelector('[name="duree"]:checked')?.value || '',
    dureeAutre: document.getElementById('inp-dureeAutre').value.trim(),
    raison: document.querySelector('[name="raison"]:checked')?.value || '',
    ecole: document.getElementById('inp-ecole').value.trim(),
    autreRaison: document.getElementById('inp-autreRaison').value.trim(),
    notes: document.getElementById('inp-notes').value.trim()
  };

  console.log('Fiche EEEM Fès:', data);

  // Simulate short save delay then show success
  setTimeout(function(){
    btn.classList.remove('loading');
    const t = T[lang];
    document.getElementById('btn-txt').textContent = t.submit;
    document.getElementById('success-screen').classList.add('show');
  }, 800);
});

// ── RESET ──
function resetForm() {
  document.getElementById('success-screen').classList.remove('show');
  document.getElementById('main-form').reset();
  document.querySelectorAll('.radio-label').forEach(l => l.classList.remove('selected'));
  document.querySelectorAll('.conditional').forEach(c => c.classList.remove('show'));
  document.querySelectorAll('.field.invalid').forEach(f => f.classList.remove('invalid'));
  // Reset date to today
  const today = new Date();
  const y = today.getFullYear();
  const m = String(today.getMonth()+1).padStart(2,'0');
  const d = String(today.getDate()).padStart(2,'0');
  document.getElementById('inp-date').value = y+'-'+m+'-'+d;
  window.scrollTo({top:0, behavior:'smooth'});
}
</script>
</body>
</html>
