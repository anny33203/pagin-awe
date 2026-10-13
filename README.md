
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Flora de Minecraft | Enciclopedia</title>
  <meta name="description" content="Enciclopedia botánica de Minecraft con flores, categorías, búsqueda y diseño mágico." />
  <style>
    :root {
      --bg-1: #f5fbf7;
      --bg-2: #ebf6ff;
      --card: rgba(255, 255, 255, 0.78);
      --card-strong: #ffffff;
      --text: #0f172a;
      --muted: #516074;
      --green: #67c98f;
      --green-deep: #2d8a62;
      --purple: #af77d9;
      --purple-deep: #7f4fb8;
      --shadow: 0 16px 40px rgba(15, 23, 42, 0.08);
      --radius-xl: 24px;
      --radius-lg: 18px;
      --radius-md: 12px;
      --radius-sm: 10px;
      --max-width: 1180px;
    }

    * { box-sizing: border-box; }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: Inter, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background:
        radial-gradient(circle at top left, rgba(175, 119, 217, 0.10), transparent 30%),
        radial-gradient(circle at top right, rgba(103, 201, 143, 0.12), transparent 30%),
        linear-gradient(180deg, var(--bg-1), var(--bg-2));
      color: var(--text);
      line-height: 1.6;
    }

    img {
      max-width: 100%;
      display: block;
    }

    a {
      color: inherit;
    }

    button, input {
      font: inherit;
    }

    .sr-only {
      position: absolute;
      width: 1px;
      height: 1px;
      padding: 0;
      margin: -1px;
      overflow: hidden;
      clip: rect(0, 0, 0, 0);
      white-space: nowrap;
      border: 0;
    }

    .container {
      width: min(var(--max-width), calc(100% - 32px));
      margin: 0 auto;
    }

    .site-header {
      position: sticky;
      top: 0;
      z-index: 10;
      backdrop-filter: blur(10px);
      background: rgba(245, 251, 247, 0.7);
      border-bottom: 1px solid rgba(15, 23, 42, 0.04);
    }

    .header-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
      min-height: 74px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      font-weight: 800;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      color: var(--green-deep);
      font-size: 0.78rem;
    }

    .brand-mark {
      width: 42px;
      height: 42px;
      display: grid;
      place-items: center;
      border-radius: 14px;
      background: linear-gradient(135deg, rgba(103, 201, 143, 0.18), rgba(175, 119, 217, 0.18));
      box-shadow: 0 8px 18px rgba(103, 201, 143, 0.18);
      font-size: 1.2rem;
    }

    .nav {
      display: flex;
      align-items: center;
      gap: 18px;
      flex-wrap: wrap;
    }

    .nav a {
      text-decoration: none;
      color: var(--muted);
      font-weight: 600;
      font-size: 0.96rem;
      transition: color 0.2s ease;
    }

    .nav a:hover,
    .nav a:focus-visible {
      color: var(--green-deep);
      outline: none;
    }

    .hero {
      padding: 42px 0 24px;
    }

    .hero-panel {
      position: relative;
      overflow: hidden;
      border-radius: var(--radius-xl);
      background:
        linear-gradient(135deg, rgba(255,255,255,0.7), rgba(255,255,255,0.55)),
        radial-gradient(circle at 20% 20%, rgba(103, 201, 143, 0.18), transparent 35%);
      border: 1px solid rgba(15, 23, 42, 0.04);
      box-shadow: var(--shadow);
      padding: 32px 28px;
      min-height: 360px;
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 18px;
      align-items: center;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 8px 12px;
      border-radius: 999px;
      background: linear-gradient(90deg, var(--green), var(--purple));
      color: #fff;
      font-size: 0.72rem;
      font-weight: 800;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      margin-bottom: 18px;
      box-shadow: 0 12px 30px rgba(175, 119, 217, 0.18);
    }

    .hero-copy h1 {
      margin: 0 0 16px;
      font-size: clamp(2.2rem, 3vw, 4rem);
      line-height: 1.05;
      letter-spacing: -0.05em;
      color: #0a2b22;
    }

    .hero-copy p {
      margin: 0;
      max-width: 640px;
      font-size: 1.08rem;
      color: var(--muted);
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 28px;
    }

    .btn {
      appearance: none;
      border: none;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 12px 18px;
      border-radius: 999px;
      font-weight: 700;
      cursor: pointer;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .btn:hover,
    .btn:focus-visible {
      transform: translateY(-2px);
      outline: none;
    }

    .btn-primary {
      background: linear-gradient(90deg, var(--green), var(--purple));
      color: white;
      box-shadow: 0 18px 28px rgba(103, 201, 143, 0.22);
    }

    .btn-secondary {
      background: rgba(255,255,255,0.6);
      border: 1px solid rgba(15, 23, 42, 0.06);
      color: var(--text);
    }

    .hero-visual {
      position: relative;
      display: grid;
      place-items: center;
      min-height: 280px;
    }

    .flower-orb {
      position: relative;
      width: min(260px, 70vw);
      aspect-ratio: 1;
      border-radius: 50%;
      background:
        radial-gradient(circle at 50% 38%, rgba(255,255,255,0.9), transparent 18%),
        radial-gradient(circle at 50% 50%, rgba(103, 201, 143, 0.18), rgba(175, 119, 217, 0.15) 52%, rgba(255,255,255,0.4));
      border: 1px solid rgba(15, 23, 42, 0.06);
      box-shadow: inset 0 0 40px rgba(255,255,255,0.5), 0 18px 40px rgba(103, 201, 143, 0.08);
      display: grid;
      place-items: center;
      animation: float 6s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-8px); }
    }

    .flower-core {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      font-size: 3rem;
      background: linear-gradient(135deg, rgba(255,255,255,0.8), rgba(103, 201, 143, 0.22));
      box-shadow: 0 10px 28px rgba(15, 23, 42, 0.08);
    }

    .petal-ring {
      position: absolute;
      inset: 18px;
      border-radius: 50%;
      border: 2px dashed rgba(175, 119, 217, 0.28);
    }

    .mini-badges {
      position: absolute;
      bottom: 22px;
      left: 18px;
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
    }

    .mini-badges span {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 8px 10px;
      background: rgba(255,255,255,0.6);
      border: 1px solid rgba(15,23,42,0.04);
      border-radius: 999px;
      font-size: 0.8rem;
      color: var(--muted);
      font-weight: 700;
    }

    .main {
      padding: 18px 0 56px;
    }

    .section-block {
      padding: 24px 0 0;
    }

    .section-header {
      display: flex;
      align-items: end;
      justify-content: space-between;
      gap: 18px;
      margin-bottom: 18px;
    }

    .section-tag {
      display: inline-block;
      margin-bottom: 10px;
      padding: 8px 12px;
      border-radius: 999px;
      background: linear-gradient(90deg, rgba(103,201,143,0.18), rgba(175,119,217,0.18));
      color: var(--green-deep);
      font-size: 0.72rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      font-weight: 800;
    }

    .section-header h2 {
      margin: 0;
      font-size: clamp(1.8rem, 2vw, 2.5rem);
      letter-spacing: -0.04em;
      color: #0e2f2a;
    }

    .section-header p {
      margin: 8px 0 0;
      color: var(--muted);
    }

    .contador {
      min-width: 170px;
      text-align: center;
      padding: 11px 14px;
      border-radius: 999px;
      background: linear-gradient(90deg, rgba(175,119,217,0.12), rgba(103,201,143,0.12));
      border: 1px solid rgba(15,23,42,0.04);
      color: var(--green-deep);
      font-weight: 800;
      font-size: 0.92rem;
    }

    .catalogo-card {
      background: rgba(255,255,255,0.48);
      border: 1px solid rgba(15,23,42,0.04);
      border-radius: var(--radius-xl);
      box-shadow: var(--shadow);
      padding: 24px;
    }

    .busqueda {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-bottom: 18px;
      padding: 12px 14px;
      border-radius: 18px;
      border: 1px solid rgba(15,23,42,0.04);
      background: rgba(255,255,255,0.72);
    }

    .busqueda-icon {
      font-size: 1.2rem;
      width: 34px;
      height: 34px;
      display: grid;
      place-items: center;
      border-radius: 12px;
      background: linear-gradient(135deg, rgba(103,201,143,0.14), rgba(175,119,217,0.12));
    }

    .busqueda input {
      width: 100%;
      border: none;
      background: transparent;
      color: var(--text);
      font-size: 1rem;
      outline: none;
    }

    .busqueda input::placeholder {
      color: #7b8696;
    }

    .filtros {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 18px;
    }

    .filtro {
      appearance: none;
      border: 1px solid rgba(15,23,42,0.06);
      background: rgba(255,255,255,0.7);
      color: var(--text);
      padding: 10px 14px;
      border-radius: 999px;
      cursor: pointer;
      font-weight: 700;
      transition: all 0.2s ease;
    }

    .filtro:hover,
    .filtro:focus-visible {
      transform: translateY(-1px);
      box-shadow: 0 12px 20px rgba(15, 23, 42, 0.06);
      outline: none;
    }

    .filtro.activo {
      background: linear-gradient(90deg, var(--green), var(--purple));
      border-color: transparent;
      color: #fff;
      box-shadow: 0 12px 24px rgba(175, 119, 217, 0.22);
    }

    .grid-flores {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 18px;
    }

    .flor-card {
      display: flex;
      align-items: center;
      gap: 12px;
      padding: 14px 12px;
      background: linear-gradient(180deg, rgba(255,255,255,0.7), rgba(255,255,255,0.5));
      border: 1px solid rgba(15,23,42,0.04);
      border-radius: var(--radius-lg);
      box-shadow: 0 10px 20px rgba(15, 23, 42, 0.05);
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .flor-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 18px 30px rgba(15,23,42,0.08);
    }

    .flor-thumb {
      width: 72px;
      height: 72px;
      display: grid;
      place-items: center;
      flex-shrink: 0;
      border-radius: 18px;
      background: linear-gradient(135deg, rgba(103,201,143,0.18), rgba(175,119,217,0.16));
      font-size: 2rem;
      box-shadow: inset 0 0 18px rgba(255,255,255,0.4);
    }

    .flor-info {
      min-width: 0;
    }

    .flor-info h3 {
      margin: 0 0 6px;
      font-size: 1.05rem;
      letter-spacing: -0.02em;
      color: #112e28;
    }

    .flor-info p {
      margin: 0;
      color: var(--muted);
      font-size: 0.87rem;
      line-height: 1.45;
    }

    .sin-resultados {
      margin-top: 18px;
      padding: 18px;
      text-align: center;
      border-radius: 16px;
      background: rgba(255,255,255,0.45);
      border: 1px dashed rgba(15,23,42,0.08);
      color: var(--muted);
      font-weight: 600;
    }

    .curiosidad {
      display: grid;
      grid-template-columns: auto 1fr auto;
      gap: 18px;
      align-items: center;
      margin-top: 40px;
      background: rgba(255,255,255,0.48);
      border: 1px solid rgba(15,23,42,0.04);
      border-radius: var(--radius-xl);
      box-shadow: var(--shadow);
      padding: 22px 20px;
    }

    .curiosidad-icon {
      width: 64px;
      height: 64px;
      display: grid;
      place-items: center;
      border-radius: 18px;
      background: linear-gradient(135deg, rgba(103,201,143,0.18), rgba(175,119,217,0.14));
      font-size: 2.1rem;
    }

    .curiosidad h2 {
      margin: 0 0 8px;
      font-size: clamp(1.6rem, 2vw, 2.3rem);
      letter-spacing: -0.04em;
      color: #153629;
    }

    .curiosidad p {
      margin: 0;
      color: var(--muted);
      max-width: 680px;
    }

    .btn-link {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 12px 18px;
      background: rgba(255,255,255,0.7);
      border: 1px solid rgba(15,23,42,0.06);
      border-radius: 999px;
      font-weight: 700;
      text-decoration: none;
      color: var(--text);
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .btn-link:hover,
    .btn-link:focus-visible {
      transform: translateY(-2px);
      box-shadow: 0 14px 26px rgba(15,23,42,0.08);
      outline: none;
    }

    .site-footer {
      padding: 26px 0 40px;
      text-align: center;
      color: var(--muted);
      font-size: 0.95rem;
    }

    @media (max-width: 980px) {
      .hero-panel {
        grid-template-columns: 1fr;
      }

      .grid-flores {
        grid-template-columns: repeat(3, minmax(0, 1fr));
      }

      .section-header {
        align-items: start;
        flex-direction: column;
      }
    }

    @media (max-width: 720px) {
      .header-inner {
        flex-direction: column;
        justify-content: center;
        padding: 12px 0;
      }

      .nav {
        justify-content: center;
      }

      .grid-flores {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .curiosidad {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 480px) {
      .container {
        width: min(var(--max-width), calc(100% - 20px));
      }

      .hero {
        padding-top: 22px;
      }

      .hero-panel,
      .catalogo-card {
        padding: 18px 16px;
      }

      .grid-flores {
        grid-template-columns: 1fr;
      }

      .filtros {
        gap: 8px;
      }

      .filtro {
        flex: 1 1 calc(50% - 8px);
        text-align: center;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; }
      *, *::before, *::after {
        animation: none !important;
        transition: none !important;
      }
    }
  </style>
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <div class="brand" aria-label="FloraCraft">
        <div class="brand-mark">🌿</div>
        <span>FloraCraft</span>
      </div>

      <nav class="nav" aria-label="Navegación principal">
        <a href="#inicio">Inicio</a>
        <a href="#catalogo">Flores</a>
        <a href="#acerca">Acerca de</a>
      </nav>
    </div>
  </header>

  <main id="inicio" class="main">
    <div class="container">
      <section class="hero">
        <div class="hero-panel">
          <div class="hero-copy">
            <div class="badge">Enciclopedia botánica</div>
            <h1>El jardín mágico de Minecraft</h1>
            <p>
              Explora las flores, descubre sus secretos y conoce la belleza natural de cada rincón del mundo cúbico.
            </p>

            <div class="hero-actions">
              <a href="#catalogo" class="btn btn-primary">🌸 Explorar flores</a>
              <a href="#acerca" class="btn btn-secondary">📚 Acerca de</a>
            </div>
          </div>

          <div class="hero-visual" aria-hidden="true">
            <div class="flower-orb">
              <div class="petal-ring"></div>
              <div class="flower-core">🌼</div>
            </div>

            <div class="mini-badges">
              <span>0 Especies</span>
              <span>∞ Decoración</span>
              <span>🌎 Mundo por explorar</span>
            </div>
          </div>
        </div>
      </section>

      <section class="section-block" id="catalogo">
        <div class="section-header">
          <div>
            <span class="section-tag">Herbario digital</span>
            <h2>Explora la colección</h2>
            <p>Selecciona una planta para conocer todos sus secretos.</p>
          </div>
          <div class="contador" id="contador" aria-live="polite">Cargando colección...</div>
        </div>

        <div class="catalogo-card">
          <div class="busqueda" role="search">
            <div class="busqueda-icon" aria-hidden="true">🔎</div>
            <label class="sr-only" for="buscador">Buscar una flor</label>
            <input
              id="buscador"
              type="search"
              placeholder="Busca una flor por su nombre..."
              aria-label="Buscar flor por nombre"
            />
          </div>

          <div class="filtros" id="filtros" aria-label="Filtros de categoría">
            <button class="filtro activo" data-categoria="Todas" type="button">🌱 Todas</button>
            <button class="filtro" data-categoria="Pequeñas" type="button">🌷 Pequeñas</button>
            <button class="filtro" data-categoria="Altas" type="button">🌻 Altas</button>
            <button class="filtro" data-categoria="Especiales" type="button">✨ Especiales</button>
            <button class="filtro" data-categoria="Follaje" type="button">🍃 Follaje</button>
          </div>

          <div class="grid-flores" id="gridFlores"></div>

          <p class="sin-resultados" id="sinResultados" hidden>
            No encontramos esa planta. ¡Prueba con otro nombre! 🌿
          </p>
        </div>
      </section>

      <section class="curiosidad" id="acerca">
        <div class="curiosidad-icon" aria-hidden="true">🌱</div>

        <div>
          <span class="section-tag">¿Sabías que...?</span>
          <h2>Las flores son más que decoración</h2>
          <p>
            Muchas flores sirven para fabricar tintes, atraer abejas y decorar construcciones.
            Algunas plantas especiales tienen mecánicas únicas que vale la pena descubrir.
          </p>
        </div>

        <a
          href="https://minecraft.wiki/w/Flower"
          target="_blank"
          rel="noopener noreferrer"
          class="btn-link"
        >
          Consultar la wiki ↗
        </a>
      </section>
    </div>
  </main>

  <footer class="site-footer">
    <div class="container">
      🌿 FloraCraft<br />
      Una pequeña enciclopedia para los amantes de Minecraft.
      <br />
      Proyecto de fans, no oficial. Minecraft pertenece a sus respectivos propietarios.
    </div>
  </footer>

  <script>
    const flores = [
      { nombre: "Tulipán de pradera", categoria: "Pequeñas", icono: "🌷", descripcion: "Color vibrante y muy decorativo." },
      { nombre: "Margarita lunar", categoria: "Pequeñas", icono: "🌼", descripcion: "Aparece con un brillo suave bajo la luz del cielo." },
      { nombre: "Girasol del campo", categoria: "Altas", icono: "🌻", descripcion: "Se ve imponente y aporta altura al jardín." },
      { nombre: "Lirio de la luna", categoria: "Altas", icono: "🪷", descripcion: "Elegante y sereno, muy apreciado en biomas tranquilos." },
      { nombre: "Flor fantasmal", categoria: "Especiales", icono: "🕊️", descripcion: "Un raro ejemplar que parece venir de otra dimensión." },
      { nombre: "Orquídea de nether", categoria: "Especiales", icono: "✨", descripcion: "Rara y resplandeciente, casi legendaria." },
      { nombre: "Hiedra verde", categoria: "Follaje", icono: "🍃", descripcion: "Ideal para cubrir muros, cercas y rincones naturales." },
      { nombre: "Pasto ondulado", categoria: "Follaje", icono: "🌿", descripcion: "Da vida a senderos y jardines llenos de movimiento." },
      { nombre: "Violeta del bosque", categoria: "Pequeñas", icono: "🪻", descripcion: "Aparece en zonas húmedas y sombrías del mundo." },
      { nombre: "Rosa de cristal", categoria: "Especiales", icono: "💎", descripcion: "Un símbolo de belleza rara y muy valorado." },
      { nombre: "Dalia de madera", categoria: "Altas", icono: "🌾", descripcion: "Aporta un aire campestre y auténtico al paisaje." },
      { nombre: "Broté de prado", categoria: "Follaje", icono: "🌱", descripcion: "Perfecto para crear zonas verdes y naturales." }
    ];

    const gridFlores = document.getElementById("gridFlores");
    const contador = document.getElementById("contador");
    const buscador = document.getElementById("buscador");
    const sinResultados = document.getElementById("sinResultados");
    const filtros = document.querySelectorAll(".filtro");

    let categoriaActual = "Todas";

    function formatearCantidad(numero) {
      return numero === 1 ? "1 especie" : `${numero} especies`;
    }

    function renderFlores() {
      const valorBusqueda = buscador.value.trim().toLowerCase();

      const floresFiltradas = flores.filter((flor) => {
        const coincideCategoria =
          categoriaActual === "Todas" || flor.categoria === categoriaActual;

        const coincideBusqueda =
          flor.nombre.toLowerCase().includes(valorBusqueda);

        return coincideCategoria && coincideBusqueda;
      });

      contador.textContent = `Mostrando ${formatearCantidad(floresFiltradas.length)}`;

      if (floresFiltradas.length === 0) {
        gridFlores.innerHTML = "";
        sinResultados.hidden = false;
        return;
      }

      sinResultados.hidden = true;

      gridFlores.innerHTML = floresFiltradas
        .map(
          (flor) => `
            <article class="flor-card" aria-label="${flor.nombre}">
              <div class="flor-thumb" aria-hidden="true">${flor.icono}</div>
              <div class="flor-info">
                <h3>${flor.nombre}</h3>
                <p>${flor.descripcion}</p>
              </div>
            </article>
          `
        )
        .join("");
    }

    filtros.forEach((boton) => {
      boton.addEventListener("click", () => {
        categoriaActual = boton.dataset.categoria;
        filtros.forEach((btn) => {
          btn.classList.toggle("activo", btn === boton);
        });
        renderFlores();
      });
    });

    buscador.addEventListener("input", renderFlores);

    renderFlores();
  </script>
</body>
</html>
