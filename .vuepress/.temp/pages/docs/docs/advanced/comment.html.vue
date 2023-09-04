<template><div><p>::: info
This feature is disabled by default.
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>Code related to the disabled features will not be included in your site's bundle files.</p>
</div>
<p><a href="https://github.com/giscus/giscus" target="_blank" rel="noopener noreferrer">Giscus<ExternalLinkIcon/></a> is supported as the third party comment system, which is powered by <a href="https://docs.github.com/en/discussions" target="_blank" rel="noopener noreferrer">GitHub Discussions<ExternalLinkIcon/></a>.</p>
<h2 id="preparation" tabindex="-1"><a class="header-anchor" href="#preparation" aria-hidden="true">#</a> Preparation</h2>
<ul>
<li>Create a public Github repository and <a href="https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/enabling-or-disabling-github-discussions-for-a-repository" target="_blank" rel="noopener noreferrer">enable Discussions<ExternalLinkIcon/></a> for it</li>
<li>Install <a href="https://github.com/apps/giscus" target="_blank" rel="noopener noreferrer">Giscus app<ExternalLinkIcon/></a></li>
<li>Browse <a href="https://giscus.app/" target="_blank" rel="noopener noreferrer">Giscus's website<ExternalLinkIcon/></a> and generate your repo id, category id and other things on the website</li>
</ul>
<h2 id="configuration" tabindex="-1"><a class="header-anchor" href="#configuration" aria-hidden="true">#</a> Configuration</h2>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">giscus</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">repo</span><span class="token operator">:</span> <span class="token string">"[repo]"</span><span class="token punctuation">,</span>  <span class="token comment">// required, string, format: user_name/repo_name</span>
      <span class="token literal-property property">repoId</span><span class="token operator">:</span> <span class="token string">"[repo id]"</span><span class="token punctuation">,</span>  <span class="token comment">// required, string, generate it on Giscus's website</span>
      <span class="token literal-property property">category</span><span class="token operator">:</span> <span class="token string">"[category name]"</span><span class="token punctuation">,</span>  <span class="token comment">// required, string</span>
      <span class="token literal-property property">categoryId</span><span class="token operator">:</span> <span class="token string">"[category id]"</span><span class="token punctuation">,</span>  <span class="token comment">// required, string, generate it on Giscus's website</span>
      <span class="token literal-property property">mapping</span><span class="token operator">:</span> <span class="token string">"[page &lt;-> discussion mapping]"</span><span class="token punctuation">,</span>  <span class="token comment">// optional, string, default="title"</span>
      <span class="token literal-property property">reactionsEnabled</span><span class="token operator">:</span> <span class="token string">"[enable reactions or not?]"</span><span class="token punctuation">,</span>  <span class="token comment">// optional, boolean, default=true</span>
      <span class="token literal-property property">lang</span><span class="token operator">:</span> <span class="token string">"[language]"</span><span class="token punctuation">,</span>  <span class="token comment">// optional, string, default="auto" (follow the site's language, fall to "en" if your site's language is not supported by Giscus)</span>
      <span class="token literal-property property">lazyLoad</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>  <span class="token comment">// optional, boolean, default=false (if true, loading of Giscus will be deferred until the user scrolls near the comments container)</span>
      <span class="token literal-property property">crossorigin</span><span class="token operator">:</span> <span class="token string">"[crossorigin]"</span><span class="token punctuation">,</span>  <span class="token comment">// optional, string, default="anonymous"</span>
      <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token string">"[theme for light mode]"</span><span class="token punctuation">,</span>  <span class="token comment">// optional, string, default="light"</span>
      <span class="token literal-property property">darkTheme</span><span class="token operator">:</span> <span class="token string">"[theme for dark mode]"</span>  <span class="token comment">// optional, string, default="dark_dimmed"</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p><code v-pre>theme</code> and <code v-pre>darkTheme</code> option could be a <a href="https://github.com/giscus/giscus/blob/main/ADVANCED-USAGE.md#data-theme" target="_blank" rel="noopener noreferrer">custom theme<ExternalLinkIcon/></a> (a URL to a CSS file).</p>
<p>Refer to the <RouterLink to="/zh/docs/plugins/giscus.html">plugin-giscus</RouterLink> for more information.</p>
</div></template>


