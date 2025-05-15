# 📦 Gestor de Pedidos para Empleados

Este bot de WhatsApp permite a los empleados de un negocio consultar el estado de los pedidos que gestionaron, recibir avisos automáticos cuando llegan productos y tener acceso a información filtrada desde una base de datos en Google Sheets.

> ✅ En uso real desde 2025

---

## 🎯 Objetivo

Automatizar la comunicación interna de una tienda o equipo de ventas, especialmente en logística post-venta. Permite:

- Consultar pedidos pendientes
- Ver pedidos por empleado
- Recibir alertas cuando un producto cambia de estado
- Evitar seguimientos manuales

---

## 📱 Cómo funciona

1. El empleado escribe al bot por WhatsApp
2. El bot le muestra botones interactivos con opciones como:
   - "Ver pedidos pendientes"
   - "Buscar pedido"
   - "Pedidos por cobrar"
3. El bot consulta una hoja de Google Sheets y devuelve los resultados filtrados
4. Si un pedido cambia de estado (por ejemplo, "en tránsito" → "pendiente"), el bot avisa automáticamente al vendedor

---

## 💬 Ejemplo de interacción

- 👤 **Empleado**: Ver pedidos pendientes  
- 🤖 **Bot**:  
  - 📦 **Pedido**: P10234  
  - 📱 **Producto**: iPhone 13  
  - 🚚 **Estado**: En tránsito  
  - 💰 **Resta pagar**: $150.000  


---

## 🧠 Tecnologías utilizadas

- `whatsapp-web.js` – Para manejar los mensajes de WhatsApp
- `Google Sheets API` – Para consultar el estado de pedidos
- `Node.js` – Backend del bot
- `Railway` – Hosting del bot
- `node-cron` – Tareas automáticas de verificación cada X minutos

---

## 🗂 Estructura de datos

Se trabaja con 2 hojas principales:

1. **Pedidos**  
   - Nro Pedido, Empleado, Cliente, Estado global, Resta pagar, etc.

2. **Productos de Pedido**  
   - Nro Pedido, Producto, Cantidad, Estado por producto, Ubicación, etc.

El bot puede detectar cambios en ambos niveles: estado del pedido general o de cada producto.

---

## 🔔 Notificaciones automáticas

- Cuando un producto pasa de "En tránsito" a "Pendiente"
- Cuando hay productos listos para entregar
- Cuando un pedido tiene pagos pendientes

---

## 📊 ¿Qué resuelve?

✅ Centraliza info en Sheets  
✅ Evita hacer consultas manuales  
✅ Agiliza la coordinación interna  
✅ Ayuda a no perder de vista productos en tránsito

---

## 🔐 Código

Este proyecto está en uso privado y el código no es público por motivos de seguridad. El funcionamiento completo está explicado en este documento.

---

> 💬 *“Pensado para equipos que manejan muchos pedidos a la vez y necesitan mantener informados a sus vendedores sin fricción.”*


