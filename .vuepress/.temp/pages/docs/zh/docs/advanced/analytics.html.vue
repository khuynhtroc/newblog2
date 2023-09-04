<template><div><p>::: info
默认不启用这些功能。
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>对于没有启用的功能，与它们相关的代码并不会被打包。</p>
</div>
<p>目前支持谷歌统计（基于插件 <a href="https://vuepress.vuejs.org/plugin/official/plugin-google-analytics.html" target="_blank" rel="noopener noreferrer">plugin-google-analytics<ExternalLinkIcon/></a>）和百度统计（基于插件 <RouterLink to="/zh/docs/plugins/baidu-tongji/">plugin-baidu-tongji</RouterLink>）。</p>
<h2 id="谷歌统计" tabindex="-1"><a class="header-anchor" href="#谷歌统计" aria-hidden="true">#</a> 谷歌统计</h2>
<p>需要去<a href="https://www.google.com/analytics/" target="_blank" rel="noopener noreferrer">谷歌统计<ExternalLinkIcon/></a>官网上申请一个跟踪代码，然后填入配置：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">ga</span><span class="token operator">:</span> <span class="token string">"your-tracking-code"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="百度统计" tabindex="-1"><a class="header-anchor" href="#百度统计" aria-hidden="true">#</a> 百度统计</h2>
<p>需要去<a href="https://tongji.baidu.com/web/welcome/login" target="_blank" rel="noopener noreferrer">百度统计<ExternalLinkIcon/></a>官网上申请一个跟踪代码，然后填入配置：</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">ba</span><span class="token operator">:</span> <span class="token string">"your-tracking-code"</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></div></template>


