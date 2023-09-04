<template><div><p>::: info
These features are disabled by default.
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>Code related to the disabled features will not be included in your site's bundle files.</p>
</div>
<p><a href="/plugins/md-plus">plugin-md-plus</a> is used for adding more syntax in Markdown. It now supports:</p>
<ul>
<li>Footnote</li>
<li>Mark</li>
<li>Subscript</li>
<li>Superscript</li>
</ul>
<p>You can enable all features simply by:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">mdPlus</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">all</span><span class="token operator">:</span> <span class="token boolean">true</span> <span class="token comment">// enable all features (default: false)</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>or enable them separately:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">mdPlus</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">footnote</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span> <span class="token comment">// Footnote (default: false)</span>
      <span class="token literal-property property">mark</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span> <span class="token comment">// Mark (default: false)</span>
      <span class="token literal-property property">sub</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span> <span class="token comment">// Subscript (default: false)</span>
      <span class="token literal-property property">sup</span><span class="token operator">:</span> <span class="token boolean">true</span> <span class="token comment">// Superscript (default: false)</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="footnote" tabindex="-1"><a class="header-anchor" href="#footnote" aria-hidden="true">#</a> Footnote</h2>
<p>Add footnotes for text[^1]</p>
<details class="custom-container details"><summary>Syntax</summary>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>Add footnotes for text[^1]

[^1]: Write your footnote here.
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></details>
<h2 id="mark" tabindex="-1"><a class="header-anchor" href="#mark" aria-hidden="true">#</a> Mark</h2>
<p>Mark important information: &quot;Excuse me. Can you tell me how much the shirt is?&quot; &quot;Yes, it's ==nine fifteen==.&quot;</p>
<details class="custom-container details"><summary>Syntax</summary>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>Yes, it's ==nine fifteen==.
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></details>
<h2 id="subscript" tabindex="-1"><a class="header-anchor" href="#subscript" aria-hidden="true">#</a> Subscript</h2>
<p>H~2~O</p>
<details class="custom-container details"><summary>Syntax</summary>
<div class="language-markdown line-numbers-mode" data-ext="md"><pre v-pre class="language-markdown"><code>H<span class="token strike"><span class="token punctuation">~</span><span class="token content">2</span><span class="token punctuation">~</span></span>O
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></details>
<h2 id="superscript" tabindex="-1"><a class="header-anchor" href="#superscript" aria-hidden="true">#</a> Superscript</h2>
<p>29^th^</p>
<details class="custom-container details"><summary>Syntax</summary>
<div class="language-text line-numbers-mode" data-ext="text"><pre v-pre class="language-text"><code>29^th^
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></details>
<hr>
<p>[^1]: Write your footnote here.</p>
</div></template>


