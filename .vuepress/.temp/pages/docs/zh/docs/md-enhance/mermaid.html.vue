<template><div><p>::: info
默认不启用该功能。
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>对于没有启用的功能，与它们相关的代码并不会被打包。</p>
</div>
<h2 id="配置" tabindex="-1"><a class="header-anchor" href="#配置" aria-hidden="true">#</a> 配置</h2>
<p>通过插件 <RouterLink to="/zh/docs/plugins/mermaid/">plugin-mermaid</RouterLink> 来在 Markdown 中使用 <a href="https://mermaid-js.github.io" target="_blank" rel="noopener noreferrer">Mermaid<ExternalLinkIcon/></a>，从而在文章中加入流程图、状态图、时序图、甘特图等：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">mermaid</span><span class="token operator">:</span> <span class="token boolean">true</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="highlight-lines"><br><br><div class="highlight-line">&nbsp;</div><br><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>如果你想自定义代码块 token（默认为 <code v-pre>mermaidjs</code>）：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">mermaid</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">token</span><span class="token operator">:</span> <span class="token string">"mermaid"</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="highlight-lines"><br><br><br><div class="highlight-line">&nbsp;</div><br><br><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="主题" tabindex="-1"><a class="header-anchor" href="#主题" aria-hidden="true">#</a> 主题</h2>
<p>Mermaid 支持<a href="https://github.com/mermaid-js/mermaid/tree/develop/src/themes" target="_blank" rel="noopener noreferrer">多种主题<ExternalLinkIcon/></a>。Gungnir 主题默认在亮色模式下使用 <code v-pre>default</code> 主题，在夜间模式下使用 <code v-pre>dark</code> 主题。你也可以通过修改插件配置项来使用其他主题：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">mermaid</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token string">"default"</span><span class="token punctuation">,</span>  <span class="token comment">// 默认："default"</span>
      <span class="token literal-property property">darkTheme</span><span class="token operator">:</span> <span class="token string">"dark"</span>  <span class="token comment">// 默认："dark"</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>更多细节和用法请参考 <RouterLink to="/zh/docs/plugins/mermaid.html#%E9%85%8D%E7%BD%AE%E9%A1%B9">plugin-mermaid</RouterLink> 的文档。</p>
<h2 id="语法" tabindex="-1"><a class="header-anchor" href="#语法" aria-hidden="true">#</a> 语法</h2>
<p>代码块的 token 需要为 <code v-pre>mermaidjs</code>（或你自定义的 token），例子：</p>
<div class="language-mermaidjs line-numbers-mode" data-ext="mermaidjs"><pre v-pre class="language-mermaidjs"><code>sequenceDiagram
  Alice-&gt;John: Hello John, how are you?
  loop Every minute
    John--&gt;Alice: Great!
  end
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><details class="custom-container details"><summary>代码</summary>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>```mermaidjs
sequenceDiagram
  Alice->John: Hello John, how are you?
  loop Every minute
    John-->Alice: Great!
  end
```
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></details>
<p>更详细的用法可以参考 <a href="https://mermaid-js.github.io" target="_blank" rel="noopener noreferrer">Mermaid 文档<ExternalLinkIcon/></a>。</p>
</div></template>


