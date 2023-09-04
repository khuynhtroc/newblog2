<template><div><p>::: info
These features are disabled by default.
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>Code related to the disabled features will not be included in your site's bundle files.</p>
</div>
<p>Now Google Analytics (via <a href="https://v2.vuepress.vuejs.org/reference/plugin/google-analytics.html" target="_blank" rel="noopener noreferrer">plugin-google-analytics<ExternalLinkIcon/></a>) and Baidu Tongji (via <RouterLink to="/docs/plugins/baidu-tongji.html">plugin-baidu-tongji</RouterLink>) are supported.</p>
<h3 id="google-analytics" tabindex="-1"><a class="header-anchor" href="#google-analytics" aria-hidden="true">#</a> Google Analytics</h3>
<p>Paste the tracking code offered by <a href="https://www.google.com/analytics/" target="_blank" rel="noopener noreferrer">Google Analytics<ExternalLinkIcon/></a> here:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">ga</span><span class="token operator">:</span> <span class="token string">"your-tracking-code"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="baidu-tongji" tabindex="-1"><a class="header-anchor" href="#baidu-tongji" aria-hidden="true">#</a> Baidu Tongji</h3>
<p>Paste the tracking code offered by <a href="https://tongji.baidu.com/web/welcome/login" target="_blank" rel="noopener noreferrer">Baidu Tongji<ExternalLinkIcon/></a> here:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">ba</span><span class="token operator">:</span> <span class="token string">"your-tracking-code"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></div></template>


