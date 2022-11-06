# rails content_for学習用

content_forは個別のビューで表示させたい内容を表示するのに使用される。
例えば、各ページでタブの内容を変えたい場合、railsアプリを作成したデフォルトだと、application.html.erbにtitleタグで
設定されているため、全ページ同じ「StudyContent」になってしまう。

<img width="938" alt="application_html_erb_—_study_content" src="https://user-images.githubusercontent.com/66200883/200158223-f600f001-ddb7-4e91-894b-a4f0712397d4.png">


そのため、各ページで別のタブ名を表示するのに使用するのが、content_forである。
まずapplication.html.erbに赤線のように「yield :任意のキーワードのシンボル」を記述する。

<img width="659" alt="application_html_erb_—_study_content" src="https://user-images.githubusercontent.com/66200883/200158341-e4fac225-73b0-4817-b458-8aaf7156de42.png">


そして、タブ名を変えたいページに以下のように記述することで実現できる。

```rails
<% content_for :任意のキーワードのシンボル do %>
表示したいERBの内容
<% end %>
```

<img width="624" alt="world_html_erb_—_study_content" src="https://user-images.githubusercontent.com/66200883/200158502-7310f78d-9713-4125-a39c-6c5bc5296eaa.png">


そうするとタブには上記で指定したメッセージを表示することができる。
<img width="1675" alt="オラオラ" src="https://user-images.githubusercontent.com/66200883/200158556-e8621717-6d09-44e9-8494-5f57e072a3ca.png">

