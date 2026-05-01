
# 🏟️ Arena LLM – Comparador de Modelos Q4

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Open in Browser](https://img.shields.io/badge/Open%20in-Browser-blue)](https://github.com/tuusuario/arena-llm)

**Arena LLM** es una aplicación web estática (single‑page) para comparar modelos de lenguaje **cuantizados en 4 bits (Q4)**.  
Selecciona dos modelos, analiza sus puntos fuertes, revisa gráficas comparativas y descubre cuál se adapta mejor a tu caso de uso.

---

## 📸 Captura de Pantalla

![Arena LLM Screenshot](screenshot.png)  
*Ejemplo de comparación entre Qwen 2.5 7B y Qwen 2.5 Coder 7B.*

---

## 🚀 Características

- ⚔️ **Comparación 1 vs 1** – Enfrenta directamente cualquier par de los 22 modelos incluidos.
- 📊 **Gráficas interactivas** – Radar de habilidades y barras comparativas con Chart.js.
- 💪 **Análisis de fortalezas** – Cada modelo muestra sus puntos fuertes y para qué destaca.
- 🏆 **Veredicto automático** – El sistema analiza los benchmarks y emite un veredicto detallado.
- 🎲 **Batalla aleatoria** – Descubre combinaciones inesperadas con un solo clic.
- ⚡ **Totalmente en cliente** – Sin backend, sin dependencias externas; abre `index.html` y listo.

---

## 🧠 Modelos incluidos (todos en Q4)

| Familia | Modelos |
|--------|---------|
| **Qwen 2.5** | Qwen 2.5 3B, Qwen 2.5 7B |
| **Qwen 2.5 Coder** | Qwen 2.5 Coder 3B, Qwen 2.5 Coder 7B |
| **Qwen 3** | Qwen 3 4B, Qwen 3 8B, Qwen 3 4B Thinking |
| **Qwen 3.5** | Qwen 3.5 4B, Qwen 3.5 9B |
| **Llama** | Llama 3.2 3B, Llama 3.1 8B |
| **DeepSeek R1** | DeepSeek R1 Distill Llama 8B, DeepSeek R1 Distill Qwen 7B, DeepSeek R1 0528 Qwen3 8B |
| **Gemma** | Gemma 3 4B, Gemma 4 e2B, Gemma 4 e4B |
| **Compactos** | SmolLM3 3B, Helium 2B, Phi-3.5 Mini |
| **Otros** | Mistral 3 7B, GLM-4 9B Chat |

*Cada modelo se evalúa en: Conocimiento General, Programación, Razonamiento Matemático, Velocidad, Seguimiento de Instrucciones y Soporte Multilingüe.*

---

## 📦 Cómo usar

1. **Clona el repositorio**
   ```bash
   git clone https://github.com/tuusuario/arena-llm.git
   cd arena-llm
   ```

2. **Abre el archivo `index.html`**  
   Haz doble clic sobre `index.html` o ábrelo con tu navegador favorito (Chrome, Firefox, Edge, Safari).  
   *No necesitas servidor ni instalar nada.*

3. **Elige dos modelos**  
   Usa los menús desplegables para seleccionar el Modelo A y el Modelo B.

4. **Explora los resultados**  
   Las gráficas, fortalezas y el veredicto se actualizan automáticamente.

---

## 🔧 Personalización

Puedes modificar fácilmente los benchmarks, las fortalezas o añadir nuevos modelos editando el objeto `modelsDB` que se encuentra dentro del `<script>` en `index.html`.  
Cada modelo tiene esta estructura:

```javascript
'qwen25-3b': {
  id: 'qwen25-3b',
  name: 'Qwen 2.5 3B',
  family: 'Qwen 2.5',
  params: '3B',
  category: 'General',
  contextWindow: '32K',
  color: '#7c5cfc',
  description: 'Modelo compacto balanceado...',
  strengths: [ ... ],
  bestFor: [ ... ],
  benchmarks: {
    generalKnowledge: 58,
    coding: 42,
    mathReasoning: 48,
    speed: 88,
    instructionFollowing: 55,
    multilingual: 72
  }
}
```

Simplemente copia un objeto existente, ajusta los valores y añade la entrada al `<select>` correspondiente.

---

## 🛠️ Tecnologías

- **HTML5 / CSS3 / JavaScript (vanilla)**
- [Chart.js](https://www.chartjs.org/) (CDN) para las visualizaciones
- Diseño responsive con CSS Grid y Flexbox
- Sin frameworks adicionales

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.

---

## 🤝 Contribuciones

¡Toda ayuda es bienvenida!  
Si quieres añadir más modelos, mejorar la UI o corregir algún dato:

1. Haz un fork del repo.
2. Crea una rama (`git checkout -b mejora/modelo-nuevo`).
3. Haz tus cambios y commitea.
4. Haz push y abre un Pull Request.

También puedes abrir un *issue* para sugerir mejoras o reportar errores.

---

## ⭐ Créditos

Desarrollado con pasión por la comunidad LLM.  
Datos de benchmarks inspirados en evaluaciones públicas y experiencia práctica con modelos cuantizados.  
¡Dale una estrella al repo si te resulta útil! ⭐
