# Breve explicación teórica: órbitas en la métrica de Kerr

La métrica de Kerr describe el espacio-tiempo exterior de un agujero negro idealmente rotante y sin carga eléctrica. A diferencia de Schwarzschild, incluye la rotación y el **arrastre de marcos**.

**De Schwarzschild a Kerr.** En el notebook se usa $s=GM/c^2$ y el espín adimensional $a_*=Jc/(GM^2)$. Al tomar $a_*=0$ se recupera la geometría de Schwarzschild. Para $|a_*|\ll1$ puede utilizarse una expansión de la métrica a primer orden en el espín.

**Geodésicas.** Una partícula de prueba en caída libre sigue, en ausencia de fuerzas no gravitacionales,

$$\frac{d^2x^\mu}{d\tau^2}+\Gamma^\mu_{\alpha\beta}\frac{dx^\alpha}{d\tau}\frac{dx^\beta}{d\tau}=0,$$

donde

$$\Gamma^\mu_{\alpha\beta}=\frac12 g^{\mu\nu}(\partial_\alpha g_{\nu\beta}+\partial_\beta g_{\nu\alpha}-\partial_\nu g_{\alpha\beta}).$$

Los símbolos de Christoffel contienen la información de cómo la geometría modifica las trayectorias. El proyecto los calcula simbólicamente con `SymPy` y `EinsteinPy`, y luego usa `SciPy` para resolver las ecuaciones diferenciales.

**Comprobación numérica.** Para trayectorias de tipo tiempo, la cuadrivelocidad satisface $g_{\mu\nu}U^\mu U^\nu=c^2$ (o $1$ si se usan unidades geometrizadas). Verificar esta relación ayuda a detectar errores de integración.

**Órbitas prógradas y retrógradas.** Para un agujero negro con espín positivo, una órbita prógrada gira en el mismo sentido que el objeto central; una retrógrada, en el sentido opuesto. La frecuencia angular **con signo** debe reflejar esa diferencia. La función original para órbitas retrógradas requiere corregir ese signo; las figuras correspondientes no están validadas.

**Visualización.** La conversión usada en parte del notebook de $(r,\theta,\phi)$ de Boyer–Lindquist a coordenadas $(x,y,z)$ es una representación aproximada para visualizar resultados. No debe interpretarse como transformación cartesiana exacta de esa geometría.
