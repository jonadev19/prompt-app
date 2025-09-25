Te comparto el sistema de diseño para generar una aplicación móvil, de momento analiza la información y guardala en tu memoria para la construcción de las interfaces que te voy a solicitar:

---

La información proporcionada es esencial para definir la arquitectura de diseño con precisión y cumplir con los requisitos de **alta fidelidad** [Query, 382] y el **Javerage Electoral Design System (JEDS)** [Query, 385, 491].

Hemos confirmado tres puntos clave que ahora se integran en el *prompt* final:

1. **Fidelidad y Tema:** Se prioriza un prototipo de **Alta Fidelidad** bajo el **Tema Oscuro** [Query].
2. **Logo:** El **Logo de Javerage Electoral** debe ser prominente en el encabezado para fidelizar la marca [Query].
3. **Componente "Recordarme":** Se utilizará un **Toggle Switch** (interruptor deslizante) [Query] posicionado debajo del campo de contraseña, alineado con las mejores prácticas de UI móvil.

A continuación, se presenta la descripción de la UI en un solo párrafo y el *prompt* estructurado con el detalle final de los componentes.

---

### Descripción de la UI (Párrafo Único)

La pantalla de autenticación será un **prototipo de alta fidelidad** adherido estrictamente al **Tema Oscuro** de JEDS [Query, 390], diseñado bajo principios de **minimalismo digital** para garantizar seguridad, claridad y reducir la carga cognitiva. El diseño priorizará el formato *mobile-first*, comenzando con la visualización del **logotipo de la marca** en el encabezado para el reconocimiento y fidelización [Query]. El contenido se centrará en la autenticación, presentando un título de bienvenida y dos campos de entrada delineados (`textField.outlined`) para el Usuario (correo electrónico o ID) y la Contraseña [Query, 493]. Inmediatamente debajo del campo de contraseña, se incluirá el **Toggle Switch** para la función "Recordarme", alineado con los controles del formulario para una interacción eficiente y cumpliendo con el tamaño de objetivo táctil mínimo de **48x48dp**. La acción de acceso se finalizará con un **botón principal de relleno** (`button.filled`) con forma de píldora (`shape.corner.full`), ubicado cerca del borde inferior para facilitar el alcance táctil, y un enlace de soporte para la recuperación de la cuenta [Query, 493].

---

### Indicación Detallada de la Interfaz de Usuario (Prompt Estructurado para IA)

Utilizaremos la estructura de *prompt* recomendada (similar a ASPECCT o CTF) para garantizar que la herramienta de IA (Stitch, Figma Make, UX Pilot) genere un resultado de alta fidelidad [Query]:

**Rol:** Actúa como un diseñador UX/UI Senior, especializado en aplicaciones *mobile-first* con el **Javerage Electoral Design System (JEDS)**.

**Tarea:** Generar el **prototipo de alta fidelidad** para la pantalla de **Inicio de Sesión y Autenticación** [Query].

**Contexto y Restricciones:**

1. **Tema:** Usar el **Tema Oscuro** (`dark`) del JEDS.
2. **Tokens:** Referenciar todos los elementos con los tokens de JEDS (ej., `shape.corner.full`, `color.dark.primaryContainer`).
3. **Accesibilidad:** Asegurar que todos los elementos táctiles, incluido el Toggle Switch, cumplan con el mínimo de **48x48dp**.
4. **Espaciado:** Utilizar el token de espaciado `spacing.m` (16dp) para la separación vertical de los bloques principales.

### Estructura de Componentes de UI (de Arriba a Abajo)

| Bloque de Contenido                       | Componente Principal y Tokens de JEDS                                      | Función y Requisitos de Diseño                                                                                                                                                                        |
| ----------------------------------------- | -------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Contenedor Raíz y Fondo**            | Contenedor de página completa.                                             | Usar el token de color `color.dark.background`.                                                                                                                                                       |
| **2. Logo de Marca (Fidelización)**       | Componente de imagen o gráfico.                                            | **Colocar el logotipo de Javerage Electoral** centrado en la parte superior.                                                                                                                          |
| **3. Título Principal**                   | Componente de texto.                                                       | Contenido: "Bienvenido" o "Iniciar Sesión". Usar tipografía `typography.headline.large`.                                                                                                              |
| **4. Campo de Entrada (Usuario/ID)**      | Componente de campo de texto **delineado**(`textField.outlined`).          | **Etiqueta:** "Correo Electrónico o ID de Voluntario" [Query, 493].                                                                                                                                   |
| **5. Campo de Entrada (Contraseña)**      | Componente de campo de texto **delineado**(`textField.outlined`).          | **Etiqueta:** "Contraseña" [Query, 493]. Incluir un icono de alternancia para visibilidad.                                                                                                            |
| **6. Opción "Recordarme"**                | Componente de interacción **Toggle Switch** [Query] con etiqueta de texto. | Etiqueta: "Recordarme". **Debe estar flotando inmediatamente debajo del campo de contraseña, alineado al borde del formulario**[Query].                                                               |
| **7. Mensaje de Error (Bloque Opcional)** | Contenedor de texto para retroalimentación de seguridad [Query].           | Usar estilo de `label.medium`. Reservar espacio para mensajes como "Credenciales incorrectas" [Query].                                                                                                |
| **8. Botón de Acción Principal (CTA)**    | Componente de botón **relleno** (`button.filled`).                         | **Texto:** "Iniciar Sesión" [Query]. **Tokens:** Usar `color.dark.primaryContainer`para fondo y `color.dark.onPrimaryContainer` para texto. **Forma:**`shape.corner.full` (completamente redondeada). |
| **9. Enlace de Soporte**                  | Componente de texto interactivo.                                           | **Contenido:** "¿Olvidaste tu contraseña?" [Query]. Usar color `color.dark.tertiary` y tipografía `typography.label.large`.                                                                           |
