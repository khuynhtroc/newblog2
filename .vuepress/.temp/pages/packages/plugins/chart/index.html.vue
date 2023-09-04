<template><div><h1 id="vuepress-plugin-chart-next" tabindex="-1"><a class="header-anchor" href="#vuepress-plugin-chart-next" aria-hidden="true">#</a> vuepress-plugin-chart@next</h1>
<p><a href="https://www.npmjs.com/package/vuepress-plugin-chart/v/next" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/npm/v/vuepress-plugin-chart/next.svg?style=flat-square&amp;logo=npm" alt="npm"><ExternalLinkIcon/></a> <a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/chart.html" target="_blank" rel="noopener noreferrer"><img src="https://img.shields.io/badge/Docs-vuepress--plugin--chart-26A2FF?style=flat-square" alt="docs"><ExternalLinkIcon/></a> <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache--2.0-green?style=flat-square" alt="license"></a></p>
<p>Plugin <code v-pre>vuepress-plugin-chart@next</code> for adding JavaScript charting library <a href="https://www.chartjs.org" target="_blank" rel="noopener noreferrer">Chart.js<ExternalLinkIcon/></a> to <a href="https://v2.vuepress.vuejs.org/" target="_blank" rel="noopener noreferrer">VuePress 2<ExternalLinkIcon/></a> to create interactive charts in Markdown.</p>
<p><a href="https://v2-vuepress-theme-gungnir.vercel.app/docs/plugins/chart.html" target="_blank" rel="noopener noreferrer">Demo<ExternalLinkIcon/></a></p>
<p> </p>
<h2 id="install" tabindex="-1"><a class="header-anchor" href="#install" aria-hidden="true">#</a> Install</h2>
<div class="language-bash line-numbers-mode" data-ext="sh"><pre v-pre class="language-bash"><code><span class="token comment"># pnpm</span>
<span class="token function">pnpm</span> <span class="token function">install</span> vuepress-plugin-chart@next
<span class="token comment"># yarn</span>
<span class="token function">yarn</span> <span class="token function">add</span> vuepress-plugin-chart@next
<span class="token comment"># npm</span>
<span class="token function">npm</span> <span class="token function">install</span> vuepress-plugin-chart@next
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>Then add it to your <code v-pre>.vuepress/config.js</code>:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> <span class="token punctuation">{</span> chartPlugin <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">require</span><span class="token punctuation">(</span><span class="token string">"vuepress-plugin-chart"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">[</span>
    <span class="token function">chartPlugin</span><span class="token punctuation">(</span><span class="token punctuation">)</span>
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
<p>Default: <code v-pre>&quot;chart&quot;</code></p>
</li>
<li>
<p>Details: Custom token of the fenced code block.</p>
</li>
</ul>
<p> </p>
<h2 id="usage" tabindex="-1"><a class="header-anchor" href="#usage" aria-hidden="true">#</a> Usage</h2>
<p>The token info of the code block should be <code v-pre>chart</code> (or <code v-pre>options.token</code> if you set), for example:</p>
<div class="language-json line-numbers-mode" data-ext="json"><pre v-pre class="language-json"><code>```chart
<span class="token punctuation">{</span>
  <span class="token property">"type"</span><span class="token operator">:</span> <span class="token string">"doughnut"</span><span class="token punctuation">,</span>
  <span class="token property">"data"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"datasets"</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token punctuation">{</span>
      <span class="token property">"data"</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token number">10</span><span class="token punctuation">,</span> <span class="token number">20</span><span class="token punctuation">,</span> <span class="token number">30</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
      <span class="token property">"backgroundColor"</span><span class="token operator">:</span> <span class="token punctuation">[</span>
        <span class="token string">"rgba(255, 99, 132)"</span><span class="token punctuation">,</span>
        <span class="token string">"rgba(255, 206, 86)"</span><span class="token punctuation">,</span>
        <span class="token string">"rgba(54, 162, 235)"</span>
      <span class="token punctuation">]</span>
    <span class="token punctuation">}</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token property">"labels"</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token string">"Red"</span><span class="token punctuation">,</span> <span class="token string">"Yellow"</span><span class="token punctuation">,</span> <span class="token string">"Blue"</span><span class="token punctuation">]</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
```
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p><strong>Notice:</strong> The <strong>key</strong> should be in quotes, or some unexpected errors will occured.</p>
<p>Functions should be stringified before being passed through <code v-pre>callback</code>. The following example shows how to change the tick marks of y-axis using <code v-pre>callback</code>:</p>
<div class="language-json line-numbers-mode" data-ext="json"><pre v-pre class="language-json"><code>```chart
<span class="token punctuation">{</span>
  <span class="token property">"type"</span><span class="token operator">:</span> <span class="token string">"bar"</span><span class="token punctuation">,</span>
  <span class="token property">"data"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"labels"</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token string">"Red"</span><span class="token punctuation">,</span> <span class="token string">"Blue"</span><span class="token punctuation">,</span> <span class="token string">"Yellow"</span><span class="token punctuation">,</span> <span class="token string">"Green"</span><span class="token punctuation">,</span> <span class="token string">"Purple"</span><span class="token punctuation">,</span> <span class="token string">"Orange"</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token property">"datasets"</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token punctuation">{</span>
      <span class="token property">"label"</span><span class="token operator">:</span> <span class="token string">"Salary"</span><span class="token punctuation">,</span>
      <span class="token property">"data"</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token number">12</span><span class="token punctuation">,</span> <span class="token number">19</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">,</span> <span class="token number">5</span><span class="token punctuation">,</span> <span class="token number">2</span><span class="token punctuation">,</span> <span class="token number">3</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
      <span class="token property">"backgroundColor"</span><span class="token operator">:</span> <span class="token punctuation">[</span>
        <span class="token string">"rgba(255, 99, 132, 1)"</span><span class="token punctuation">,</span>
        <span class="token string">"rgba(54, 162, 235, 1)"</span><span class="token punctuation">,</span>
        <span class="token string">"rgba(255, 206, 86, 1)"</span><span class="token punctuation">,</span>
        <span class="token string">"rgba(75, 192, 192, 1)"</span><span class="token punctuation">,</span>
        <span class="token string">"rgba(153, 102, 255, 1)"</span><span class="token punctuation">,</span>
        <span class="token string">"rgba(255, 159, 64, 1)"</span>
      <span class="token punctuation">]</span>
    <span class="token punctuation">}</span><span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token property">"options"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"scales"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token property">"y"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token property">"ticks"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
          <span class="token property">"beginAtZero"</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
          <span class="token property">"callback"</span><span class="token operator">:</span> <span class="token string">"function(value){ return '￥' + value + 'k'; }"</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
```
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>Refer to the <a href="https://www.chartjs.org/docs/latest/" target="_blank" rel="noopener noreferrer">documentation of Chart.js<ExternalLinkIcon/></a> for more information.</p>
<p> </p>
<h2 id="license" tabindex="-1"><a class="header-anchor" href="#license" aria-hidden="true">#</a> License</h2>
<p><a href="https://github.com/Renovamen/vuepress-theme-gungnir/blob/main/packages/plugins/chart/LICENSE" target="_blank" rel="noopener noreferrer">MIT<ExternalLinkIcon/></a></p>
</div></template>


