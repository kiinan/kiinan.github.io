---
layout: default
permalink: /about/
title: "About"
---

アバウト


サイトについて
プライバシーポリシー
個人情報保護方針

制定日：2021年012月11日

最終改訂日：2022年01月11日

 

【当サイトにて表示されている広告について】
当サイトでは、第三者配信の広告サービスであるGoogleアドセンスを使用しています。
閲覧者のアクセスに関する情報 『Cookie』(個人情報は一切は含まれません) を使用し、ユーザーの興味に応じた商品やサービスの広告を表示する場合があります。

【当サイトにて利用しているアクセス解析ツールについて】
当サイトでは、トラフィックデータの収集のためにCookieを使用しています。
このトラフィックデータは匿名で収集されており、個人を特定するものではありません。
Cookieを無効にすることで収集を拒否することが出来ますので、お使いのブラウザので設定をご確認ください。

 

【著作権について】

使用している版権物の知的所有権は、それぞれの著作者・団体に帰属します。
著作権所有よりご連絡がある際は迅速に対処させていただきます。

　
{% if page.header.overlay_color or page.header.overlay_image or page.header.image %}
  {% include page__hero.html %}
{% elsif page.header.video.id and page.header.video.provider %}
  {% include page__hero_video.html %}
{% endif %}

<div id="main" role="main">
  <article class="splash" itemscope itemtype="https://schema.org/CreativeWork">
    {% if page.title %}<meta itemprop="headline" content="{{ page.title | markdownify | strip_html | strip_newlines | escape_once }}">{% endif %}
    {% if page.excerpt %}<meta itemprop="description" content="{{ page.excerpt | markdownify | strip_html | strip_newlines | escape_once }}">{% endif %}
    {% if page.date %}<meta itemprop="datePublished" content="{{ page.date | date_to_xmlschema }}">{% endif %}
    {% if page.last_modified_at %}<meta itemprop="dateModified" content="{{ page.last_modified_at | date_to_xmlschema }}">{% endif %}

    <section class="page__content" itemprop="text">
      {{ content }}
    </section>
  </article>
</div>
