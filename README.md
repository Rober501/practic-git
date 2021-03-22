# practic-git
20210322-</br> 
新增初始-Repository 
在要做"檔案控制"的檔案下 初始化這個目錄 ==git init==</br>
$ echo "hello,git" > welcome.html (此指令是在該目錄下建立一個檔案.html 並在內容打上"hello,git")</br>
$ git add "*".html ("*"全部的.html 檔案) / add "--all"(將全部的當案都加到 暫存區)  / add "." (僅在這個目錄之下的檔案加入暫存區)<br/>
$ git commit -m "修改大綱" -m 後面的 "內容一定要寫" </br>
$ git commit -a -m (快捷指令從工作區>推到暫存區>再推到儲存區)</br>
$ git log 檢查git紀錄 / --onelin --graph  加上額外參數-精簡顯示 . 找符合內容"wtf" --onelin -- grep="wtf" </br>
$ git log -s "ruby" -s參數  照符合條件 人 或是時間 --since="9am" --until="12pm" </br>
$ git rm welcome.html 刪除也需要 add 及 commit  兩段才完成</br>
$ git rm welcome --cached 移除 git 控制.</br> 
$ mv hello.html  world.html 將前檔案名字改成後者

常用指令
+ cd 切換目錄
+ pwd 取得目前所位置
+ ls列出目前檔案列表
+ mkdir 建立新目錄
+ touch 建立檔案
+ 檔案複製 cp.移動 mv. 刪除 rm
+ 查詢現在目錄的狀況 git status

- vim 視窗編寫內容. i 才可以打內容  離開:q   存檔離開:wq
- code 打javacscrip  離開 ctrl + c
- js. 位元運算還不懂 , var 變數, {}陣列

20210307<br/>
在本地主機local  <font color=red>分3個為</font> working directory（工作資料夾）>> staging area（暫存區）>>和 repositories（檔案庫）。</br>
確認沒問題則 commit 到檔案庫中，最後 push 上去HUB- remote 環境。在 Git 中若是有和其他開發者一起合作，則會需要處理不同 branch 之間 conflict 和 merge 的問題。
