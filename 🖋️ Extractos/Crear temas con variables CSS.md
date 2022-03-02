Podemos hacer uso de las Variables CSS para crear temas con dos modos de colores: Light y Dark.

**Opción Típica:**
Establecemos un tema por defecto y en una clase llamada _Dark_ reescribimos los valores de las variables, se agrega y se quita la clase con Javascript para reescribir los estilos. 
<pre><code>:root {
--theme-bg: hsl(216,100%,99%);
--theme-bg-alt: hsl(220,20%,97.1%);
--theme-border: hsl(222,21.7%,91%);
--theme-lighter: hsl(214,16%,57.1%);
--theme-light: hsl(218,14%,46.1%);
--theme-text: hsl(216,11.2%,34.9%);
--theme-title: hsl(219,17.1%,16.1%);
}

.dark {
--theme-dark-bg: hsl(203,26.7%,5.9%);
--theme-dark-bg-alt: hsl(204,29.4%,10%);
--theme-dark-border: hsl(207,23.9%,22.2%);
--theme-dark-lighter: hsl(200,8.2%,64.1%);
--theme-dark-light: hsl(203,9.8%,73.9%);
 --theme-dark-text: hsl(202,9.8%,83.9%);
--theme-dark-title: hsl(240,4%,95.1%);
}
</code></pre>
---
**Opción Bonita (Quedé sorpredido):**
Con una Media Querie podemos aplicar los estilos con el tema que tenga aplicado el usuario al navegador en ese momento

[Documentación de prefers-color-scheme](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme)
<pre><code>:root {
--theme-bg: hsl(216,100%,99%);
--theme-bg-alt: hsl(220,20%,97.1%);
--theme-border: hsl(222,21.7%,91%);
--theme-lighter: hsl(214,16%,57.1%);
--theme-light: hsl(218,14%,46.1%);
--theme-text: hsl(216,11.2%,34.9%);
--theme-title: hsl(219,17.1%,16.1%);
}

@media (prefers-color-scheme: dark) {
	:root {
	--theme-dark-bg: hsl(203,26.7%,5.9%);
	--theme-dark-bg-alt: hsl(204,29.4%,10%);
	--theme-dark-border: hsl(207,23.9%,22.2%);
	--theme-dark-lighter: hsl(200,8.2%,64.1%);
	--theme-dark-light: hsl(203,9.8%,73.9%);
	--theme-dark-text: hsl(202,9.8%,83.9%);
	--theme-dark-title: hsl(240,4%,95.1%);
	}
}
</code></pre>