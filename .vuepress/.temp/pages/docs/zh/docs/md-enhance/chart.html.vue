<template><div><p>::: info
默认不启用该功能。
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>对于没有启用的功能，与它们相关的代码并不会被打包。</p>
</div>
<h2 id="配置" tabindex="-1"><a class="header-anchor" href="#配置" aria-hidden="true">#</a> 配置</h2>
<p>通过插件 <RouterLink to="/zh/docs/plugins/chart/">plugin-chart</RouterLink> 来在 Markdown 中使用 JavaScript 图表库 <a href="https://www.chartjs.org" target="_blank" rel="noopener noreferrer">Chart.js<ExternalLinkIcon/></a>：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">chartjs</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="highlight-lines"><br><br><div class="highlight-line">&nbsp;</div><br><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>如果你想自定义代码块 token（默认为 <code v-pre>chart</code>）：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">chartjs</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">token</span><span class="token operator">:</span> <span class="token string">"chartjs"</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="highlight-lines"><br><br><br><div class="highlight-line">&nbsp;</div><br><br><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="语法" tabindex="-1"><a class="header-anchor" href="#语法" aria-hidden="true">#</a> 语法</h2>
<p>代码块的 token 需要为 <code v-pre>chart</code>（或你自定义的 token），例子：</p>
<div class="language-chart line-numbers-mode" data-ext="chart"><pre v-pre class="language-chart"><code>{
  &quot;type&quot;: &quot;doughnut&quot;,
  &quot;data&quot;: {
    &quot;datasets&quot;: [{
      &quot;data&quot;: [10, 20, 30],
      &quot;backgroundColor&quot;: [
        &quot;rgba(255, 99, 132)&quot;,
        &quot;rgba(255, 206, 86)&quot;,
        &quot;rgba(54, 162, 235)&quot;
      ]
    }],
    &quot;labels&quot;: [&quot;Red&quot;, &quot;Yellow&quot;, &quot;Blue&quot;]
  }
}
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><details class="custom-container details"><summary>代码</summary>
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
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></details>
<div class="custom-container danger"><p class="custom-container-title">DANGER</p>
<p>key 值一定要加引号，否则会报错。</p>
</div>
<p>更详细的用法可以参考 <a href="https://www.chartjs.org/docs/latest/" target="_blank" rel="noopener noreferrer">Chart.js 文档<ExternalLinkIcon/></a>。</p>
</div></template>


