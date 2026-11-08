# Teoría · Pieza 10: Caja y refrigeración

**Grupo:** Alejandro Correa · Adrian  Gámez

## 1. Ideas básicas

- Todo lo que consume la CPU o la gráfica **se convierte en calor**, y hay que sacarlo del PC.
- Si la CPU se calienta demasiado (unos **95–100 °C**), **baja su velocidad** para protegerse (*thermal throttling*) y, si sigue subiendo, el PC **se apaga**.
- El calor siempre va de lo caliente a lo frío. La refrigeración crea un camino:
  **CPU → pasta térmica → disipador → ventilador → fuera de la caja.**

## 2. Las piezas y para qué sirven

| Pieza | Para qué sirve |
|---|---|
| **Pasta térmica** | Rellena los huecos microscópicos de aire entre la CPU y el disipador. El aire conduce muy mal el calor. |
| **Disipador** | Bloque de metal (cobre y aluminio) con aletas que recoge el calor de la CPU. |
| **Heatpipes** | Tubos de cobre con líquido dentro que se evapora con el calor y lo lleva rápido hasta las aletas. |
| **Ventilador** | Sopla aire entre las aletas y se lleva el calor. |
| **Caja** | Organiza la entrada y salida de aire y filtra el polvo. |
| **AIO** | Refrigeración líquida cerrada: bomba sobre la CPU + tubos + radiador con ventiladores. |

## 3. Datos de la ficha técnica

| Dato | Unidad | Qué significa |
|---|---|---|
| **TDP** | W (vatios) | Calor que debe sacar el disipador |
| **Velocidad** | RPM | Vueltas por minuto del ventilador |
| **Caudal** | CFM o m³/h | Cuánto aire mueve |
| **Presión estática** | mmH₂O | Fuerza para empujar aire cuando algo estorba |
| **Ruido** | dB(A) | Lo que se oye (< 25 dB(A) = muy silencioso) |
| **Vida útil** | horas (MTTF) | Cuánto dura de media |

**Ojo:** las CPUs actuales consumen **más que su TDP** en turbo (ej.: Intel i9-14900K → 125 W base, 253 W turbo). Elige el disipador pensando en la cifra alta.

## 4. Ventiladores

| | 3 pines | 4 pines (PWM) |
|---|---|---|
| Cables | Tierra, 12 V, sensor de RPM | Los mismos + **cable de control** (azul) |
| Cómo se regula | Bajando el voltaje | La placa enciende y apaga la señal muy rápido (25.000 veces/s) |
| Control | Peor | Más preciso y silencioso |

- Si un ventilador PWM **pierde la señal**, gira **al máximo** por seguridad.
- Tamaños más comunes: **120 mm y 140 mm**.

| Tipo | Dónde va mejor |
|---|---|
| De **caudal** | Delante y detrás de la caja (sin obstáculos) |
| De **presión estática** | Radiadores y disipadores con muchas aletas |

## 5. Tipos de refrigeración

| Tipo | Lo bueno | Lo malo |
|---|---|---|
| **Pasiva** | Silencio total | Solo para chips que se calientan poco |
| **Por aire** | Barata y fiable | Ocupa mucho, puede chocar con la RAM |
| **Líquida AIO** | Enfría muy bien y deja libre la zona de la CPU | Más cara; la bomba puede fallar |
| **Líquida custom** | La que mejor enfría | Cara y necesita mantenimiento |

- **Radiadores:** 120, 240, **360**, 420 mm (para 1, 2, 3… ventiladores).
- **Pastas:** silicona/cerámica (la normal y segura), con partículas metálicas, y **metal líquido** (la mejor, pero **conduce la electricidad**).

## 6. Flujo de aire en la caja

- **El aire fresco entra por delante** y **el caliente sale por detrás y por arriba** (porque el calor sube).
- **Presión positiva:** entra un poco más de aire del que sale → el polvo solo entra por los filtros. **Es lo recomendado.**
- **Presión negativa:** sale más del que entra → el polvo se cuela por las rendijas.
- La **flecha** del marco del ventilador indica hacia dónde va el aire.
- Formatos de caja: **ATX** (normal) > micro-ATX > Mini-ITX (muy pequeña).

## 7. Errores típicos

1. **No quitar el plástico** de la base del disipador.
2. Pasta: ni mucha ni poca, **un punto del tamaño de un guisante**.
3. Ventilador de la CPU fuera de **CPU_FAN** → aviso **“CPU Fan Error”**.
4. No comprobar si el disipador o el radiador **caben en la caja**.
5. Ventiladores puestos al revés o cables que tapan el aire.
6. Con el tiempo: **pasta seca** y **polvo** → limpiar y cambiar la pasta.

**Ejemplo real · Noctua NH-D15:** disipador de doble torre, 2 ventiladores de 140 mm PWM, 165 mm de alto, 1.320 g, 24,6 dB(A), más de 150.000 h de vida.

---

## Preguntas tipo test (8)

**1. ¿Para qué sirve la pasta térmica?**
a) Para pegar el disipador a la CPU · **b) Para rellenar los huecos de aire entre la CPU y el disipador** ✅ · c) Para aislar la CPU de la electricidad · d) Para enfriar la CPU por sí sola
> El aire conduce muy mal el calor, y la pasta lo sustituye por algo que conduce mejor.

**2. ¿Qué hace una CPU cuando se calienta demasiado?**
a) Sube su velocidad · **b) Baja su velocidad para protegerse** ✅ · c) Enciende más ventiladores por su cuenta · d) Nada, sigue igual
> Se llama *thermal throttling*: reduce la velocidad para generar menos calor.

**3. ¿Qué tiene de más un ventilador de 4 pines respecto a uno de 3?**
a) Luces RGB · b) Más potencia · **c) Un cable para controlar la velocidad (PWM)** ✅ · d) Un sensor de temperatura
> El cuarto pin permite que la placa regule las vueltas de forma precisa.

**4. Si un ventilador PWM pierde la señal de control…**
a) Se para · b) Gira a la mitad · **c) Gira al máximo** ✅ · d) Hace saltar la alarma
> Es una medida de seguridad para que la CPU nunca se quede sin refrigeración.

**5. ¿Qué tipo de ventilador va mejor en un radiador?**
a) De caudal · **b) De presión estática** ✅ · c) Uno de 3 pines · d) Da igual
> El radiador frena el aire, y los de presión estática empujan con más fuerza.

**6. ¿Cuál es la forma recomendada de mover el aire en la caja?**
a) Entra por arriba y sale por delante · **b) Entra por delante y sale por detrás y por arriba** ✅ · c) Todo hacia dentro · d) Todo hacia fuera
> El aire caliente sube, así que lo lógico es sacarlo por arriba y por detrás.

**7. ¿Qué ventaja tiene la presión positiva en una caja?**
a) Hace menos ruido · b) Gasta menos electricidad · **c) Entra menos polvo, porque solo pasa por los filtros** ✅ · d) La CPU va más rápida
> Al entrar más aire del que sale, el sobrante escapa por las rendijas y el polvo no entra por ellas.

**8. Al encender el PC aparece “CPU Fan Error”. ¿Cuál es la causa más probable?**
a) Hay demasiada pasta · **b) El ventilador de la CPU no está en el conector CPU_FAN** ✅ · c) La caja es pequeña · d) Falta RAM
> La placa vigila el conector CPU_FAN, y si no detecta giro ahí, muestra el aviso.
