# operativos-seguridad.html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Operativos de Seguridad | Dirección de Prevención y Seguridad</title>
  <style>
    :root {
      --color-primario: #0b3a63;
      --color-secundario: #0f5b94;
      --color-acento: #d9a441;
      --color-fondo: #f4f7fa;
      --color-blanco: #ffffff;
      --color-texto: #1f2937;
      --color-texto-sec: #5b6675;
      --color-borde: #d9e2ec;
      --color-exito: #1f7a4d;
      --sombra: 0 8px 24px rgba(11, 58, 99, 0.08);
      --radio: 14px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Segoe UI", Arial, sans-serif;
      background: var(--color-fondo);
      color: var(--color-texto);
      line-height: 1.5;
    }

    header {
      background: linear-gradient(135deg, var(--color-primario), var(--color-secundario));
      color: var(--color-blanco);
      padding: 28px 20px;
      box-shadow: var(--sombra);
    }

    .header-contenido {
      max-width: 1280px;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .marca {
      display: flex;
      align-items: center;
      gap: 16px;
    }

    .logo {
      width: 64px;
      height: 64px;
      border-radius: 50%;
      background: rgba(255,255,255,0.15);
      border: 2px solid rgba(255,255,255,0.25);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 28px;
      font-weight: 700;
    }

    .titulo h1 {
      font-size: 1.9rem;
      margin-bottom: 4px;
    }

    .titulo p {
      font-size: 0.98rem;
      color: rgba(255,255,255,0.9);
    }

    .fecha {
      background: rgba(255,255,255,0.12);
      padding: 12px 16px;
      border-radius: 10px;
      font-size: 0.95rem;
      border: 1px solid rgba(255,255,255,0.16);
    }

    .contenedor {
      max-width: 1280px;
      margin: 28px auto;
      padding: 0 20px 40px;
    }

    .panel {
      background: var(--color-blanco);
      border-radius: var(--radio);
      box-shadow: var(--sombra);
      padding: 22px;
      margin-bottom: 24px;
      border: 1px solid var(--color-borde);
    }

    .panel h2 {
      color: var(--color-primario);
      margin-bottom: 14px;
      font-size: 1.35rem;
      border-left: 5px solid var(--color-acento);
      padding-left: 12px;
    }

    .subtexto {
      color: var(--color-texto-sec);
      margin-bottom: 18px;
      font-size: 0.96rem;
    }

    .resumen-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 18px;
    }

    .tarjeta {
      background: linear-gradient(180deg, #ffffff, #f8fbff);
      border: 1px solid var(--color-borde);
      border-radius: 14px;
      padding: 18px;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .tarjeta:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 24px rgba(15, 91, 148, 0.12);
    }

    .tarjeta .etiqueta {
      color: var(--color-texto-sec);
      font-size: 0.9rem;
      margin-bottom: 8px;
    }

    .tarjeta .valor {
      font-size: 2rem;
      font-weight: 700;
      color: var(--color-primario);
      margin-bottom: 8px;
    }

    .tarjeta .detalle {
      font-size: 0.92rem;
      color: var(--color-texto-sec);
    }

    .filtros {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      align-items: center;
      margin-bottom: 16px;
    }

    select {
      padding: 10px 12px;
      border-radius: 10px;
      border: 1px solid var(--color-borde);
      background: white;
      min-width: 220px;
      font-size: 0.95rem;
      color: var(--color-texto);
    }

    .tabla-wrap {
      overflow-x: auto;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      min-width: 920px;
    }

    thead {
      background: var(--color-primario);
      color: white;
    }

    th, td {
      padding: 14px 12px;
      text-align: left;
      border-bottom: 1px solid var(--color-borde);
      font-size: 0.95rem;
      vertical-align: middle;
    }

    tbody tr:hover {
      background: #f8fbff;
    }

    .estado {
      display: inline-block;
      padding: 6px 10px;
      border-radius: 999px;
      font-size: 0.82rem;
      font-weight: 600;
    }

    .estado.ejecutado {
      background: #e7f6ee;
      color: var(--color-exito);
    }

    .estado.programado {
      background: #eef4fb;
      color: var(--color-secundario);
    }

    .destacados-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 18px;
    }

    .operativo {
      border: 1px solid var(--color-borde);
      border-radius: 14px;
      overflow: hidden;
      background: white;
    }

    .operativo-header {
      background: linear-gradient(135deg, var(--color-primario), var(--color-secundario));
      color: white;
      padding: 14px 16px;
      font-weight: 700;
    }

    .operativo-body {
      padding: 16px;
    }

    .operativo-body p {
      margin-bottom: 10px;
      color: var(--color-texto-sec);
      font-size: 0.94rem;
    }

    .operativo-body strong {
      color: var(--color-texto);
    }

    .grafico-wrap {
      margin-top: 18px;
    }

    .grafico {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      gap: 16px;
      align-items: end;
      min-height: 260px;
      padding: 20px 10px 0;
      border-left: 2px solid var(--color-borde);
      border-bottom: 2px solid var(--color-borde);
    }

    .barra-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: end;
      gap: 8px;
      height: 100%;
    }

    .barra {
      width: 55px;
      border-radius: 10px 10px 0 0;
      background: linear-gradient(180deg, var(--color-acento), #c88f22);
      position: relative;
      transition: 0.3s ease;
    }

    .barra:hover {
      filter: brightness(1.05);
      transform: scaleY(1.02);
    }

    .barra span {
      position: absolute;
      top: -28px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 0.84rem;
      color: var(--color-primario);
      font-weight: 700;
    }

    .mes-label {
      font-size: 0.9rem;
      color: var(--color-texto-sec);
      text-align: center;
    }

    footer {
      background: var(--color-primario);
      color: rgba(255,255,255,0.9);
      padding: 20px;
      text-align: center;
      font-size: 0.9rem;
      margin-top: 20px;
    }

    .nota {
      margin-top: 12px;
      padding: 12px 14px;
      background: #fff8e8;
      border: 1px solid #f1ddaa;
      border-radius: 10px;
      color: #6a571f;
      font-size: 0.92rem;
    }

    @media (max-width: 768px) {
      .titulo h1 {
        font-size: 1.5rem;
      }

      .grafico {
        gap: 10px;
      }

      .barra {
        width: 38px;
      }
    }
  </style>
</head>
<body>

  <header>
    <div class="header-contenido">
      <div class="marca">
        <div class="logo">DS</div>
        <div class="titulo">
          <h1>Operativos de Seguridad</h1>
          <p>Dirección de Prevención y Seguridad</p>
        </div>
      </div>
      <div class="fecha">
        Periodo de visualización: Enero a Junio 2026
      </div>
    </div>
  </header>

  <main class="contenedor">

    <section class="panel">
      <h2>Resumen Ejecutivo</h2>
      <p class="subtexto">
        Plataforma de visualización de acciones mensuales ejecutadas por la Dirección de Prevención y Seguridad,
        incluyendo operativos preventivos, fiscalizaciones, patrullajes e intervenciones territoriales.
      </p>

      <div class="resumen-grid">
        <div class="tarjeta">
          <div class="etiqueta">Operativos realizados</div>
          <div class="valor">148</div>
          <div class="detalle">Acumulado del semestre</div>
        </div>
        <div class="tarjeta">
          <div class="etiqueta">Patrullajes preventivos</div>
          <div class="valor">426</div>
          <div class="detalle">Cobertura territorial mensual acumulada</div>
        </div>
        <div class="tarjeta">
          <div class="etiqueta">Fiscalizaciones</div>
          <div class="valor">214</div>
          <div class="detalle">Comercio, tránsito y ocupación de espacios</div>
        </div>
        <div class="tarjeta">
          <div class="etiqueta">Procedimientos coordinados</div>
          <div class="valor">63</div>
          <div class="detalle">Acciones conjuntas con instituciones</div>
        </div>
      </div>
    </section>

    <section class="panel">
      <h2>Visualización Mensual</h2>
      <p class="subtexto">
        Seleccione un mes para revisar el detalle de acciones ejecutadas. Los datos son referenciales y pueden ser actualizados con información operativa real.
      </p>

      <div class="filtros">
        <label for="filtroMes"><strong>Filtrar por mes:</strong></label>
        <select id="filtroMes">
          <option value="todos">Todos los meses</option>
          <option value="Enero">Enero</option>
          <option value="Febrero">Febrero</option>
          <option value="Marzo">Marzo</option>
          <option value="Abril">Abril</option>
          <option value="Mayo">Mayo</option>
          <option value="Junio">Junio</option>
        </select>
      </div>

      <div class="tabla-wrap">
        <table id="tablaOperativos">
          <thead>
            <tr>
              <th>Mes</th>
              <th>Tipo de acción</th>
              <th>Sector / Territorio</th>
              <th>Cantidad</th>
              <th>Instituciones participantes</th>
              <th>Estado</th>
            </tr>
          </thead>
          <tbody>
            <tr data-mes="Enero">
              <td>Enero</td>
              <td>Patrullaje preventivo</td>
              <td>Sector Poniente</td>
              <td>72</td>
              <td>Seguridad Municipal</td>
              <td><span class="estado ejecutado">Ejecutado</span></td>
            </tr>
            <tr data-mes="Enero">
              <td>Enero</td>
              <td>Fiscalización de comercio</td>
              <td>Centro Cívico</td>
              <td>18</td>
              <td>Inspección / Seguridad</td>
              <td><span class="estado ejecutado">Ejecutado</span></td>
            </tr>
            <tr data-mes="Febrero">
              <td>Febrero</td>
              <td>Operativo intersectorial</td>
              <td>Plazas y áreas verdes</td>
              <td>11</td>
              <td>Seguridad / Aseo / Carabineros</td>
              <td><span class="estado ejecutado">Ejecutado</span></td>
            </tr>
            <tr data-mes="Febrero">
              <td>Febrero</td>
              <td>Control vehicular preventivo</td>
              <td>Ejes viales principales</td>
              <td>14</td>
              <td>Tránsito / Seguridad</td>
              <td><span class="estado ejecutado">Ejecutado</span></td>
            </tr>
            <tr data-mes="Marzo">
              <td>Marzo</td>
              <td>Intervención territorial</td>
              <td>Barrios priorizados</td>
              <td>9</td>
              <td>Gestión Territorial / Seguridad</td>
              <td><span class="estado ejecutado">Ejecutado</span></td>
            </tr>
            <tr data-mes="Marzo">
              <td>Marzo</td>
              <td>Ronda preventiva nocturna</td>
              <td>Sector Sur</td>
              <td>68</td>
              <td>Seguridad Municipal</td>
              <td><span class="estado ejecutado">Ejecutado</span></td>
            </tr>
            <tr data-mes="Abril">
              <td>Abril</td>
              <td>Fiscalización de incivilidades</td>
              <td>Entornos escolares</td>
              <td>26</td>
              <td>Seguridad / Educación / Inspección</td>
              <td><span class="estado ejecutado">Ejecutado</span></td>
            </tr>
            <tr data-mes="Abril">
              <td>Abril</td>
              <td>Operativo de recuperación de espacios</td>
              <td>Sector Oriente</td>
              <td>8</td>
              <td>Seguridad / Operaciones</td>
              <td><span class="estado ejecutado">Ejecutado</span></td>
            </tr>
            <tr data-mes="Mayo">
              <td>Mayo</td>
              <td>Patrullaje mixto</td>
              <td>Cuadrantes priorizados</td>
              <td>84</td>
              <td>Carabineros / Seguridad</td>
              <td><span class="estado ejecutado">Ejecutado</span></td>
            </tr>
            <tr data-mes="Mayo">
              <td>Mayo</td>
              <td>Operativo comunitario</td>
              <td>Ferias libres</td>
              <td>12</td>
              <td>Seguridad / Fiscalización</td>
              <td><span class="estado ejecutado">Ejecutado</span></td>
            </tr>
            <tr data-mes="Junio">
              <td>Junio</td>
              <td>Plan preventivo invierno</td>
              <td>Puntos críticos comunales</td>
              <td>15</td>
              <td>Seguridad / Emergencia</td>
              <td><span class="estado programado">Programado</span></td>
            </tr>
            <tr data-mes="Junio">
              <td>Junio</td>
              <td>Fiscalización territorial</td>
              <td>Entorno comercial</td>
              <td>22</td>
              <td>Inspección / Seguridad</td>
              <td><span class="estado programado">Programado</span></td>
            </tr>
          </tbody>
        </table>
      </div>

      <div class="nota">
        Nota: puede reemplazar cada fila por datos reales mensuales provenientes de reportes operativos de la Dirección.
      </div>
    </section>

    <section class="panel">
      <h2>Comportamiento Mensual</h2>
      <p class="subtexto">
        Representación gráfica simple del volumen de operativos ejecutados por mes.
      </p>

      <div class="grafico-wrap">
        <div class="grafico">
          <div class="barra-item">
            <div class="barra" style="height: 110px;"><span>18</span></div>
            <div class="mes-label">Enero</div>
          </div>
          <div class="barra-item">
            <div class="barra" style="height: 130px;"><span>22</span></div>
            <div class="mes-label">Febrero</div>
          </div>
          <div class="barra-item">
            <div class="barra" style="height: 155px;"><span>27</span></div>
            <div class="mes-label">Marzo</div>
          </div>
          <div class="barra-item">
            <div class="barra" style="height: 145px;"><span>25</span></div>
            <div class="mes-label">Abril</div>
          </div>
          <div class="barra-item">
            <div class="barra" style="height: 180px;"><span>31</span></div>
            <div class="mes-label">Mayo</div>
          </div>
          <div class="barra-item">
            <div class="barra" style="height: 120px;"><span>20</span></div>
            <div class="mes-label">Junio</div>
          </div>
        </div>
      </div>
    </section>

    <section class="panel">
      <h2>Operativos Destacados</h2>
      <p class="subtexto">
        Síntesis de acciones relevantes desarrolladas por la Dirección en coordinación con otras unidades e instituciones.
      </p>

      <div class="destacados-grid">
        <article class="operativo">
          <div class="operativo-header">Patrullajes Mixtos</div>
          <div class="operativo-body">
            <p><strong>Objetivo:</strong> reforzar presencia preventiva en sectores priorizados.</p>
            <p><strong>Cobertura:</strong> cuadrantes con mayor demanda operativa.</p>
            <p><strong>Coordinación:</strong> Carabineros y Seguridad Municipal.</p>
          </div>
        </article>

        <article class="operativo">
          <div class="operativo-header">Fiscalización Territorial</div>
          <div class="operativo-body">
            <p><strong>Objetivo:</strong> controlar incivilidades y uso irregular del espacio público.</p>
            <p><strong>Ámbito:</strong> comercio, tránsito, ferias y puntos críticos.</p>
            <p><strong>Coordinación:</strong> Inspección General y equipos municipales.</p>
          </div>
        </article>

        <article class="operativo">
          <div class="operativo-header">Intervención Comunitaria</div>
          <div class="operativo-body">
            <p><strong>Objetivo:</strong> recuperar espacios y fortalecer percepción de seguridad.</p>
            <p><strong>Territorio:</strong> barrios priorizados y entornos comunitarios.</p>
            <p><strong>Coordinación:</strong> Gestión Territorial y unidades de apoyo.</p>
          </div>
        </article>
      </div>
    </section>

  </main>

  <footer>
    Dirección de Prevención y Seguridad · Plataforma de Visualización de Operativos
  </footer>

  <script>
    const filtroMes = document.getElementById("filtroMes");
    const filas = document.querySelectorAll("#tablaOperativos tbody tr");

    filtroMes.addEventListener("change", function () {
      const valor = this.value;

      filas.forEach(fila => {
        const mes = fila.getAttribute("data-mes");

        if (valor === "todos" || mes === valor) {
          fila.style.display = "";
        } else {
          fila.style.display = "none";
        }
      });
    });
  </script>
</body>
</html>
