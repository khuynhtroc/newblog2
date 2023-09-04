<template><div><p>The theme can be configured in <code v-pre>.vuepress/config.js</code>. Refer to <a href="https://github.com/Renovamen/vuepress-theme-gungnir/blob/main/packages/theme/src/shared/options.ts" target="_blank" rel="noopener noreferrer">here<ExternalLinkIcon/></a> for all possible options.</p>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>The configs of this theme are compatible with all the configs of <a href="https://v2.vuepress.vuejs.org/reference/default-theme/config.html" target="_blank" rel="noopener noreferrer">VuePress's default theme<ExternalLinkIcon/></a> except:</p>
<ul>
<li>logo</li>
<li>logoDark</li>
<li>darkMode (dark mode switching is always enabled in this theme)</li>
<li>repo</li>
<li>repoLabel</li>
</ul>
<p>Please refer to <a href="https://v2.vuepress.vuejs.org/reference/default-theme/config.html" target="_blank" rel="noopener noreferrer">reference of VuePress's default theme config<ExternalLinkIcon/></a> for how to set them.</p>
</div>
<div class="custom-container tip"><p class="custom-container-title">TIP</p>
<p>Please make sure all the icons you specified in the configuration file are already imported, see <RouterLink to="/docs/advanced/icons/">here</RouterLink> to know how to import icons.</p>
</div>
<h2 id="navbar-title" tabindex="-1"><a class="header-anchor" href="#navbar-title" aria-hidden="true">#</a> Navbar Title</h2>
<p>Different from the default theme, Gungnir theme displays <code v-pre>themeConfig.navbarTitle</code> instead of the <a href="https://v2.vuepress.vuejs.org/reference/config.html#title" target="_blank" rel="noopener noreferrer"><code v-pre>title</code> option in site config<ExternalLinkIcon/></a> at the left of the navbar:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token comment">/*
    other site configurations
    ...
  */</span>

  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token comment">/*
      other theme configurations
      ...
    */</span>
    <span class="token literal-property property">navbarTitle</span><span class="token operator">:</span> <span class="token string">"Gungnir"</span>  <span class="token comment">// optional, default: "$ cd /home/"</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="highlight-lines"><br><br><br><br><br><br><br><br><br><br><br><br><br><div class="highlight-line">&nbsp;</div><br><br></div><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>It can also be used in the <a href="https://v2.vuepress.vuejs.org/reference/default-theme/config.html#locales" target="_blank" rel="noopener noreferrer"><code v-pre>locales</code><ExternalLinkIcon/></a> option, for example:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">locales</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token string-property property">"/"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token literal-property property">navbarTitle</span><span class="token operator">:</span> <span class="token string">"Gungnir"</span>
      <span class="token punctuation">}</span><span class="token punctuation">,</span>
      <span class="token string-property property">"/zh/"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token literal-property property">navbarTitle</span><span class="token operator">:</span> <span class="token string">"冈格尼尔"</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="author-information" tabindex="-1"><a class="header-anchor" href="#author-information" aria-hidden="true">#</a> Author Information</h2>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">personalInfo</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token comment">// required: nickname, will be showed on home page, mobile sidebar and author info of articles</span>
      <span class="token literal-property property">name</span><span class="token operator">:</span> <span class="token string">"Cool Dragon"</span><span class="token punctuation">,</span>

      <span class="token comment">// required: avatar, will be showed on home page and mobile sidebar</span>
      <span class="token literal-property property">avatar</span><span class="token operator">:</span> <span class="token string">"/img/avatar.jpeg"</span><span class="token punctuation">,</span>

      <span class="token comment">// required: a description, will be showed on home page</span>
      <span class="token literal-property property">description</span><span class="token operator">:</span> <span class="token string">'A cool dragon lost in human world.'</span><span class="token punctuation">,</span>
      
      <span class="token comment">// optional: id of social platform, will be showed on home page and mobile sidebar</span>
      <span class="token literal-property property">sns</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token literal-property property">github</span><span class="token operator">:</span> <span class="token string">'Renovamen'</span><span class="token punctuation">,</span>  <span class="token comment">// Github</span>
        <span class="token literal-property property">linkedin</span><span class="token operator">:</span> <span class="token string">'xiaohan-zou-55bba0160'</span><span class="token punctuation">,</span>  <span class="token comment">// Linkedin</span>
        <span class="token literal-property property">facebook</span><span class="token operator">:</span> <span class="token string">'renovamen.zou'</span><span class="token punctuation">,</span>  <span class="token comment">// Facebook</span>
        <span class="token literal-property property">twitter</span><span class="token operator">:</span> <span class="token string">'renovamen_zxh'</span><span class="token punctuation">,</span>  <span class="token comment">// Twitter</span>
        <span class="token literal-property property">zhihu</span><span class="token operator">:</span> <span class="token string">'chao-neng-gui-su'</span><span class="token punctuation">,</span>  <span class="token comment">// Zhihu</span>
        <span class="token literal-property property">weibo</span><span class="token operator">:</span> <span class="token string">'your-weibo-id'</span><span class="token punctuation">,</span>  <span class="token comment">// Sina Weibo</span>
        <span class="token literal-property property">email</span><span class="token operator">:</span> <span class="token string">'renovamenzxh@gmail.com'</span><span class="token punctuation">,</span>  <span class="token comment">// Email</span>
        <span class="token literal-property property">rss</span><span class="token operator">:</span> <span class="token string">"/rss.xml"</span><span class="token punctuation">,</span>  <span class="token comment">// link to RSS file</span>
        <span class="token comment">// if you want to add other social platforms</span>
        <span class="token literal-property property">bilibili</span><span class="token operator">:</span> <span class="token punctuation">{</span>  <span class="token comment">// any name you want</span>
          <span class="token literal-property property">icon</span><span class="token operator">:</span> <span class="token string">"ri-bilibili-line"</span><span class="token punctuation">,</span>  <span class="token comment">// platform icon</span>
          <span class="token literal-property property">link</span><span class="token operator">:</span> <span class="token string">"https://www.bilibili.com/"</span>  <span class="token comment">// profile URL</span>
        <span class="token punctuation">}</span>
        <span class="token comment">// ...</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="home-page" tabindex="-1"><a class="header-anchor" href="#home-page" aria-hidden="true">#</a> Home Page</h2>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">homeHeaderImages</span><span class="token operator">:</span> <span class="token punctuation">[</span>
      <span class="token comment">// image 1</span>
      <span class="token punctuation">{</span>
        <span class="token string-property property">"path"</span><span class="token operator">:</span> <span class="token string">"/img/home-bg/1.jpg"</span><span class="token punctuation">,</span>
        <span class="token string-property property">"mask"</span><span class="token operator">:</span> <span class="token string">"rgba(40, 57, 101, .4)"</span>
      <span class="token punctuation">}</span><span class="token punctuation">,</span>
      <span class="token comment">// image 2</span>
      <span class="token punctuation">{</span>
        <span class="token string-property property">"path"</span><span class="token operator">:</span> <span class="token string">"/img/home-bg/2.jpg"</span><span class="token punctuation">,</span>
        <span class="token string-property property">"mask"</span><span class="token operator">:</span> <span class="token string">"rgb(251, 170, 152, .2)"</span>
      <span class="token punctuation">}</span>
      <span class="token operator">...</span>
    <span class="token punctuation">]</span><span class="token punctuation">,</span>
    <span class="token literal-property property">blogNumPerPage</span><span class="token operator">:</span> <span class="token number">20</span>  <span class="token comment">// optional: maximum number of blogs per page, default: 10</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>The <code v-pre>mask</code> is a translucent overlay placed on the cover image. It will be helpful when your cover image is so complex that your title can not stand out.</p>
<p>Check the <RouterLink to="/">home page</RouterLink> of this site to see the effect. Click the left and right button to switch among multiple cover images.</p>
<h2 id="other-pages" tabindex="-1"><a class="header-anchor" href="#other-pages" aria-hidden="true">#</a> Other Pages</h2>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">pages</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token comment">// tags page</span>
      <span class="token literal-property property">tags</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token comment">// optional: subtitle of tags page</span>
        <span class="token literal-property property">subtitle</span><span class="token operator">:</span> <span class="token string">'Hey! Here is tags page!'</span><span class="token punctuation">,</span>

        <span class="token comment">// optional: paths to and masks of the tags page cover images</span>
        <span class="token literal-property property">bgImage</span><span class="token operator">:</span> <span class="token punctuation">{</span>
          <span class="token literal-property property">path</span><span class="token operator">:</span> <span class="token string">'/img/pages/tags.jpg'</span><span class="token punctuation">,</span>
          <span class="token literal-property property">mask</span><span class="token operator">:</span> <span class="token string">'rgba(211, 136, 37, .5)'</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span><span class="token punctuation">,</span>

      <span class="token comment">// links page</span>
      <span class="token literal-property property">links</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token comment">// optional: subtitle of links page</span>
        <span class="token literal-property property">subtitle</span><span class="token operator">:</span> <span class="token string">'Hey! Here is links page!'</span><span class="token punctuation">,</span>

        <span class="token comment">// optional: paths to and masks of the links page cover images</span>
        <span class="token literal-property property">bgImage</span><span class="token operator">:</span> <span class="token punctuation">{</span>
          <span class="token literal-property property">path</span><span class="token operator">:</span> <span class="token string">'/img/pages/links.jpg'</span><span class="token punctuation">,</span>
          <span class="token literal-property property">mask</span><span class="token operator">:</span> <span class="token string">'rgba(64, 118, 190, 0.5)'</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>Check the <RouterLink to="/tags/">tags page</RouterLink> and <RouterLink to="/links/">links page</RouterLink> to see the effect.</p>
<p>To edit the title of the above mentioned pages, please refer to Multi-language Support (TODO) section.</p>
<h2 id="custom-footer" tabindex="-1"><a class="header-anchor" href="#custom-footer" aria-hidden="true">#</a> Custom Footer</h2>
<p>Support HTML. For example, the footer of this site is:</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">footer</span><span class="token operator">:</span> <span class="token template-string"><span class="token template-punctuation string">`</span><span class="token string">
      &amp;copy; &lt;a href="https://github.com/Renovamen" target="_blank">Renovamen&lt;/a> 2018-2022
      &lt;br>
      Powered by &lt;a href="https://v2.vuepress.vuejs.org" target="_blank">VuePress&lt;/a> &amp;
      &lt;a href="https://github.com/Renovamen/vuepress-theme-gungnir" target="_blank">Gungnir&lt;/a>
    </span><span class="token template-punctuation string">`</span></span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h2 id="catalog" tabindex="-1"><a class="header-anchor" href="#catalog" aria-hidden="true">#</a> Catalog</h2>
<p>Enable or disable <strong>post</strong> catalog for all posts. Can be rewritten in each post's front matter.</p>
<div class="language-javascript line-numbers-mode" data-ext="js"><pre v-pre class="language-javascript"><code><span class="token comment">// .vuepress/config.js</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">gungnirTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">catalog</span><span class="token operator">:</span> <span class="token boolean">false</span>  <span class="token comment">// optional, default: true</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></div></template>


