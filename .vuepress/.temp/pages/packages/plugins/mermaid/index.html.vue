<template><div><h1 id="renovamen-vuepress-plugin-mermaid-next" tabindex="-1"><a class="header-anchor" href="#renovamen-vuepress-plugin-mermaid-next" aria-hidden="true">#</a> @renovamen/vuepress-plugin-mermaid@next</h1>
<p><a href="https://www.npmjs.com/package/@renovamen/vuepress-plugin-mermaid/v/next" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/npm/v/@renovamen/vuepress-plugin-mermaid/next.svg?style=flat-square&amp;logo=npm" alt="npm"><ExternalLinkIcon/></a> <a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/mermaid.html" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Docs-@renovamen/vuepress--plugin--mermaid-26A2FF?style=flat-square" alt="docs"><ExternalLinkIcon/></a> <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache--2.0-green?style=flat-square" alt="license"></a></p>
<p>Plugin <code v-pre>@renovamen/vuepress-plugin-mermaid@next</code> for adding <a href="https://mermaid-js.github.io" target="_blank" rel="noopener noreferrer">Mermaid<ExternalLinkIcon/></a> to <a href="https://v2.vuepress.vuejs.org/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a> to create complex diagrams in Markdown.</p>
<p><a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/mermaid.html" target="_blank" rel="noopener noreferrer">Demo<ExternalLinkIcon/></a></p>
<p> </p>
<h2 id="install" tabindex="-1"><a class="header-anchor" href="#install" aria-hidden="true">#</a> Install</h2>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token comment"># pnpm</span>
<span class="token function">pnpm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-mermaid@next
<span class="token comment"># yarn</span>
<span class="token function">yarn</span> <span class="token function">add</span> @renovamen/vuepress-plugin-mermaid@next
<span class="token comment"># npm</span>
<span class="token function">npm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-mermaid@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>Then add it to your <code v-pre>.vuepress/config.js</code>:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> <span class="token punctuation">{</span> mermaidPlugin <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">require</span><span class="token punctuation">(</span><span class="token string">"@renovamen/vuepress-plugin-mermaid"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token function">mermaidPlugin</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p> </p>
<h2 id="options" tabindex="-1"><a class="header-anchor" href="#options" aria-hidden="true">#</a> Options</h2>
<h3 id="token" tabindex="-1"><a class="header-anchor" href="#token" aria-hidden="true">#</a> token</h3>
<ul>
<li>
<p>Type: <code v-pre>string</code></p>
</li>
<li>
<p>Default: <code v-pre>&quot;mermaidjs&quot;</code></p>
</li>
<li>
<p>Details: Custom token of the fenced code block.</p>
</li>
</ul>
<h3 id="theme" tabindex="-1"><a class="header-anchor" href="#theme" aria-hidden="true">#</a> theme</h3>
<ul>
<li>
<p>Type: <code v-pre>string</code></p>
</li>
<li>
<p>Default: <code v-pre>&quot;default&quot;</code></p>
</li>
<li>
<p>Details: Theme (<a href="https://github.com/mermaid-js/mermaid/tree/develop/src/themes" target="_blank" rel="noopener noreferrer">here<ExternalLinkIcon/></a> are all themes supported by Mermaid)</p>
</li>
</ul>
<h3 id="darktheme" tabindex="-1"><a class="header-anchor" href="#darktheme" aria-hidden="true">#</a> darkTheme</h3>
<ul>
<li>
<p>Type: <code v-pre>string</code></p>
</li>
<li>
<p>Default: <code v-pre>&quot;dark&quot;</code></p>
</li>
<li>
<p>Details: Theme for dark mode. Only works when <a href="#darkselector">darkSelector</a> and <a href="#darkclass">darkClass</a> are set.</p>
</li>
</ul>
<h3 id="darkselector" tabindex="-1"><a class="header-anchor" href="#darkselector" aria-hidden="true">#</a> darkSelector</h3>
<ul>
<li>
<p>Type: <code v-pre>string</code></p>
</li>
<li>
<p>Default: <code v-pre>undefined</code></p>
</li>
<li>
<p>Details</p>
<ul>
<li>A CSS selector for the plugin to select an element and check if the dark mode is enabled by <a href="#darkclass">darkClass</a></li>
<li>For default theme and Gungnir theme, this option should be <code v-pre>html</code></li>
</ul>
</li>
</ul>
<h3 id="darkclass" tabindex="-1"><a class="header-anchor" href="#darkclass" aria-hidden="true">#</a> darkClass</h3>
<ul>
<li>
<p>Type: <code v-pre>string</code></p>
</li>
<li>
<p>Default: <code v-pre>undefined</code></p>
</li>
<li>
<p>Details</p>
<ul>
<li>A class name for the plugin to check if the dark mode is enabled</li>
<li>For default theme and Gungnir theme, this option should be <code v-pre>dark</code></li>
</ul>
</li>
</ul>
<p><strong>Tips:</strong> The default theme and Gungnir theme will add a class name <code v-pre>dark</code> to the <code v-pre>html</code> element to enable dark mode.</p>
<p> </p>
<h2 id="usage" tabindex="-1"><a class="header-anchor" href="#usage" aria-hidden="true">#</a> Usage</h2>
<p>The token info of the code block should be <code v-pre>mermaidjs</code> (or <code v-pre>options.token</code> if you set), for example:</p>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>```mermaidjs
sequenceDiagram
  Alice->John: Hello John, how are you?
  loop Every minute
    John-->Alice: Great!
  end
```
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>Refer to the <a href="https://mermaid-js.github.io" target="_blank" rel="noopener noreferrer">documentation of Mermaid<ExternalLinkIcon/></a> for more information.</p>
<p> </p>
<h2 id="license" tabindex="-1"><a class="header-anchor" href="#license" aria-hidden="true">#</a> License</h2>
<p><a href="https://github.com/Renovamen/vuepress-theme-gungnir/blob/main/packages/plugins/mermaid/LICENSE" target="_blank" rel="noopener noreferrer">MIT<ExternalLinkIcon/></a></p>
</div></template>


