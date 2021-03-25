# practic-git
0325-<br/>
+ 從伺服器上取得repository - 可以用 https 或是 ssh 兩種方式連接</br>
+ push -u  推上 後面-u 是指上游 upstream 意思是傳到遠端某server上的分支 第一次上傳設定 成為預設  下次自然會指向該分支<br/>
+ pull 下載更新  $ git pull = git fetch + git merge</br>
+ pull+rebase 在做完 fetch 後 也可以用rebase 來完成合併, 跟 merge 的方式有些不同. 可避免掉額外的 commit</br> 
+ clone 跟 pull 的差異- colne 使用在第一次看到,將檔案下載回來時,爾後的更新最新的線上版本 使用 pull and fetch 就可以了</br>
+ pull request (PR)-與其他開發者互動 ,請求原開發者拉回審視</br>
+ fork - 複製檔案回到本地,使用修改</br>

分支就像是貼紙一樣　head > master> 789d5e</br>
.git 目錄裡的寶藏四大物件- blob(.git目錄下使用blob物件方式存放), tree, commit(在這裡表示查看更細節的內容), tag(標籤)
+ blob-物件的檔名 是由SHA-1 演算法決定的(40個字.拿前面2個字當目錄名稱,剩餘38個字是檔案名字), blob 的內容則是由壓縮演算法決定
+ tree-目錄以及檔案的名使用tree方式存放,tree的物件內容會指向某些blob或是其他的tree
+ git cat-file (-t /-p) 該指令查看.git檔案內容, -t 參數,查SHA-1這個值所代表物件的型態, -p 參數,查SHA-1指向那顆物件的內容
+ tag 標籤- 是一個指向某一個commit的指標, 跟分支branch很像 -有兩種標籤 清量標籤lighweight tab及附註標籤annotated tag.



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
