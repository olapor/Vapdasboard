# Caja Vapers

App para llevar las cuentas del negocio de vapers: ventas al por menor (unidad) y al por mayor (caja),
compras de stock al proveedor, gastos del negocio y personales, y un freno a los gastos impulsivos.

- App publicada (con base de datos en la nube, funciona en iPhone y cualquier dispositivo):
  https://claude.ai/artifact/QNPKNqM4LRMrCHTCBnDis4
- Código fuente: `index.html`

## Qué guarda la base de datos
| Colección | Contenido |
|---|---|
| `products` | Modelos: unidades por caja, coste de la caja, precio por unidad, precio mínimo por caja, stock inicial |
| `sales` | Cada venta: modelo, unidad/caja, cantidad, precio, total, coste de la mercancía, forma de pago, cliente |
| `purchases` | Compras de stock: cajas, € por caja, proveedor (suman stock) |
| `expenses` | Gastos: importe, categoría, negocio o personal, necesario o capricho |
| `wait` | Lista de espera de caprichos (esperar antes de comprar) |
| `settings/main` | Límites de gasto, pausa antes de gastar, caja inicial, categorías |

El stock se calcula solo: stock inicial + compras − ventas.
