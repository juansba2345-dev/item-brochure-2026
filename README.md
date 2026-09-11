# ITEM Brochure 2026

Brochure público de ITEM Constructores S.A.S. Página estática de una sola pieza
(`index.html`), autocontenida — fuentes, imágenes y logos empacados adentro,
no depende de ningún servicio externo.

## Publicar en Azure Static Web Apps (mismo patrón que erp.itemconstructoressas.com)

1. Portal de Azure → Crear recurso → Static Web App
2. Origen: GitHub → este repo → rama `main`
3. Build presets: **Custom**. App location: `/`. Output location: (vacío)
4. Una vez creado: Dominios personalizados → agregar `brochure.itemconstructoressas.com`
   (o el subdominio que se decida) → Azure da el registro CNAME a poner en el DNS
5. Cada push a `main` lo actualiza solo (GitHub Action que Azure agrega sola al repo)
