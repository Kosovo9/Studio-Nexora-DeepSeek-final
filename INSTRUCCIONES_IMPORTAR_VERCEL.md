# 📥 Cómo Importar Variables de Entorno en Vercel

## Método 1: Importar Archivo .env (Recomendado)

1. **Ve a tu proyecto en Vercel:**
   - Dashboard → Tu Proyecto → Settings → Environment Variables

2. **Click en "Import .env"** (botón gris con icono de documento)

3. **Selecciona el archivo `vercel.env`** de este repositorio

4. **Revisa las variables importadas** y reemplaza los valores de ejemplo con tus valores reales

5. **Selecciona los entornos** para cada variable:
   - ✅ Production
   - ✅ Preview  
   - ✅ Development

6. **Click en "Deploy"** para aplicar los cambios

---

## Método 2: Pegar Contenido Directamente

1. **Abre el archivo `vercel.env`** en este repositorio

2. **Copia TODO el contenido** del archivo

3. **En Vercel, en la sección Environment Variables**, pega el contenido en el área de texto que dice "or paste the .env contents above"

4. **Vercel detectará automáticamente** las variables y las agregará

5. **Reemplaza los valores de ejemplo** con tus valores reales

6. **Selecciona los entornos** para cada variable

7. **Click en "Deploy"**

---

## ⚠️ Importante Después de Importar

1. **Reemplaza TODOS los valores de ejemplo:**
   - `pk_test_...` → Tu clave real de Clerk
   - `sk_test_...` → Tu clave secreta real
   - `https://your-project.supabase.co` → Tu URL real de Supabase
   - etc.

2. **Actualiza `NEXT_PUBLIC_APP_URL`:**
   - Para producción: `https://tu-proyecto.vercel.app`
   - O tu dominio personalizado si lo tienes

3. **Verifica que todas las variables críticas estén configuradas:**
   - ✅ Clerk (2 variables)
   - ✅ Supabase (2 variables)
   - ✅ Stripe (3 variables)
   - ✅ Google AI (2 variables)
   - ✅ APP_URL (1 variable)

---

## 📋 Orden de Variables en el Archivo

Las variables están organizadas en este orden:

1. **Autenticación - Clerk** (2 variables)
2. **Base de Datos - Supabase** (2 variables)
3. **Pagos - Stripe** (3 variables)
4. **Inteligencia Artificial - Google AI** (2 variables)
5. **URL de la Aplicación** (1 variable)
6. **Analytics y Monitoreo** (2 variables)
7. **Verificación de Motores de Búsqueda** (3 variables)
8. **IA Alternativas** (4 variables)
9. **Notificaciones - Email** (6 variables)
10. **Notificaciones - Webhooks** (3 variables)
11. **CMS y Contenido** (1 variable)
12. **Google Search Console** (2 variables)
13. **SEO y Monitoreo** (1 variable)
14. **Token Refresh** (1 variable)

**Total: 33 variables** (9 críticas + 24 opcionales)

---

## ✅ Checklist Post-Importación

- [ ] Todas las variables críticas tienen valores reales (no ejemplos)
- [ ] `NEXT_PUBLIC_APP_URL` apunta a la URL correcta de producción
- [ ] Variables configuradas para los entornos correctos (Production/Preview/Development)
- [ ] Primer despliegue exitoso después de importar
- [ ] Aplicación funcionando correctamente en producción

---

**Archivo a usar:** `vercel.env` en la raíz del proyecto

