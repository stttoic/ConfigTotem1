# 🎹 Cómo Actualizar el Layout de tu Teclado Totem

Guía simple paso a paso para cambiar las teclas de tu teclado sin saber programación.

---

## 📋 Lo que necesitas antes de empezar:

- [ ] Tu teclado Totem
- [ ] Un cable USB-C
- [ ] Conexión a internet
- [ ] Git instalado en tu computadora
- [ ] Tu repositorio clonado en tu computadora

---

## 🛠️ Pasos para actualizar tu teclado:

### **Paso 1: Abrir el Editor Visual**

1. Ve a esta página web: https://nickcoutsos.github.io/keymap-editor/
2. En la sección **"Repository"**, elige la opción **"Clipboard"**
3. En **"Keyboard"**, selecciona **"totem"** de la lista

### **Paso 2: Cargar tu Configuración Actual**

1. En tu computadora, abre el archivo `config/totem.keymap` con cualquier editor de texto
2. **Copia TODO el contenido** del archivo (Ctrl+A, luego Ctrl+C)
3. En la página web, busca el área de texto llamada **"Keymap"**
4. **Pega el contenido** ahí (Ctrl+V)
5. Haz clic en el botón **"Load"** o **"Cargar"**

### **Paso 3: Hacer tus Cambios**

1. Verás un dibujo de tu teclado con todas las teclas
2. Haz clic en cualquier tecla que quieras cambiar
3. Se abrirá un menú con opciones
4. Selecciona la nueva función que quieres para esa tecla
5. Repite para todas las teclas que quieras modificar

### **Paso 4: Guardar los Cambios**

1. Cuando termines, busca el botón **"Export"** o **"Exportar"**
2. **Copia todo el código** que aparece en el área de texto
3. Vuelve al archivo `config/totem.keymap` en tu computadora
4. **Reemplaza TODO el contenido** con lo que acabas de copiar
5. **Guarda el archivo** (Ctrl+S)

### **Paso 5: Subir los Cambios a GitHub**

Abre la terminal en la carpeta de tu proyecto y ejecuta estos comandos **uno por uno**:

```bash
git add .
```
*(Esto prepara los cambios)*

```bash
git commit -m "Actualizar keymap"
```
*(Esto guarda los cambios con un mensaje)*

```bash
git push
```
*(Esto sube los cambios a GitHub)*

> **💡 Tip:** Puedes cambiar "Actualizar keymap" por cualquier mensaje que describa tus cambios, por ejemplo: "Agregar ñ en la N" o "Cambiar números a multimedia"

### **Paso 6: Descargar el Firmware Compilado**

1. Ve a tu repositorio en GitHub (en tu navegador)
2. Haz clic en la pestaña **"Actions"** (arriba)
3. Verás una lista de compilaciones. Haz clic en la **más reciente** (la de arriba)
4. Espera a que termine de compilar (puede tomar 2-5 minutos)
   - ✅ Marca verde = compiló correctamente
   - ❌ Marca roja = hay un error (revisa tu código)
5. Cuando tenga marca verde, baja hasta el final de la página
6. Descarga el archivo **"firmware.zip"**
7. **Descomprime** el archivo ZIP

### **Paso 7: Flashear el Teclado**

**Para el lado IZQUIERDO:**
1. Conecta la **mitad IZQUIERDA** del teclado con el cable USB
2. Presiona el **botón de reset DOS veces rápido** (está en la parte de atrás)
3. El teclado aparecerá como una **unidad USB** en tu computadora
4. Arrastra el archivo `totem_left-seeeduino_xiao_ble-zmk.uf2` a esa unidad
5. El teclado se reiniciará automáticamente

**Para el lado DERECHO:**
1. Desconecta el lado izquierdo
2. Conecta la **mitad DERECHA** del teclado con el cable USB
3. Presiona el **botón de reset DOS veces rápido**
4. Arrastra el archivo `totem_right-seeeduino_xiao_ble-zmk.uf2` a la unidad
5. El teclado se reiniciará automáticamente

---

## ✅ ¡Listo!

Tu teclado ahora tiene la nueva configuración. Prueba todas las teclas para verificar que funcionen como esperabas.

---

## 🆘 Problemas Comunes:

### **"No puedo encontrar el botón de Actions en GitHub"**
- Asegúrate de estar en TU repositorio (tu nombre de usuario/zmk-config)
- Actions está en la barra superior junto a "Code", "Issues", "Pull requests"

### **"La compilación tiene una X roja"**
- Hay un error en el código
- Revisa que hayas copiado y pegado correctamente
- Verifica que no falten comas o paréntesis en el código

### **"El teclado no aparece como USB cuando presiono reset"**
- Presiona el botón reset DOS veces seguidas (no una sola vez)
- Debe ser rápido, como un doble clic del mouse
- Prueba con otro cable USB

### **"Una tecla no funciona como esperaba"**
- Verifica que tu sistema operativo tenga el layout de teclado correcto (español, inglés, etc.)
- Algunas teclas especiales (æ, ø, ñ) dependen del layout del sistema

---

## 📝 Notas Importantes:

- **Siempre guarda una copia** de tu archivo `totem.keymap` que funciona antes de hacer cambios grandes
- **Haz cambios pequeños** y pruébalos antes de hacer más modificaciones
- **Anota tus cambios** en el mensaje de commit para saber qué hiciste después
- Si algo sale mal, puedes volver a tu configuración anterior desde GitHub

---

**¿Necesitas ayuda?** Consulta la documentación oficial de ZMK: https://zmk.dev/docs
