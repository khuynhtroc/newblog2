<template><div><p>::: info
This feature is disabled by default.
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>Code related to the disabled features will not be included in your site's bundle files.</p>
</div>
<h2 id="configuration" tabindex="-1"><a class="header-anchor" href="#configuration" aria-hidden="true">#</a> Configuration</h2>
<p>Use JavaScript charting library <a href="https://www.chartjs.org" target="_blank" rel="noopener noreferrer">Chart.js<ExternalLinkIcon/></a> in Markdown via <RouterLink to="/docs/plugins/chart/">plugin-chart</RouterLink>:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">chartjs</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="highlight-lines"><br><br><div class="highlight-line">&nbsp;</div><br><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>If you want to customize the token of the fenced code block (which is <code v-pre>chart</code> by default):</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">chartjs</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">token</span><span class="token operator">:</span> <span class="token string">"chartjs"</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="highlight-lines"><br><br><br><div class="highlight-line">&nbsp;</div><br><br><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="syntax" tabindex="-1"><a class="header-anchor" href="#syntax" aria-hidden="true">#</a> Syntax</h2>
<p>The token of the code block should be <code v-pre>chart</code> (or your custom one), for example:</p>
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
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><details class="custom-container details"><summary>Code</summary>
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
<p>The <strong>key</strong> should be in quotes, or some unexpected errors will occured.</p>
</div>
<p>Refer to the <a href="https://www.chartjs.org/docs/latest/" target="_blank" rel="noopener noreferrer">documentation of Chart.js<ExternalLinkIcon/></a> for more information.</p>
</div></template>


