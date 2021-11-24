---
layout: post
---

<h3>用 github + jekyll 建立個人頁</h3>

1. 建立repository <br/>
   ![repo](/images/create-pages/REPO.PNG)
    - 命名為 \<user>.github.io
    - \<user> **<font color="#FFA042">必須</font>** 使用個人帳號命名，且將字母轉小寫

2. 建立個人頁面 <br/>
      - clone 剛建立的 repository, 用指令建立個人頁面<br/>
         - move to repository
            ```
            cd {REPOSITORY-NAME}
            ```
         - 建立 Jekyll 網站
            ```
            git checkout --orphan gh-pages 
            jekyll new --skip-bundle .
            ```
         - 修改 Gemfile 設定 <br/>
            - gem "jekyll" 修改為 <br/> `#gem "jekyll"`
            - gem "github-pages" 修改為 <br/> `gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins` <br/>
             (將 {GITHUB-PAGES-VERSION} 換成 [最新版](https://pages.github.com/versions/))

         - 自動下載並安裝 Gem 套件
            ```
            bundle install
            ```
         - 調整 _config.yml 設定
            ```
            domain: my-site.github.io
            url: https://my-site.github.io
            baseurl: /REPOSITORY-NAME/
            ```

      - 上傳至repository

3. 檢視結果 <br/>
   進入專案設定 -> Pages
    ![repo](/images/create-pages/Setting.PNG) <br/>
   網站位置
   ![repo](/images/create-pages/Pages.PNG)
   
4. 其他常用指令 <br/>
   本機執行測試 預設位置[http://127.0.0.1:4000](http://127.0.0.1:4000)
   ```
   bundle exec jekyll serve
   ```
---

{: data-content="footnotes"}

參考 <br/>
[Creating a GitHub Pages site](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll) <br/>
[jekyll themes](http://jekyllthemes.org/)
