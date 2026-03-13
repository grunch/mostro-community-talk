---
theme: default
title: "Mostro Community Talk #1"
info: |
  ## Primera llamada con comunidades hispanohablantes
  mostro.community
class: text-center
drawings:
  persist: false
transition: fade-out
mdc: true
fonts:
  mono: 'Fira Code'
---

# Mostro Community Talk #1 {.font-mono .text-green-400}

## Primera llamada con comunidades hispanohablantes {.text-gray-400 .font-mono}

<div class="mt-10 flex justify-center items-center gap-4">
  <img src="/mostro-node.png" class="h-20 rounded-lg" />
</div>

<div class="abs-br m-6 text-sm text-gray-500 font-mono">
mostro.community · 2026
</div>

<div class="abs-bl m-6">
  <a href="/en/" class="text-xs text-gray-500 hover:text-green-400 font-mono">🇬🇧 English</a>
</div>

<!--
Bienvenida corta. Objetivo: alinear visión + operación real.
Duración total sugerida: 20-25 min + Q&A.
-->

---
layout: center
class: text-center
transition: fade
---

<div class="text-3xl font-mono text-green-400 leading-relaxed">

No venimos a vender humo.<br/>
Venimos a construir mercados P2P comunitarios.

</div>

<!--
Slide de tono.
-->

---
transition: slide-left
---

# Agenda (25 min) {.font-mono}

<!--
Nota: Mantener ritmo. Si se extiende Q&A, recortar ronda de presentaciones a 2 preguntas clave.
-->
<div class="mt-8 text-left max-w-3xl mx-auto text-lg">

1. Bienvenida e introducción
2. Qué es Mostro y cómo funciona
3. Qué implica correr un nodo
4. Requisitos técnicos + instalación
5. Presentaciones de comunidades
6. Preguntas y respuestas
7. Próximos pasos y cierre

</div>

---
transition: slide-left
---

# ¿Qué es Mostro? {.font-mono}

<!--
Mensaje clave: Mostro no reemplaza comunidad, la potencia con infraestructura.
Evitar tecnicismos largos aquí.
-->
<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

- Infraestructura P2P sobre **Lightning + Nostr**  
- Sin custodia central de fondos  
- Con reputación y resolución de disputas  
- Diseñado para comunidades, no para plataformas cerradas

</div>

<div class="mt-8 p-4 border border-green-700/50 rounded-lg bg-green-950/20 text-sm text-gray-300">
Mostro no es “una app”. Es un ecosistema operativo.
</div>

---
transition: slide-left
---

# Proyectos clave del ecosistema {.font-mono}

<!--
Guión sugerido (60-90s):
- mostro = motor
- mobile = puerta de entrada usuario
- mostrix = panel operativo/disputas (hoy imprescindible)
- watchdog = alertas inmediatas (sin esto se te pasan disputas)
-->
<div class="grid grid-cols-2 gap-5 mt-6 text-left">

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="flex items-center gap-3 mb-2">
    <img src="/mostro-node.png" class="h-10 w-10 rounded" />
    <div class="font-bold">mostro</div>
  </div>
  <div class="text-sm text-gray-400">Daemon core del mercado P2P.</div>
  <div class="text-xs font-mono text-green-400 mt-2">github.com/MostroP2P/mostro</div>
</div>

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="flex items-center gap-3 mb-2">
    <img src="/mostro-mobile.png" class="h-10 w-10 rounded" />
    <div class="font-bold">mobile</div>
  </div>
  <div class="text-sm text-gray-400">Cliente para usuarios finales.</div>
  <div class="text-xs font-mono text-green-400 mt-2">github.com/MostroP2P/mobile</div>
</div>

<div class="p-4 border border-yellow-700 rounded-lg bg-yellow-950/20">
  <div class="flex items-center gap-3 mb-2">
    <img src="/mostrix-logo.png" class="h-10 w-10 rounded" />
    <div class="font-bold text-yellow-300">mostrix</div>
  </div>
  <div class="text-sm text-gray-300">Panel más completo hoy para administración y disputas.</div>
  <div class="text-xs font-mono text-yellow-300 mt-2">github.com/MostroP2P/mostrix</div>
</div>

<div class="p-4 border border-yellow-700 rounded-lg bg-yellow-950/20">
  <div class="flex items-center gap-3 mb-2">
    <img src="/mostro-watchdog.png" class="h-10 w-10 rounded" />
    <div class="font-bold text-yellow-300">watchdog</div>
  </div>
  <div class="text-sm text-gray-300">Bot Telegram: alerta de disputas en tiempo real.</div>
  <div class="text-xs font-mono text-yellow-300 mt-2">github.com/MostroP2P/mostro-watchdog</div>
</div>

</div>

<!--
Punto clave: hoy mostrix + watchdog son indispensables para operar serio.
-->

---
transition: slide-left
---

# Cómo funciona (visión simple) {.font-mono}

<!--
No bajar a detalle de protocol internals.
Objetivo: que cualquiera entienda el flujo de una orden en <90s.
-->
<div class="mt-8 text-sm font-mono">

```text
Maker publica orden  →  Taker acepta  →  Hold invoice activo
        ↓                                  ↓
   Mensajería Nostr                 Confirmación fiat
        ↓                                  ↓
     Release ------------------> BTC al comprador
```

</div>

<div class="mt-6 text-gray-400 text-sm">
Lightning liquida. Nostr coordina. Mostro aplica reglas.
</div>

---
transition: slide-left
---

# Qué implica correr un nodo {.font-mono}

<!--
Subrayar que correr nodo = responsabilidad técnica + social.
No venderlo como "solo levantar un docker".
-->
<div class="grid grid-cols-2 gap-8 mt-8 text-left">

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="font-bold mb-2">Técnico</div>
  <ul class="text-sm text-gray-300">
    <li>Uptime y monitoreo</li>
    <li>Backups y updates</li>
    <li>Observabilidad y alertas</li>
  </ul>
</div>

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="font-bold mb-2">Operativo</div>
  <ul class="text-sm text-gray-300">
    <li>Soporte a comunidad</li>
    <li>Políticas claras</li>
    <li>Gestión de disputas</li>
  </ul>
</div>

</div>

---
transition: slide-left
---

# Stack mínimo recomendado {.font-mono}

<!--
Frase fuerte: sin mostrix/watchdog no hay operación seria de disputas.
-->
<div class="grid grid-cols-4 gap-4 mt-8 text-center">

<div class="p-3 border border-gray-700 rounded-lg">
  <img src="/mostro-node.png" class="h-14 mx-auto mb-2 rounded" />
  <div class="text-sm font-bold">mostro</div>
</div>

<div class="p-3 border border-gray-700 rounded-lg">
  <img src="/mostrix-logo.png" class="h-14 mx-auto mb-2 rounded" />
  <div class="text-sm font-bold">mostrix</div>
</div>

<div class="p-3 border border-gray-700 rounded-lg">
  <img src="/mostro-watchdog.png" class="h-14 mx-auto mb-2 rounded" />
  <div class="text-sm font-bold">watchdog</div>
</div>

<div class="p-3 border border-gray-700 rounded-lg">
  <img src="/mostro-mobile.png" class="h-14 mx-auto mb-2 rounded" />
  <div class="text-sm font-bold">mobile</div>
</div>

</div>

<div class="mt-8 text-sm text-yellow-300 font-mono">
Nodo sin mostrix + watchdog = operar a ciegas en disputas.
</div>

---
transition: slide-left
---

# Requisitos técnicos {.font-mono}

<!--
Mantenerlo realista: empezar pequeño, pero con disciplina operativa.
-->
<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

- Servidor Linux estable (VPS o bare metal)  
- Nodo Lightning operativo  
- Conectividad a relays Nostr  
- Gestión segura de secretos y backups

</div>

---
transition: slide-left
---

# Instalación (alto nivel) {.font-mono}

<div class="mt-8 text-sm font-mono">

```bash
1) Preparar servidor
2) Configurar Lightning
3) Desplegar mostro
4) Configurar mostrix
5) Activar watchdog (alertas Telegram)
6) Validar flujo end-to-end con órdenes de prueba
```

</div>

<div class="mt-6 text-gray-400 text-sm">
El detalle de comandos va en la guía técnica posterior.
</div>

---
transition: slide-left
---

# Ronda de comunidades (2-3 min c/u) {.font-mono}

<!--
Si hay mucha gente: pedir respuestas en formato corto (30-45s por punto).
Priorizar: meta de 30 días + bloqueo principal.
-->
<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

1. Nombre de la comunidad y región  
2. Nivel técnico del equipo  
3. Meta para los próximos 30 días  
4. Principal bloqueo actual

</div>

---
transition: slide-left
---

# Preguntas y respuestas {.font-mono}

<div class="mt-8 grid grid-cols-2 gap-8 text-left">

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="font-bold">Técnicas</div>
  <div class="text-sm text-gray-400 mt-2">Infraestructura, seguridad, operación, monitoreo.</div>
</div>

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="font-bold">Comunidad</div>
  <div class="text-sm text-gray-400 mt-2">Soporte, reputación, disputas, gobernanza local.</div>
</div>

</div>

---
transition: slide-left
---

# Próximos pasos {.font-mono}

<!--
Cerrar con claridad operativa: quién hace qué, para cuándo, y por dónde se coordina.
-->
<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

- Crear grupo piloto hispanohablante  
- Publicar guía de despliegue + checklist operativo  
- Definir métricas de salud por nodo  
- Agendar segunda call con aprendizajes

</div>

---
layout: center
class: text-center
transition: fade
---

# Gracias {.font-mono .text-green-400}

<div class="mt-6 text-gray-300">
Construyamos infraestructura P2P resiliente, abierta y comunitaria.
</div>

<div class="mt-10 text-sm text-gray-500 font-mono">
mostro.community · @MostroP2P · @lnp2pBot
</div>

<!--
Cierre (20s):
- Gracias por sumarse temprano.
- Esta etapa define estándares de operación para toda la red.
- Nos vemos en la siguiente call con avances concretos.
-->

---
transition: slide-left
---

# Backup Q&A: Disputas {.font-mono}

<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

- Flujo recomendado hoy: **mostrix + watchdog**  
- Watchdog alerta en Telegram cuando aparece disputa  
- Operador entra a mostrix y gestiona resolución  
- Registrar lecciones para mejorar política local

</div>

<div class="mt-6 p-4 border border-yellow-700 rounded-lg bg-yellow-950/20 text-sm text-gray-300">
Si no hay alertas, la disputa puede quedar sin atender. Ese riesgo hoy es real.
</div>

---
transition: slide-left
---

# Backup Q&A: Seguridad operativa {.font-mono}

<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

Checklist mínimo por nodo:

- Acceso SSH endurecido + actualizaciones  
- Backups frecuentes y verificados  
- Monitoreo de servicios críticos  
- Procedimiento de incidentes documentado

</div>

<div class="mt-6 text-sm text-gray-400">
Objetivo: operar de forma predecible, no heroica.
</div>
