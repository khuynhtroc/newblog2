<template><div><h1 id="renovamen-vuepress-plugin-md-plus-next" tabindex="-1"><a class="header-anchor" href="#renovamen-vuepress-plugin-md-plus-next" aria-hidden="true">#</a> @renovamen/vuepress-plugin-md-plus@next</h1>
<p><a href="https://www.npmjs.com/package/@renovamen/vuepress-plugin-md-plus/v/next" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/npm/v/@renovamen/vuepress-plugin-md-plus/next.svg?style=flat-square&amp;logo=npm" alt="npm"><ExternalLinkIcon/></a> <a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/md-plus.html" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Docs-@renovamen/vuepress--plugin--md--plus-26A2FF?style=flat-square" alt="docs"><ExternalLinkIcon/></a> <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache--2.0-green?style=flat-square" alt="license"></a></p>
<p>A plugin for enhancing Markdown in <a href="https://v2.vuepress.vuejs.org/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a>. Now the following features are supported:</p>
<ul>
<li>footnote (supported by <a href="https://github.com/markdown-it/markdown-it-footnote" target="_blank" rel="noopener noreferrer">markdown-it-footnote<ExternalLinkIcon/></a>)</li>
<li>mark (supported by <a href="https://github.com/markdown-it/markdown-it-mark" target="_blank" rel="noopener noreferrer">markdown-it-footnote<ExternalLinkIcon/></a>)</li>
</ul>
<p><a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/md-plus.html" target="_blank" rel="noopener noreferrer">Demo<ExternalLinkIcon/></a></p>
<p> </p>
<h2 id="install" tabindex="-1"><a class="header-anchor" href="#install" aria-hidden="true">#</a> Install</h2>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token comment"># pnpm</span>
<span class="token function">pnpm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-md-plus@next
<span class="token comment"># yarn</span>
<span class="token function">yarn</span> <span class="token function">add</span> @renovamen/vuepress-plugin-md-plus@next
<span class="token comment"># npm</span>
<span class="token function">npm</span> <span class="token function">install</span> @renovamen/vuepress-plugin-md-plus@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p> </p>
<h2 id="configuration" tabindex="-1"><a class="header-anchor" href="#configuration" aria-hidden="true">#</a> Configuration</h2>
<p>You can enable all features simply by:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> <span class="token punctuation">{</span> mdPlusPlugin <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">require</span><span class="token punctuation">(</span><span class="token string">"@renovamen/vuepress-plugin-md-plus"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token function">mdPlusPlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
      <span class="token literal-property property">all</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>  <span class="token comment">// Enable all features or not, this will rewrite all the following options (default: false)</span>
    <span class="token punctuation">}</span><span class="token punctuation">)</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>or enable them separately:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code>module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token function">mdPlusPlugin</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
      <span class="token literal-property property">footnote</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>  <span class="token comment">// Enable footnote or not (default: false)</span>
      <span class="token literal-property property">mark</span><span class="token operator">:</span> <span class="token boolean">true</span>  <span class="token comment">// Enable mark or not (default: false)</span>
    <span class="token punctuation">}</span><span class="token punctuation">)</span>
  <span class="token punctuation">]</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p> </p>
<h2 id="usage" tabindex="-1"><a class="header-anchor" href="#usage" aria-hidden="true">#</a> Usage</h2>
<h3 id="footnote" tabindex="-1"><a class="header-anchor" href="#footnote" aria-hidden="true">#</a> Footnote</h3>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>Add footnotes for text[^1]

[^1]: Write your footnote here.
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="mark" tabindex="-1"><a class="header-anchor" href="#mark" aria-hidden="true">#</a> Mark</h3>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>Mark important information: "Excuse me. Can you tell me how much the shirt is?" "Yes, it's ==nine fifteen==."
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div><p> </p>
<h2 id="license" tabindex="-1"><a class="header-anchor" href="#license" aria-hidden="true">#</a> License</h2>
<p><a href="LICENSE">MIT</a></p>
</div></template>


