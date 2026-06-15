# IG Analytics Dashboard

Dashboard de rendimiento de Instagram con análisis de IA powered by Claude.

## Características

- **Overview** — Métricas clave, alcance semanal, mix de contenido, heatmap de mejores horarios
- **Audiencia** — Demografía, género, edad, ciudades, crecimiento
- **Contenido** — Engagement por tipo, top posts, interacciones
- **Analizar contenido** — Sube una foto/Reel/video y Claude genera:
  - Scores de potencial viral, calidad visual, hook strength
  - 3 opciones de caption con distintos tonos
  - Hashtags optimizados para el nicho
  - Mejor horario para publicar
  - Recomendaciones de mejora
- **IA Advisor** — Chat directo con Claude sobre estrategia
- **Para marcas** — Media kit ejecutivo

## Setup

1. Abre `index.html` en tu navegador (o súbelo a cualquier hosting)
2. En la barra lateral, ingresa tu Anthropic API Key (`sk-ant-...`)
3. La key se guarda en localStorage del navegador

## Deployment (gratis)

### Opción A — Netlify (recomendado)
1. Ve a https://netlify.com
2. Arrastra la carpeta del proyecto al dashboard
3. Listo — obtienes URL tipo `https://tu-dashboard.netlify.app`

### Opción B — GitHub Pages
1. Sube los archivos a un repositorio de GitHub
2. Ve a Settings → Pages → Deploy from branch: main
3. URL: `https://tuusuario.github.io/ig-dashboard`

### Opción C — Vercel
```bash
npx vercel --prod
```

## Seguridad

La API key se almacena en localStorage del navegador del usuario.
Para producción, considera usar un backend proxy para no exponer la key.

## Personalización

Edita los datos de muestra directamente en `index.html`:
- Métricas: busca `metric-value` en el HTML
- Datos de charts: busca `initCharts()` en el script
- Perfil del system prompt: busca `Contexto del perfil` en el script
