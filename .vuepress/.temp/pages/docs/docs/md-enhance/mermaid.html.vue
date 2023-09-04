<template><div><p>::: info
This feature is disabled by default.
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>Code related to the disabled features will not be included in your site's bundle files.</p>
</div>
<h2 id="configuration" tabindex="-1"><a class="header-anchor" href="#configuration" aria-hidden="true">#</a> Configuration</h2>
<p>Use <a href="https://mermaid-js.github.io" target="_blank" rel="noopener noreferrer">Mermaid<ExternalLinkIcon/></a> via <RouterLink to="/docs/plugins/mermaid.html">plugin-mermaid</RouterLink> to create complex diagrams in Markdown:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">mermaid</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="highlight-lines"><br><br><div class="highlight-line">&nbsp;</div><br><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>If you want to customize the token of the fenced code block (which is <code v-pre>mermaidjs</code> by default):</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">mermaid</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">token</span><span class="token operator">:</span> <span class="token string">"mermaid"</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="highlight-lines"><br><br><br><div class="highlight-line">&nbsp;</div><br><br><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="themes" tabindex="-1"><a class="header-anchor" href="#themes" aria-hidden="true">#</a> Themes</h2>
<p>Mermaid supports <a href="https://github.com/mermaid-js/mermaid/tree/develop/src/themes" target="_blank" rel="noopener noreferrer">multiple themes<ExternalLinkIcon/></a>. By default, Gungnir uses <code v-pre>default</code> theme in light mode and <code v-pre>dark</code> in dark mode. You can also use other themes by configuring the plugin options:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">mermaid</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token string">"default"</span><span class="token punctuation">,</span>  <span class="token comment">// default: "default"</span>
      <span class="token literal-property property">darkTheme</span><span class="token operator">:</span> <span class="token string">"dark"</span>  <span class="token comment">// default: "dark"</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>Also see <RouterLink to="/docs/plugins/mermaid.html#options">plugin-mermaid</RouterLink> for more details.</p>
<h2 id="syntax" tabindex="-1"><a class="header-anchor" href="#syntax" aria-hidden="true">#</a> Syntax</h2>
<p>The token info of the code block should be <code v-pre>mermaidjs</code> (or your custom one), for example:</p>
<div class="language-mermaidjs line-numbers-mode" data-ext="mermaidjs"><pre v-pre class="language-mermaidjs"><code>sequenceDiagram
  Alice-&gt;John: Hello John, how are you?
  loop Every minute
    John--&gt;Alice: Great!
  end
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><details class="custom-container details"><summary>Code</summary>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>```mermaidjs
sequenceDiagram
  Alice->John: Hello John, how are you?
  loop Every minute
    John-->Alice: Great!
  end
```
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></details>
<p>Refer to the <a href="https://mermaid-js.github.io" target="_blank" rel="noopener noreferrer">documentation of Mermaid<ExternalLinkIcon/></a> for more information.</p>
</div></template>


