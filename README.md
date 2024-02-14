# pLaTeX
mysyle.sty:スタイルファイル  
template.tex:テンプレ  
latex.json:VScodeで使う場合のユーザースニペット  
.styファイルをダウンロードし,.texと同じ階層に置けば,\usepackage{mystyle}とすることでマクロをつかえる様になる
template.texで直接参照されるので,mksty~(覚えてない)みたいな更新はしなくてよい  

# 使用例
空行\lnskip  
字下げなし\noindent  
字下げ\par  

画像コマンド\img[htbp(H)]{name}{caption}{fig:label}{scale}  
表コマンド\begin{tab}{caption}{tab:label}{lll}\end{tab}  
\multicolumn{3}{l}{}  
\multirow{3}{l}{}  
改行\shortstack{aa\aa}  
縦位置を合わすには別の列の要素も\shortstack{aa\{}}  
縦結合 罫線\cline{2-5}  
表の中に脚注 *1とつけたいとこに\footnotemark[数字]{文字を書きたいときはこれを追加}  
表の下に脚注 \multicolumn{3}{l}{\cite{hagiwara}p.6 表1.1 より引用し一部改変.}  
複数画像  
\begin{figure}[htbp]  
   \someimg[scale]{filename}{caption}{label}{pagesize(半分なら0.5とか)}  
   \someimg[scale]{filename}{caption}{label}{pagesize}  
   \caption{caption}  
   \label{label}  
\end{figure}  

複数表  
\begin{table}[htbp]  
   \begin{sometab}{caption}{tab:label}{lll}{pagesize(半分なら0.5とか)}  
       sin & cos \ \hline\hline  
      love & hate \  
      holy & meteo \ \hline  
   \end{sometab}  
   \begin{sometab}{caption}{tab:label}{lll}{pagesize}  
       sin & cos \ \hline\hline  
      love & hate \  
      holy & meteo \ \hline  
   \end{sometab}  
   \caption{caption}  
   \label{label}  
\end{table}  


#### 参考資料
https://github.com/Loliver1224/own-tex-style
