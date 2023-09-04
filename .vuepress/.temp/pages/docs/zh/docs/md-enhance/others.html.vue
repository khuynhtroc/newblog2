<template><div><p>::: info
默认不启用这些功能。
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>对于没有启用的功能，与它们相关的代码并不会被打包。</p>
</div>
<p>通过插件 <RouterLink to="/zh/docs/plugins/md-plus/">plugin-md-plus</RouterLink> 来在 Markdown 中加入更多语法和功能。目前支持：</p>
<ul>
<li>脚注</li>
<li>高亮标记</li>
<li>下标</li>
<li>上标</li>
</ul>
<p>你可以一键启用所有功能：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">mdPlus</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">all</span><span class="token operator">:</span> <span class="token boolean">true</span> <span class="token comment">// 全部启用（默认：false）</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>也可以分别启用：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">mdPlus</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">footnote</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span> <span class="token comment">// 脚注（默认：false）</span>
      <span class="token literal-property property">mark</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span> <span class="token comment">// 高亮标记（默认：false）</span>
      <span class="token literal-property property">sub</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span> <span class="token comment">// 下标（默认：false）</span>
      <span class="token literal-property property">sup</span><span class="token operator">:</span> <span class="token boolean">true</span> <span class="token comment">// 上标（默认：false）</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="脚注" tabindex="-1"><a class="header-anchor" href="#脚注" aria-hidden="true">#</a> 脚注</h2>
<p>给文字加上脚注<a href="%E8%84%9A%E6%B3%A8%E5%86%85%E5%AE%B9">^1</a></p>
<details class="custom-container details"><summary>语法</summary>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>给文字加上脚注[^1]

[^1]: 脚注内容
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></details>
<h2 id="高亮标记" tabindex="-1"><a class="header-anchor" href="#高亮标记" aria-hidden="true">#</a> 高亮标记</h2>
<p>高亮标记重要的内容：衬衫的价格是 ==九磅十五便士==</p>
<details class="custom-container details"><summary>语法</summary>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>衬衫的价格是 ==九磅十五便士==
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></details>
<h2 id="下标" tabindex="-1"><a class="header-anchor" href="#下标" aria-hidden="true">#</a> 下标</h2>
<p>H~2~O</p>
<details class="custom-container details"><summary>语法</summary>
<div class="language-markdown line-numbers-mode" data-ext="md"><pre v-pre class="language-markdown"><code>H<span class="token strike"><span class="token punctuation">~</span><span class="token content">2</span><span class="token punctuation">~</span></span>O
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></details>
<h2 id="上标" tabindex="-1"><a class="header-anchor" href="#上标" aria-hidden="true">#</a> 上标</h2>
<p>29^th^</p>
<details class="custom-container details"><summary>语法</summary>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>29^th^
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></details>
<hr>
</div></template>


