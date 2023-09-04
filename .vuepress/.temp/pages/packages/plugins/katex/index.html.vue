<template><div><h1 id="renovamen-vuepress-plugin-katex-next" tabindex="-1"><a class="header-anchor" href="#renovamen-vuepress-plugin-katex-next" aria-hidden="true">#</a> @renovamen/vuepress-plugin-katex@next</h1>
<p><a href="https://www.npmjs.com/package/@renovamen/vuepress-plugin-katex/v/next" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/npm/v/@renovamen/vuepress-plugin-katex/next.svg?style=flat-square&amp;logo=npm" alt="npm"><ExternalLinkIcon/></a> <a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/katex.html" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Docs-@renovamen/vuepress--plugin--katex-26A2FF?style=flat-square" alt="docs"><ExternalLinkIcon/></a> <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache--2.0-green?style=flat-square" alt="license"></a></p>
<p>Plugin <code v-pre>@renovamen/vuepress-plugin-katex@next</code> for adding <a href="https://katex.org/" target="_blank" rel="noopener noreferrer">KaTeX<ExternalLinkIcon/></a> to <a href="https://v2.vuepress.vuejs.org/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a> to support mathematical formulas rendering in Markdown. This plugin is based on <a href="https://github.com/waylonflinn/markdown-it-katex" target="_blank" rel="noopener noreferrer">waylonflinn/markdown-it-katex<ExternalLinkIcon/></a>.</p>
<p><a href="https://katex.org/" target="_blank" rel="noopener noreferrer">KaTeX<ExternalLinkIcon/></a> is a faster alternative to MathJax (see <a href="https://www.intmath.com/cg5/katex-mathjax-comparison.php" target="_blank" rel="noopener noreferrer">here<ExternalLinkIcon/></a>).</p>
<p><a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/katex.html" target="_blank" rel="noopener noreferrer">Demo<ExternalLinkIcon/></a></p>
<p> </p>
<h2 id="install" tabindex="-1"><a class="header-anchor" href="#install" aria-hidden="true">#</a> Install</h2>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token comment"># pnpm</span>
<span class="token function">pnpm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-katex@next
<span class="token comment"># yarn</span>
<span class="token function">yarn</span> <span class="token function">add</span> @renovamen/vuepress-plugin-katex@next
<span class="token comment"># npm</span>
<span class="token function">npm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-katex@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>Then add it to your <code v-pre>.vuepress/config.js</code>:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> <span class="token punctuation">{</span> katexPlugin <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">require</span><span class="token punctuation">(</span><span class="token string">"@renovamen/vuepress-plugin-katex"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token function">katexPlugin</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>You can also enable it with some <a href="https://katex.org/docs/options.html" target="_blank" rel="noopener noreferrer">KaTeX options<ExternalLinkIcon/></a>:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> <span class="token punctuation">{</span> katexPlugin <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">require</span><span class="token punctuation">(</span><span class="token string">"@renovamen/vuepress-plugin-katex"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token function">katexPlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
      <span class="token string-property property">"throwOnError"</span><span class="token operator">:</span> <span class="token boolean">false</span><span class="token punctuation">,</span>
      <span class="token string-property property">"errorColor"</span><span class="token operator">:</span> <span class="token string">"#cc0000"</span>
    <span class="token punctuation">}</span><span class="token punctuation">)</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p> </p>
<h2 id="usage" tabindex="-1"><a class="header-anchor" href="#usage" aria-hidden="true">#</a> Usage</h2>
<p><a href="https://katex.org/docs/supported.html" target="_blank" rel="noopener noreferrer">Here<ExternalLinkIcon/></a> is a list of TeX functions supported by KaTeX.</p>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>Inline math: E = mc^2

Display math:

$$
i\hbar\frac{\partial \psi}{\partial t} = \frac{-\hbar^2}{2m} ( \frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2} + \frac{\partial^2}{\partial z^2} ) \psi + V \psi.
$$
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p> </p>
<h2 id="license" tabindex="-1"><a class="header-anchor" href="#license" aria-hidden="true">#</a> License</h2>
<p><a href="https://github.com/Renovamen/vuepress-theme-gungnir/blob/main/packages/plugins/katex/LICENSE" target="_blank" rel="noopener noreferrer">MIT<ExternalLinkIcon/></a></p>
</div></template>


