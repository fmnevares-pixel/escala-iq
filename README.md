# 🚀 Escala IQ™ - Guía de Deployment en Vercel

## 📦 Archivos Incluidos

1. **index.html** - Aplicación completa de Escala IQ™
2. **vercel.json** - Configuración de Vercel
3. **README.md** - Este archivo (guía paso a paso)

---

## ⚡ DEPLOYMENT RÁPIDO (30 minutos)

### **PASO 1: Descargar los Archivos**

1. Crea una carpeta en tu computadora llamada `escala-iq`
2. Guarda los 3 archivos en esa carpeta:
   - `index.html`
   - `vercel.json`
   - `README.md`

---

### **PASO 2: Crear Cuenta en Vercel**

1. Ve a **https://vercel.com/**
2. Clic en **"Sign Up"** (esquina superior derecha)
3. Regístrate con una de estas opciones:
   - **GitHub** (Recomendado - más fácil para actualizar después)
   - **GitLab**
   - **Bitbucket**
   - **Email**

4. Si eliges GitHub:
   - Clic en "Continue with GitHub"
   - Autoriza Vercel
   - Listo

5. Completa tu perfil (nombre, uso: "Personal Project")

---

### **PASO 3: Subir tu Proyecto**

#### **Opción A: Sin GitHub (Más Rápido)**

1. En el dashboard de Vercel, clic en **"Add New..."** → **"Project"**
2. Clic en **"Continue with Different Deployment Method"**
3. Selecciona **"Deploy with Vercel CLI"** → pero ignorar esto
4. En su lugar, ve a la parte inferior y busca **"Import from File System"**
5. Arrastra la carpeta `escala-iq` a la ventana
6. Vercel detectará automáticamente el proyecto
7. Configuración:
   - **Project Name**: `escala-iq` (o el que prefieras)
   - **Framework Preset**: `Other`
   - **Root Directory**: `./`
   - **Build Command**: (déjalo vacío)
   - **Output Directory**: (déjalo vacío)
8. Clic en **"Deploy"**
9. ¡Espera 30-60 segundos!
10. ✅ Tu aplicación estará lista en: `https://escala-iq-XXXXX.vercel.app`

#### **Opción B: Con GitHub (Recomendada - Permite actualizaciones fáciles)**

1. Crea un repositorio en GitHub:
   - Ve a **https://github.com/new**
   - Nombre: `escala-iq`
   - Público o Privado (tu elección)
   - Clic en **"Create repository"**

2. Sube los archivos a GitHub:
   - **Opción Fácil**: Usa GitHub Desktop
     - Descarga: https://desktop.github.com/
     - Abre GitHub Desktop
     - File → Add Local Repository
     - Selecciona la carpeta `escala-iq`
     - Commit to main
     - Push origin
   
   - **Opción Avanzada**: Línea de comandos
     ```bash
     cd escala-iq
     git init
     git add .
     git commit -m "Initial commit"
     git branch -M main
     git remote add origin https://github.com/TU-USUARIO/escala-iq.git
     git push -u origin main
     ```

3. En Vercel:
   - Clic en **"Add New..."** → **"Project"**
   - Selecciona **"Import Git Repository"**
   - Busca y selecciona `escala-iq`
   - Clic en **"Import"**
   - Configuración (igual que Opción A)
   - Clic en **"Deploy"**

---

### **PASO 4: Configurar tu Dominio Personalizado**

Ahora vamos a hacer que funcione en `diagnostico.escalaestexito.com.mx`

1. En Vercel, ve a tu proyecto
2. Clic en **"Settings"**
3. En el menú lateral, clic en **"Domains"**
4. En el campo "Domain", escribe:
   ```
   diagnostico.escalaestexito.com.mx
   ```
5. Clic en **"Add"**

6. Vercel te mostrará instrucciones DNS. Verás algo como:
   ```
   Type: CNAME
   Name: diagnostico
   Value: cname.vercel-dns.com
   ```

7. **IMPORTANTE**: Copia estos datos, los necesitarás para el siguiente paso

---

### **PASO 5: Configurar DNS (Tu Proveedor Web)**

Ahora necesitas que tu proveedor web agregue el registro DNS.

#### **Información que debes dar a tu proveedor:**

Envía este mensaje a tu proveedor web:

```
Hola,

Necesito agregar un subdominio para una aplicación.

Por favor agrega este registro DNS:

Tipo: CNAME
Nombre/Host: diagnostico
Valor/Apunta a: cname.vercel-dns.com
TTL: 3600 (o automático)

El dominio completo será: diagnostico.escalaestexito.com.mx

Gracias.
```

#### **Tiempo de propagación:**
- DNS tarda entre **5 minutos a 48 horas** en propagarse
- Normalmente funciona en 15-30 minutos

#### **Verificar que funcionó:**
1. Ve a https://dnschecker.org/
2. Escribe: `diagnostico.escalaestexito.com.mx`
3. Tipo: CNAME
4. Clic en "Search"
5. Si ves "cname.vercel-dns.com" en verde = ✅ Funcionó

---

### **PASO 6: Verificar Dominio en Vercel**

1. Regresa a Vercel → Settings → Domains
2. Espera a que el status cambie de "Pending" a "Valid"
3. Puede tomar 5-30 minutos
4. Una vez que diga "Valid", visita:
   ```
   https://diagnostico.escalaestexito.com.mx
   ```
5. ¡Debería funcionar! 🎉

---

## ✅ CHECKLIST FINAL

Antes de considerarlo terminado, verifica:

- [ ] La página carga en `diagnostico.escalaestexito.com.mx`
- [ ] Puedes completar el formulario inicial
- [ ] Las 15 preguntas funcionan
- [ ] Se muestra el reporte de resultados
- [ ] **CRÍTICO**: Los emails llegan correctamente
  - [ ] Email al cliente con su diagnóstico
  - [ ] Email a contacto@escalaestexito.com.mx con notificación
- [ ] El logo se ve correctamente
- [ ] Los colores son los de Escala (azul #1B3A6D)
- [ ] Funciona en móvil (prueba desde tu teléfono)

---

## 🔧 CÓMO ACTUALIZAR EN EL FUTURO

### **Si usaste GitHub (Opción B):**
1. Edita `index.html` en tu computadora
2. Guarda los cambios
3. En GitHub Desktop:
   - Commit changes
   - Push origin
4. Vercel detecta el cambio automáticamente
5. ¡En 30 segundos está actualizado!

### **Si usaste carga directa (Opción A):**
1. Ve a Vercel → Tu proyecto
2. Clic en **"Deployments"**
3. Arrastra el nuevo archivo `index.html`
4. Listo

---

## 📧 VERIFICAR QUE EMAILS FUNCIONAN

Después del deployment, haz una prueba completa:

1. Ve a `diagnostico.escalaestexito.com.mx`
2. Llena el formulario con TUS datos reales
3. Completa las 15 preguntas
4. Al terminar, espera 1-2 minutos
5. Revisa:
   - Tu email personal (debe llegar diagnóstico)
   - contacto@escalaestexito.com.mx (debe llegar notificación)
6. Si no llegan, revisa:
   - EmailJS → History (debe mostrar envíos)
   - Carpeta de SPAM
   - Consola del navegador (F12) para errores

---

## 🆘 SOLUCIÓN DE PROBLEMAS

### **Problema: "Domain not found" o error 404**
**Solución**: El DNS aún no se propagó. Espera 30 minutos más.

### **Problema: Los emails no llegan**
**Solución**:
1. Abre consola del navegador (F12)
2. Busca errores en rojo
3. Verifica en EmailJS → History si los envíos aparecen
4. Si aparecen como "OK" pero no llegan → problema de KorreoWeb SMTP

### **Problema: La página se ve rara o sin estilos**
**Solución**: El CDN de Tailwind puede tardar. Refresca la página (Ctrl+F5)

### **Problema: No puedo agregar el dominio en Vercel**
**Solución**: Verifica que el DNS esté correctamente configurado primero

---

## 📞 CONTACTO PARA SOPORTE

Si tienes problemas técnicos:
1. Revisa la consola del navegador (F12)
2. Toma screenshot del error
3. Busca en la documentación de Vercel: https://vercel.com/docs

---

## 🎉 ¡FELICIDADES!

Si todo funcionó, ahora tienes:

✅ Escala IQ™ funcionando 24/7
✅ URL profesional: diagnostico.escalaestexito.com.mx
✅ Emails automáticos
✅ SSL incluido (https)
✅ Carga súper rápida (CDN global)
✅ Costo: $0 MXN/mes
✅ Control total (actualizas cuando quieras)

---

## 📈 PRÓXIMOS PASOS

1. **Promociona tu herramienta:**
   - Agrégala al menú de tu sitio web principal
   - Compártela en LinkedIn
   - Envíala por email a prospectos
   - Úsala en llamadas de ventas

2. **Analiza resultados:**
   - Revisa los emails que recibes
   - Identifica patrones en los scores
   - Ajusta tu pitch según los diagnósticos

3. **Mejoras futuras:**
   - Dashboard para ver todos los diagnósticos
   - Reportes en PDF automáticos
   - Integración con CRM
   - Más preguntas personalizadas

---

**¡Tu diferenciador estratégico está listo!** 🚀

Ninguna otra consultoría MiPyME en México tiene esto.