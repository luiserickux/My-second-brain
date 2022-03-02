Es la acción que hace el navegador de forma automática de mover al principio del scope todos los recursos que utilizemos para evitar conflictos.

**Ejemplo de Hoisting:**
El navegador de forma interna mueve la declaración de la variable al principio para evitar que haya un error al aplicar la variable.
<pre><code>h1 {
	color: var(--color);
}

:root {
	--color: red;
}
</code></pre>

Esto se mencionó en la clase de [[Scope en variables CSS]]