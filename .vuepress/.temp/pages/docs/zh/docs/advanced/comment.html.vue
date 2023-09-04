<template><div><p>::: info
默认不启用该功能。
:::</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>对于没有启用的功能，与它们相关的代码并不会被打包。</p>
</div>
<p>评论系统使用了基于 <a href="https://docs.github.com/en/discussions" target="_blank" rel="noopener noreferrer">GitHub Discussions<ExternalLinkIcon/></a> 的 <a href="https://github.com/giscus/giscus" target="_blank" rel="noopener noreferrer">Giscus<ExternalLinkIcon/></a>。</p>
<h2 id="准备" tabindex="-1"><a class="header-anchor" href="#准备" aria-hidden="true">#</a> 准备</h2>
<ul>
<li>建一个公开的 Github 仓库并<a href="https://docs.github.com/cn/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/enabling-or-disabling-github-discussions-for-a-repository" target="_blank" rel="noopener noreferrer">启用 Discussions<ExternalLinkIcon/></a></li>
<li>安装 <a href="https://github.com/apps/giscus" target="_blank" rel="noopener noreferrer">Giscus app<ExternalLinkIcon/></a>，在选择仓库时至少要把上述仓库选进去</li>
<li>查看 <a href="https://giscus.app" target="_blank" rel="noopener noreferrer">Giscus 官网<ExternalLinkIcon/></a>并在上面生成你的 repo id、category id 以及别的必要信息</li>
</ul>
<h2 id="配置" tabindex="-1"><a class="header-anchor" href="#配置" aria-hidden="true">#</a> 配置</h2>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
  <span class="token literal-property property">themePlugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token literal-property property">giscus</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">repo</span><span class="token operator">:</span> <span class="token string">"[仓库]"</span><span class="token punctuation">,</span>  <span class="token comment">// 必须，string，格式：user_name/repo_name</span>
      <span class="token literal-property property">repoId</span><span class="token operator">:</span> <span class="token string">"[仓库 ID]"</span><span class="token punctuation">,</span>  <span class="token comment">// 必须，string，在 Giscus 官网上生成</span>
      <span class="token literal-property property">category</span><span class="token operator">:</span> <span class="token string">"[discussion 分类名]"</span><span class="token punctuation">,</span>  <span class="token comment">// 必须，string</span>
      <span class="token literal-property property">categoryId</span><span class="token operator">:</span> <span class="token string">"[discussion 分类 ID]"</span><span class="token punctuation">,</span>  <span class="token comment">// 必须，string，在 Giscus 官网上生成</span>
      <span class="token literal-property property">mapping</span><span class="token operator">:</span> <span class="token string">"[页面 &lt;-> discussion 映射]"</span><span class="token punctuation">,</span>  <span class="token comment">// 可选，string，default="title"</span>
      <span class="token literal-property property">reactionsEnabled</span><span class="token operator">:</span> <span class="token string">"[是否启用 reaction]"</span><span class="token punctuation">,</span>  <span class="token comment">// 可选，boolean，default=true</span>
      <span class="token literal-property property">lang</span><span class="token operator">:</span> <span class="token string">"[语言]"</span><span class="token punctuation">,</span>  <span class="token comment">// 可选，string，default="auto"（跟随网站语言，如果 Giscus 不支持你的网站的语言，则会使用 "en"）</span>
      <span class="token literal-property property">lazyLoad</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>  <span class="token comment">// 可选，boolean，default=false（如果设为 true，Giscus 的加载将延迟到用户滚动到评论容器附近）</span>
      <span class="token literal-property property">crossorigin</span><span class="token operator">:</span> <span class="token string">"[crossorigin]"</span><span class="token punctuation">,</span>  <span class="token comment">// 可选，string，default="anonymous"</span>
      <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token string">"[light 模式主题]"</span><span class="token punctuation">,</span>  <span class="token comment">// 可选，string，default="light"</span>
      <span class="token literal-property property">darkTheme</span><span class="token operator">:</span> <span class="token string">"[dark 模式主题]"</span>  <span class="token comment">// 可选，string，default="dark_dimmed"</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>）
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>其中，<code v-pre>theme</code> 和 <code v-pre>darkTheme</code> 项可以传入<a href="https://github.com/giscus/giscus/blob/main/ADVANCED-USAGE.md#data-theme" target="_blank" rel="noopener noreferrer">自定义主题<ExternalLinkIcon/></a>（一个 CSS 文件的 URL）。</p>
<p>参考：<RouterLink to="/zh/docs/plugins/giscus.html">plugin-giscus</RouterLink></p>
</div></template>


