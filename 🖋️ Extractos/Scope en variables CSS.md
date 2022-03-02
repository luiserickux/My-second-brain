El scope es el contexto o el alcance en el que se puede utilizar un recurso respecto a otro.

## Ejemplos de tipo de scope:

**Alcance a nivel global:**
La variable está al alcance de todo el documento.
<pre><code>:root {
	--color: red;
}

h1 {
	color: var(--color);
}
</code></pre>

**Alcance a nivel de DOM:**
La variable está al alcance del elemento y de los hijos.
<pre><code>.article {
	--color: red;
}

.article div p {
	color: var(--color);
}
</code></pre>

**Alcance a nivel local:**
La variable está al alcance del elemento y de los hijos.
<pre><code>.article {
	--color: red;
	color: var(--color);
}

---------------------------------------------------------------------------------------------------

<elemento class="article" styel="--color: blue;">Este elemento tiene una variable en linea, osea a nivel local</elemento></code>
</pre>