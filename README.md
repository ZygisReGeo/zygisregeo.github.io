<html lang="lt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prašome išsirinkti žemėlapį</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    /* Baziniai stiliai kūnui */
    body {
      margin: 0;
      padding: 0;
      font-family: 'Inter', sans-serif; /* Naudojamas Inter šriftas */
      color: #f0f0f0; /* Šviesi teksto spalva */
      min-height: 100vh; /* Užtikrina, kad fonas užimtų visą aukštį */
      display: flex;
      flex-direction: column;
      justify-content: flex-start; /* Turinio lygiavimas viršuje */
      align-items: flex-start; /* Elementų lygiavimas kairėje */
      /* Foninio paveikslėlio nustatymai - animuota Pakistano vėliava */
      background-image: url('https://www.animatedimages.org/data/media/1667/animated-world-globe-image-0012.gif'); /* Animuotas Žemės bei mėnulio vaizdas */
      background-size: cover; /* Padengia visą foną */
      background-position: center; /* Centruoja paveikslėlį */
      background-repeat: no-repeat; /* Nepakartoja paveikslėlio */
      background-attachment: fixed; /* Paveikslėlis fiksuotas slenkant puslapį */
    }

    /* Navigacijos juostos stiliai */
    nav {
      width: 100%;
      background-color: rgba(0, 0, 0, 0.9); /* Tamsus, šiek tiek permatomas fonas */
      padding: 15px 5%; /* Vidiniai tarpai */
      display: flex;
      justify-content: space-between; /* Elementai išdėstomi kraštuose */
      align-items: center;
      position: sticky; /* Navigacija lieka viršuje slenkant */
      top: 0;
      z-index: 1000; /* Užtikrina, kad navigacija būtų virš kitų elementų */
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5); /* Šešėlis */
      box-sizing: border-box;
    }

    nav a {
      color: #00ccff; /* Nuorodų spalva */
      text-decoration: none;
      font-size: 1.1em;
      padding: 8px 15px;
      border-radius: 5px;
      transition: background-color 0.3s ease, color 0.3s ease;
    }

    nav a:hover {
      background-color: #00ccff;
      color: #000;
    }

    /* Konteinerio stiliai */
    .container {
      background-color: rgba(0, 0, 0, 0.2); /* Permatomas fonas */
      padding: 40px 60px; /* Vidiniai tarpai */
      max-width: 960px; /* Maksimalus plotis */
      width: 90%; /* Prisitaiko prie ekrano pločio */
      border-radius: 15px; /* Suapvalinti kampai */
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5); /* Šešėlis */
      text-align: center;
      box-sizing: border-box; /* Įskaičiuoja padding ir border į elemento plotį/aukštį */
      margin-top: 50px; /* Viršutinė paraštė, kad turinys būtų žemiau */
      margin-left: 5%; /* Lygiavimas kairėje su 5% parašte */
      margin-right: auto; /* Likusią erdvę stumia į dešinę */
      margin-bottom: 50px; /* Apatinė paraštė */
    }

    /* Antraštės stiliai */
    h1 {
      text-align: center; /* Centruoja tekstą */
      margin-bottom: 40px; /* Apatinė paraštė */
      font-size: 2.5em; /* Didesnis šrifto dydis */
      color: #00ccff; /* Ryškesnė antraštės spalva */
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3); /* Teksto šešėlis */
    }

    /* Svetainės pristatymo skiltis */
    .section-intro {
      background-color: rgba(30, 30, 30, 0.8); /* Tamsesnis fonas */
      padding: 25px 35px;
      border-radius: 10px;
      margin-bottom: 40px; /* Tarpas po šia skiltimi */
      text-align: left;
      line-height: 1.6;
      font-size: 1.1em;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
    }

    /* Informacinių skilčių konteineris */
    .info-sections {
      display: flex;
      flex-direction: column; /* Kortelės viena po kitos vertikaliai */
      gap: 30px; /* Tarpas tarp informacinių kortelių */
      margin-top: 40px; /* Tarpas virš šios skilties */
      margin-bottom: 40px; /* Tarpas po šia skiltimi */
    }

    /* Kiekvienos informacinės kortelės stilius */
    .info-card {
      background-color: rgba(30, 30, 30, 0.3); /* Tamsesnis fonas */
      border-radius: 12px;
      box-shadow: 0 6px 15px rgba(0, 0, 0, 0); /* Šešėlis panaikintas */
      overflow: hidden;
      display: flex;
      flex-direction: row; /* Paveikslėlis ir tekstas šalia */
      align-items: flex-start; /* Lygiavimas viršuje */
      text-align: left;
      color: #f0f0f0;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .info-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0, 204, 255, 0.3);
    }

    .info-card-img {
      width: 200px; /* Fiksuotas paveikslėlio plotis */
      height: 150px; /* Fiksuotas paveikslėlio aukštis */
      object-fit: cover;
      flex-shrink: 0;
      border-right: 2px solid #00ccff;
    }

    .info-card-content {
      padding: 20px;
      line-height: 1.5;
      font-size: 1em;
    }

    /* Nuorodų konteineris, išdėstytas kaip vertikalus kortelių sąrašas */
    .links-list {
      display: flex;
      flex-direction: column; /* Kortelės viena po kitos vertikaliai */
      gap: 25px; /* Tarpas tarp kortelių */
      margin-top: 30px;
    }

    /* Kiekvienos žemėlapio kortelės stilius */
    .map-card {
      background-color: transparent; /* Fonas panaikintas / permatomas */
      border-radius: 12px; /* Suapvalinti kampai */
      border: 10px solid #006400; /* 10px storio tamsiai žalias rėmelis */
      box-shadow: none; /* Šešėlis panaikintas */
      overflow: hidden; /* Paslepia perteklinį turinį, pvz., suapvalintus kampus paveikslėliui */
      transition: transform 0.3s ease, box-shadow 0.3s ease; /* Sklandūs perėjimai */
      display: flex; /* Naudojamas flexbox vidiniam išdėstymui (paveikslėlis ir turinys šalia) */
      flex-direction: row; /* Paveikslėlis ir turinys šalia */
      align-items: center; /* Vertikaliai lygina elementus kortelėje */
      text-decoration: none; /* Pašalina pabraukimą iš kortelės, jei ji yra nuoroda */
      color: #f0f0f0; /* Teksto spalva kortelėje */
    }

    .map-card:hover {
      transform: translateY(-5px); /* Šiek tiek pakelia kortelę užvedus pelę */
      box-shadow: none; /* Šešėlis panaikintas užvedus pelę */
    }

    /* Miniatiūros paveikslėlio stilius */
    .map-thumbnail {
      width: 250px; /* Fiksuotas miniatiūros plotis */
      height: 150px; /* Fiksuotas miniatiūros aukštis */
      object-fit: cover; /* Užtikrina, kad paveikslėlis užpildytų visą vietą */
      flex-shrink: 0; /* Neleidžia miniatiūrai susitraukti */
      border-right: 2px solid #00ccff; /* Atskyrimo linija */
    }

    /* Turinio sritis kortelės viduje */
    .map-card-content {
      padding: 20px;
      text-align: left; /* Teksto lygiavimas kairėje */
      flex-grow: 1; /* Leidžia turiniui užimti likusią vietą */
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    /* Nuorodos tekstas kortelės viduje */
    .map-card-content a {
      color: #fff; /* Baltas teksto spalva */
      text-decoration: none; /* Pašalina pabraukimą */
      font-size: 1.3em; /* Didesnis šrifto dydis nuorodai */
      transition: color 0.3s ease;
      display: flex; /* Leidžia piktogramai ir tekstui būti vienoje eilutėje */
      align-items: center; /* Vertikaliai centruoja piktogramą ir tekstą */
      justify-content: flex-start; /* Turinio lygiavimas kairėje */
    }

    .map-card-content a:hover {
      color: #00ccff; /* Mėlyna spalva užvedus pelę */
    }

    /* Font Awesome piktogramos stiliai kortelės viduje */
    .map-card-content .fas {
      margin-right: 12px; /* Tarpas tarp piktogramos ir teksto */
      font-size: 1.2em; /* Piktogramos dydis */
      color: #00ccff; /* Piktogramos spalva */
    }

    /* Poraštės stiliai */
    footer {
      width: 100%;
      background-color: rgba(0, 0, 0, 0.8); /* Tamsesnis fonas poraštei */
      color: #f0f0f0; /* Šviesi teksto spalva */
      padding: 20px 0;
      text-align: center;
      margin-top: auto; /* Stumia poraštę į apačią */
      border-top: 2px solid #00ccff; /* Viršutinis rėmelis atskyrimui */
      box-sizing: border-box;
    }

    footer p {
      margin: 5px 0;
      font-size: 0.9em;
    }

    /* Prisitaikymas prie mažesnių ekranų */
    @media (max-width: 768px) {
      .container {
        padding: 30px;
        margin-left: auto; /* Centruojama mažesniuose ekranuose */
        margin-right: auto; /* Centruojama mažesniuose ekranuose */
        width: 95%; /* Platesnis plotis mažesniuose ekranuose */
      }

      h1 {
        font-size: 2em;
      }

      .section-intro, .info-card {
        padding: 20px;
      }

      .info-card {
        flex-direction: column; /* Paveikslėlis ir turinys vienas po kito vertikaliai mažuose ekranuose */
        align-items: center;
      }

      .info-card-img {
        width: 100%;
        height: 180px;
        border-right: none;
        border-bottom: 2px solid #00ccff;
      }

      .info-card-content {
        padding: 15px;
        text-align: center;
      }

      .map-card {
        flex-direction: column; /* Paveikslėlis ir turinys vienas po kitos vertikaliai mažuose ekranuose */
        align-items: center;
      }

      .map-thumbnail {
        width: 100%; /* Miniatiūra užima visą plotį */
        height: 180px; /* Paveikslėlio aukštis geresniam rodymui */
        border-right: none; /* Pašalinamas dešinysis rėmelis */
        border-bottom: 2px solid #00ccff; /* Pridedamas apatinis rėmelis */
      }

      .map-card-content {
        padding: 15px;
        text-align: center; /* Tekstas centruojamas mažuose ekranuose */
      }

      .map-card-content a {
        font-size: 1.1em;
        justify-content: center; /* Turinys centruojamas mažuose ekranuose */
      }
    }

    @media (max-width: 480px) {
      .container {
        padding: 20px;
        margin: 20px auto;
      }

      h1 {
        font-size: 1.8em;
        margin-bottom: 20px;
      }

      .info-card-img {
        height: 150px;
      }

      .map-thumbnail {
        height: 150px;
      }

      .map-card-content a {
        font-size: 1em;
      }
    }
  </style>
</head>
<body>
  <nav>
    <a href="#top">Pagrindinis puslapis</a>
    <a href="https://zygisregeo.github.io/Kontaktai.html" target="_blank">Kontaktai</a>
  </nav>

  <div class="container">
    <h1 id="top">Mano internetinis viešas turinys</h1>

    <div class="section-intro">
      <p>Sveiki atvykę į mano puslapį, skirtą dalintis įvairiais žemėlapių projektais ir geografinės informacijos sistemų (GIS) aplikacijomis. Čia rasite mano praktinius darbus, atliktus studijų metu, ir kitus įdomius projektus, susijusius su kartografija ir erdvinių duomenų analize.</p>
    </div>

    <div class="info-sections">
      <div class="info-card">
        <div class="info-card-content">
          <p>Ši svetainė yra naudojama tik atsiskaityti studijų metu atliktiem darbam ir bus apleista, kai viskas bus atsiskaityta.</p>
        </div>
      </div>

      <div class="info-card">
        <div class="info-card-content">
          <p>Svarbios papildomos informacijos klausti trumpąją SMS žinute</p>
        </div>
      </div>
    </div>

    <div class="links-list">
      <div class="map-card">
        <img src="https://i.ibb.co/VYPHRYv4/img1.png" class="map-thumbnail">
        <div class="map-card-content">
          <a href="https://zygisregeo.github.io/1_praktinis/map_1.html" target="_blank"><i class="fas fa-map"></i> 1 Žemėlapis</a>
        </div>
      </div>

      <div class="map-card">
        <img src="https://i.ibb.co/dst0rrCN/img2.png" class="map-thumbnail">
        <div class="map-card-content">
          <a href="https://zygisregeo.github.io/1_praktinis/map_2.html" target="_blank"><i class="fas fa-map"></i> 2 Žemėlapis</a>
        </div>
      </div>

      <div class="map-card">
        <img src="https://i.ibb.co/zW6NCM8k/img3.png" class="map-thumbnail">
        <div class="map-card-content">
          <a href="https://zygisregeo.github.io/1_praktinis/map_3.html" target="_blank"><i class="fas fa-map"></i> 3 Žemėlapis</a>
        </div>
      </div>

      <div class="map-card">
        <img src="https://i.ibb.co/DPfbPNLK/img4.png" class="map-thumbnail">
        <div class="map-card-content">
          <a href="https://zygisregeo.github.io/2_praktinis/zhemelapyzas.html" target="_blank"><i class="fas fa-map"></i> Geoportal žemėlapis</a>
        </div>
      </div>

      <div class="map-card">
        <img src="https://i.ibb.co/jk8M7DgX/img5.png" class="map-thumbnail">
        <div class="map-card-content">
          <a href="https://zygisregeo.github.io/3_praktinis/appsas.html" target="_blank"><i class="fas fa-map"></i> ArcGIS aplikacija</a>
        </div>
      </div>
    </div>
  </div>
  <footer>
    <p><strong>Kontaktinė informacija</strong></p>
    <p>Vardas: Žygimantas Remeika</p>
    <p>Adresas: T. Kosciuškos g. 1</p>
    <p>Telefonas: +370 615 50116</p>
    <p>Sukūrimo data: 2025-05-31</p>
  </footer>
</body>
</html>