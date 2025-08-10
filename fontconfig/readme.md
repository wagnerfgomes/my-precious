# font-config.scss

Este arquivo SCSS define um sistema de configuração tipográfica responsiva para projetos web, facilitando o ajuste de tamanhos de fonte, pesos e famílias de acordo com diferentes breakpoints (mobile, tablet, desktop).

## Variáveis Principais

-   **Tamanhos base:**  
    `$size-base-mobile`, `$size-base-tablet`, `$size-base-desktop`  
    Define o tamanho base da fonte para cada dispositivo.

-   **Razão tipográfica:**  
    `$text-ratio-mobile`, `$text-ratio-tablet`, `$text-ratio-laptop-desktop`  
    Controla a progressão dos tamanhos das fontes.

-   **Breakpoints:**  
    `$breakpoint-mobile`, `$breakpoint-tablet`, `$breakpoint-laptop`, `$breakpoint-desktop`  
    Define os pontos de quebra para responsividade.

-   **Famílias de fonte:**  
    `$font-title`, `$font-body`  
    Define as fontes para títulos e textos.

## Funções

-   **size($base, $ratio, $step, $unit: px):**  
    Calcula o tamanho da fonte baseado na razão tipográfica e no passo desejado.
    **passo: é o nível de hierarquia da fonte acima da base. Ex: para 4 passos temos: h1 = 4, h2 = 3, h3 = 2 e base = 1**

## Classes CSS

-   **Títulos:**  
    `.title-1` até `.title-6`  
    Tamanhos e pesos progressivos para hierarquia de títulos.

-   **Texto:**  
    `.font-body`, `.font-body-2`  
    Define estilos para textos principais e secundários.

-   **Tooltip:**  
    `.tooltip`  
    Estilo específico para tooltips.

## Responsividade

Os tamanhos de fonte são ajustados automaticamente para tablet e desktop usando media queries, garantindo boa legibilidade em diferentes dispositivos.

## Como usar

1. instale o Sass globalmente (acho que só funciona globalmente):

    ```bash
    npm install -g sass
    ```

2. Importe o arquivo SCSS no seu projeto.

3. Rode o compilador:
   
   ```bash
   sass --watch font-confg.scss seu-arquivo.css
   ```
    
4. Utilize as classes `.title-*`, `.font-body`, `.tooltip` nos elementos HTML conforme a hierarquia e contexto desejados.

5. Ajuste as variáveis conforme a identidade visual do seu projeto.

---

**Exemplo de uso:**

```html
<h1 class="title-1">Título Principal</h1>
<p class="font-body">Texto do corpo.</p>
<span class="tooltip">Dica</span>
```

