<template><div><p>::: info
This feature is enabled by default.
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>Code related to the disabled features will not be included in your site's bundle files.</p>
</div>
<p>The reading time estimation will be shown on the head of the article by default, supported by <RouterLink to="/docs/plugins/reading-time/">plugin-reading-time</RouterLink>.</p>
<h2 id="configuration" tabindex="-1"><a class="header-anchor" href="#configuration" aria-hidden="true">#</a> Configuration</h2>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">readingTime</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">excludes</span><span class="token operator">:</span> <span class="token punctuation">[</span><span class="token string">"/url1"</span><span class="token punctuation">,</span> <span class="token string">"/url2/.*"</span><span class="token punctuation">]</span><span class="token punctuation">,</span>  <span class="token comment">// exclude pages by their path via a regular expression (optional, default: [])</span>
      <span class="token literal-property property">includes</span> <span class="token operator">:</span> <span class="token punctuation">[</span><span class="token string">"/url1"</span><span class="token punctuation">,</span> <span class="token string">"/url2/.*"</span><span class="token punctuation">]</span><span class="token punctuation">,</span>  <span class="token comment">// include pages by their path via a regular expression, if `includes` is specified, `excludes` will be ignored (optional, default: [])</span>
      <span class="token literal-property property">wordsPerMinuteCN</span><span class="token operator">:</span> <span class="token number">500</span><span class="token punctuation">,</span>  <span class="token comment">// number of Chinese words per minute a user can read (optional, default: 300)</span>
      <span class="token literal-property property">wordsPerMinuteEN</span><span class="token operator">:</span> <span class="token number">200</span><span class="token punctuation">,</span>  <span class="token comment">// number of English words per minute a user can read (optional, default: 160)</span>
      <span class="token literal-property property">excludeCodeBlock</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>  <span class="token comment">// exclude all content inside code blocks or not (optional, default: false)</span>
      <span class="token literal-property property">excludeTexBlock</span><span class="token operator">:</span> <span class="token boolean">true</span>    <span class="token comment">// exclude all content inside tex blocks or not (optional, default: false)</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="override" tabindex="-1"><a class="header-anchor" href="#override" aria-hidden="true">#</a> Override</h2>
<p>You can override reading time in the front matter of each article by:</p>
<div class="language-yaml line-numbers-mode" data-ext="yml"><pre v-pre class="language-yaml"><code><span class="token key atrule">title</span><span class="token punctuation">:</span> Hello Word
<span class="token key atrule">readingTime</span><span class="token punctuation">:</span> <span class="token punctuation">{</span> <span class="token key atrule">minutes</span><span class="token punctuation">:</span> <span class="token number">3</span> <span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="disable" tabindex="-1"><a class="header-anchor" href="#disable" aria-hidden="true">#</a> Disable</h2>
<p>Or if you want to disable this feature:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">readingTime</span><span class="token operator">:</span> <span class="token boolean">false</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></div></template>


