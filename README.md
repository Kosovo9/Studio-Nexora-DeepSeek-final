# 🚀 Studio Nexora DeepSeek Final - AI Photo Studio MVP

**Repositorio Final Optimizado** - Production-ready Next.js application for AI-powered photo transformations.

## 📦 Repositorio

- **GitHub:** https://github.com/Kosovo9/Studio-Nexora-DeepSeek-final
- **Vercel:** Configurar en [vercel.com](https://vercel.com) (ver `CONFIGURACION_VERCEL.md`)

## 🛠️ Tech Stack

- **Next.js 14** - React framework with App Router
- **React 18** - UI library
- **Clerk** - Authentication
- **Supabase** - Database & Storage
- **Google AI Studio** - AI image generation
- **Stripe** - Payment processing
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Three.js** - 3D Earth visualization

## ✨ Features

✅ Photo upload (3+ images required)  
✅ Consent form (authorize image use)  
✅ Style selector (Dark Studio / Paris Café)  
✅ AI generation (Google AI Studio)  
✅ Watermark preview  
✅ Payment system (Bank MX + Stripe)  
✅ Download without watermark  
✅ 3D Earth visualization  
✅ Admin dashboard  
✅ SEO tools  
✅ Analytics integration  
✅ Bilingual support (ES/EN)  
✅ 27 API routes optimized for dynamic rendering  

## 🚀 Quick Start

### 1. Instalar Dependencias

```bash
npm install
```

### 2. Configurar Variables de Entorno

Copia `.env.local` o crea uno nuevo con las variables necesarias. Ver `VARIABLES_ENTORNO_COMPLETAS.md` para la lista completa.

**Variables Críticas:**
```env
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_...
CLERK_SECRET_KEY=sk_test_...
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
NEXT_PUBLIC_GOOGLE_AI_API_KEY=your-google-ai-key
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_test_...
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

### 3. Configurar Supabase

1. Ve a tu proyecto en Supabase
2. Ejecuta el SQL de `supabase-schema.sql` en el SQL Editor
3. Crea un bucket de Storage llamado `images` (acceso público)
4. Configura las políticas RLS según sea necesario

### 4. Ejecutar en Desarrollo

```bash
npm run dev
```

Abre [http://localhost:3000](http://localhost:3000)

### 5. Build para Producción

```bash
npm run build
npm start
```

## 📋 Despliegue en Vercel

### Configuración Automática

1. **Conectar Repositorio:**
   - Ve a [vercel.com/dashboard](https://vercel.com/dashboard)
   - Click en "Add New..." → "Project"
   - Importa: `Kosovo9/Studio-Nexora-DeepSeek-final`

2. **Configurar Variables de Entorno:**
   - Ve a Settings → Environment Variables
   - Agrega todas las variables críticas
   - Ver `CONFIGURACION_VERCEL.md` para instrucciones detalladas

3. **Despliegue Automático:**
   - Cada push a `main` desplegará automáticamente
   - Los Pull Requests crearán preview deployments

**📖 Guía Completa:** Ver `CONFIGURACION_VERCEL.md`

## 🧪 Testing

```bash
# Abrir Cypress UI
npm run cypress:open

# Ejecutar todos los tests
npm run test:e2e:full

# Generar reporte
npm run test:report
```

## 📚 Scripts Disponibles

```bash
# Desarrollo
npm run dev          # Servidor de desarrollo
npm run build        # Build de producción
npm run start        # Servidor de producción

# Testing
npm run test:e2e     # Tests E2E completos
npm run test:report  # Generar reporte de tests

# SEO
npm run seo:audit    # Auditoría SEO
npm run seo:monitor  # Monitoreo SEO

# Utilidades
npm run sitemap:generate  # Generar sitemap
npm run backup:supabase   # Backup de Supabase
```

## 📁 Estructura del Proyecto

```
├── app/                    # Next.js App Router
│   ├── api/               # API Routes (27 rutas dinámicas)
│   ├── admin/             # Admin dashboard
│   └── ...
├── components/            # Componentes React
├── lib/                   # Utilidades y configuraciones
├── public/                # Archivos estáticos
├── scripts/               # Scripts de utilidad
└── cypress/               # Tests E2E
```

## 🔧 Optimizaciones Implementadas

- ✅ 27 rutas API configuradas como dinámicas (`export const dynamic = 'force-dynamic'`)
- ✅ Build optimizado para producción
- ✅ Image optimization con Next.js Image
- ✅ Code splitting automático
- ✅ SEO optimizado
- ✅ Analytics integrado

## 📖 Documentación

- `CONFIGURACION_VERCEL.md` - Guía completa de configuración en Vercel
- `VARIABLES_ENTORNO_COMPLETAS.md` - Lista completa de variables de entorno
- `DIAGNOSTICO_DESPLIEGUE_VERCEL.md` - Guía de diagnóstico de problemas
- `README_DEPLOYMENT.md` - Guía de despliegue detallada

## 🐛 Solución de Problemas

### Error de Build

1. Verifica que todas las variables de entorno estén configuradas
2. Revisa los logs de build en Vercel
3. Consulta `DIAGNOSTICO_DESPLIEGUE_VERCEL.md`

### Error de Runtime

1. Revisa los Runtime Logs en Vercel
2. Verifica que las variables de entorno estén accesibles
3. Asegúrate de que las rutas API estén configuradas correctamente

## 📝 Licencia

Private - Studio Nexora

## 👥 Contribuidores

- **Desarrollo:** Studio Nexora Team
- **Repositorio:** https://github.com/Kosovo9/Studio-Nexora-DeepSeek-final

---

**Versión:** 1.0.0  
**Última actualización:** Noviembre 2025  
**Estado:** ✅ Production Ready
