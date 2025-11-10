# 🚀 Configuración Completa de Vercel - Studio Nexora DeepSeek Final

## 📋 Pasos para Configurar Vercel

### 1. Conectar Repositorio en Vercel

1. **Ve a Vercel Dashboard:**
   - Visita: https://vercel.com/dashboard
   - Inicia sesión con tu cuenta

2. **Importar Proyecto:**
   - Click en "Add New..." → "Project"
   - Selecciona "Import Git Repository"
   - Busca: `Kosovo9/Studio-Nexora-DeepSeek-final`
   - Click en "Import"

3. **Configurar Proyecto:**
   - **Framework Preset:** Next.js (detectado automáticamente)
   - **Root Directory:** `./` (raíz del proyecto)
   - **Build Command:** `npm run build` (ya configurado en vercel.json)
   - **Output Directory:** `.next` (automático para Next.js)
   - **Install Command:** `npm install` (ya configurado)

4. **Click en "Deploy"** (las variables de entorno las configuramos después)

---

## 🔐 Configurar Variables de Entorno

### Paso 1: Ir a Settings → Environment Variables

1. En el dashboard de Vercel, selecciona tu proyecto
2. Ve a **Settings** → **Environment Variables**
3. Agrega cada variable una por una

### Paso 2: Variables Críticas (REQUERIDAS)

Agrega estas variables para **Production, Preview, y Development**:

```env
# Autenticación - Clerk
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_live_... (o pk_test_... para desarrollo)
CLERK_SECRET_KEY=sk_live_... (o sk_test_... para desarrollo)

# Base de Datos - Supabase
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...

# Pagos - Stripe
STRIPE_SECRET_KEY=sk_live_... (o sk_test_... para desarrollo)
STRIPE_WEBHOOK_SECRET=whsec_...
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_live_... (o pk_test_... para desarrollo)

# Inteligencia Artificial - Google AI
NEXT_PUBLIC_GOOGLE_AI_API_KEY=your-google-ai-key
GOOGLE_AI_API_KEY=your-google-ai-key

# URL de la Aplicación
NEXT_PUBLIC_APP_URL=https://studio-nexora-deepseek-final.vercel.app
```

### Paso 3: Variables Opcionales (Recomendadas)

```env
# Analytics y Monitoreo
NEXT_PUBLIC_GA_ID=G-XXXXXXXXXX
NEXT_PUBLIC_SENTRY_DSN=https://xxx@sentry.io/yyy

# Verificación de Motores de Búsqueda
NEXT_PUBLIC_GOOGLE_VERIFICATION=your-google-verification-code
NEXT_PUBLIC_YANDEX_VERIFICATION=your-yandex-verification-code
NEXT_PUBLIC_BING_VERIFICATION=your-bing-verification-code

# Notificaciones - Email
EMAIL_USERNAME=your-email@gmail.com
EMAIL_PASSWORD=your-app-password
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
QA_REPORT_EMAIL=recipient@example.com
ALERT_EMAIL=admin@studio-nexora.com

# Notificaciones - Webhooks
SLACK_WEBHOOK_URL=https://hooks.slack.com/services/...
SLACK_WEBHOOK=https://hooks.slack.com/services/...
DISCORD_WEBHOOK_URL=https://discord.com/api/webhooks/...

# CMS y Contenido
NOTION_API_KEY=secret_xxx

# SEO y Monitoreo
SEO_URL=https://studio-nexora.com
```

### Paso 4: Configurar para cada Entorno

Para cada variable, selecciona los entornos donde aplicará:
- ✅ **Production** - Solo producción
- ✅ **Preview** - Para preview deployments
- ✅ **Development** - Para desarrollo local con Vercel CLI

**Recomendación:** Configura todas las variables críticas para los 3 entornos.

---

## 🔄 Despliegue Automático

Una vez configuradas las variables:

1. **Vercel detectará automáticamente** los cambios en GitHub
2. **Cada push a `main`** desplegará automáticamente
3. **Pull Requests** crearán preview deployments automáticamente

### Verificar Despliegue

1. Ve a **Deployments** en el dashboard de Vercel
2. Verifica que el build sea exitoso
3. Click en el deployment para ver los logs
4. Si hay errores, revisa los **Build Logs** y **Runtime Logs**

---

## 🛠️ Configuración Adicional

### Dominio Personalizado (Opcional)

1. Ve a **Settings** → **Domains**
2. Agrega tu dominio personalizado
3. Sigue las instrucciones de DNS

### Webhooks de Stripe

1. Ve a tu dashboard de Stripe
2. **Developers** → **Webhooks**
3. Agrega endpoint: `https://tu-dominio.vercel.app/api/payments/webhook`
4. Copia el **Signing Secret** y agrégalo como `STRIPE_WEBHOOK_SECRET` en Vercel

### Variables de Entorno por Entorno

Puedes tener diferentes valores para producción y desarrollo:

- **Production:** Usa claves `live_` de Stripe y Clerk
- **Preview/Development:** Usa claves `test_` de Stripe y Clerk

---

## ✅ Checklist de Verificación

- [ ] Repositorio conectado en Vercel
- [ ] Variables críticas configuradas (Clerk, Supabase, Stripe, Google AI)
- [ ] `NEXT_PUBLIC_APP_URL` configurado con la URL de Vercel
- [ ] Primer despliegue exitoso
- [ ] Build logs sin errores
- [ ] Aplicación funcionando en producción
- [ ] Webhook de Stripe configurado (si usas pagos)

---

## 🐛 Solución de Problemas

### Error: "Missing Environment Variables"

- Verifica que todas las variables críticas estén configuradas
- Asegúrate de seleccionar los entornos correctos (Production, Preview, Development)
- Reinicia el deployment después de agregar variables

### Error: "Build Failed"

- Revisa los **Build Logs** en Vercel
- Verifica que `npm install` se ejecute correctamente
- Asegúrate de que no haya errores de TypeScript

### Error: "Runtime Error"

- Revisa los **Runtime Logs** en Vercel
- Verifica que las variables de entorno estén accesibles
- Asegúrate de que las rutas API estén configuradas como dinámicas

---

## 📞 Soporte

Si encuentras problemas:
1. Revisa los logs en Vercel Dashboard
2. Verifica la documentación: https://vercel.com/docs
3. Consulta `DIAGNOSTICO_DESPLIEGUE_VERCEL.md` para más detalles

---

**Última actualización:** Noviembre 2025
**Repositorio:** https://github.com/Kosovo9/Studio-Nexora-DeepSeek-final

