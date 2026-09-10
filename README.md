# 🪺 Nest

**Nest** es una aplicación web de gestión de tareas con estética Apple, sincronización en la nube y un comportamiento motivacional pensado para no sentir culpa por lo que no haces.

> Hecha desde cero sin saber programar, usando Claude como asistente y herramientas gratuitas (GitHub Pages + Supabase).

🔗 **Demo en vivo:** [https://pkekw.github.io/Nest/](https://pkekw.github.io/Nest/)

---

## ✨ Características

### 🎨 Diseño
- Estética limpia y minimalista inspirada en Apple
- Tipografía del sistema (SF Pro / Inter)
- Modo claro y oscuro automáticos
- Animaciones y sonidos sutiles (generados con Web Audio API)
- Totalmente responsive: PC y móvil

### ✅ Gestión de tareas
- Crear, editar, completar y eliminar tareas
- **5 niveles de prioridad:**
  - 🔴 **Obligatoria** — requiere fecha de entrega, se destaca y aumenta su urgencia al acercarse
  - 🟠 **Alta**
  - 🔵 **Media**
  - ⚪ **Baja**
  - 🟣 **Opcional + Motivo** — tareas que suman pero se pueden dejar pasar sin culpa (con motivo visible)
- **Categorías personalizables:** Instituto, Ocio, Trabajo, Personal, Hogar...
- Una tarea puede tener varias categorías
- Buscador por texto
- Filtros: Todas / Pendientes / Completadas / Obligatorias / Opcional+Motivo
- Ordenar por fecha, prioridad o categoría

### 📅 Calendario
- Vista mensual y semanal
- Importancia representada con el color del subrayado
- Leyenda de colores
- Arrastrar tareas entre días para cambiar la fecha
- Reordenar tareas dentro de un día
- Bandeja de tareas sin fecha con recordatorio persistente

### 💬 Comportamiento inteligente
- **Recordatorios escalonados** para no dejar las cosas para el último momento:
  - Obligatorias: avisos a 14, 7, 3 y 1 día
  - Altas: avisos a 7, 3 y 1 día
- **Mensaje motivacional** cuando no hay nada urgente, sugiriendo avanzar tareas opcionales sin generar culpa

### ☁️ En la nube
- Autenticación con email y contraseña (Supabase Auth)
- Base de datos PostgreSQL en Supabase con Row Level Security
- **Sincronización en tiempo real** entre dispositivos (Supabase Realtime)
- Cada usuario solo ve sus propias tareas
- Exportar/Importar tareas como copia de seguridad manual

---

## 🛠️ Stack técnico

| Componente | Tecnología |
|---|---|
| Frontend | HTML + CSS + JavaScript (un solo archivo) |
| Base de datos | Supabase (PostgreSQL) |
| Autenticación | Supabase Auth |
| Sincronización | Supabase Realtime |
| Hosting | GitHub Pages |
| Keep-alive | GitHub Actions |
| Sonidos | Web Audio API |

---

## 🚀 Cómo usarlo

1. Entra a [https://pkekw.github.io/Nest/](https://pkekw.github.io/Nest/)
2. Crea una cuenta con tu email y contraseña
3. Empieza a añadir tareas
4. Ábrelo también en el móvil con la misma cuenta y verás cómo se sincroniza todo al instante

---

## 🧠 Cómo se hizo

Este proyecto nació de una idea simple: *"me apetece hacer algo creativo con tecnología"*.

Sin experiencia previa en programación, se utilizó **Claude** como asistente para:
- Diseñar la estructura de la app
- Generar el código HTML/CSS/JS
- Configurar Supabase (SQL, RLS, Realtime)
- Montar GitHub Pages y el workflow de keep-alive

Todo el proceso fue iterativo: describir la idea, probar, ajustar y mejorar.

---

## 📌 Notas técnicas

- La app es un único archivo `index.html` con todo embebido
- Las credenciales de Supabase se guardan en constantes al inicio del `<script>`
- Se usa la clave pública (`sb_publishable_...`) con políticas RLS para proteger los datos
- El workflow `.github/workflows/keepalive.yml` mantiene activo el proyecto de Supabase con una consulta diaria

---

## 🔮 Mejoras futuras

- [ ] Confirmación antes de borrar
- [ ] Estadísticas (rachas, tareas completadas por semana)
- [ ] Búsqueda en motivo y categorías
- [ ] Vista de "Hoy"
- [ ] Tareas recurrentes
- [ ] Sincronización con calendarios externos

---

## 📄 Licencia

Proyecto personal, sin licencia específica. Si te sirve de inspiración, adelante.
