# Git-Version-Control-Commands

### Git Yapılandırması

`git config --global user.name "Fatih"` <br>
`git config --global user.email "fatih_duygu@hotmail.com"` <br>
- Global seviyedeki tüm ayarları listelemek için ; <br>
`git config --global -l` <br>


### Git Proje Oluşturma (Local Repo) <br>

`cd desktop/poject_directory`<br>
`git init`<br>
`ls -la`<br>


### Commit and Log 

- Staging areaya eklemek için ;<br>
`git add .`<br>

- commit etmek için ;<br>
`git commit -m "initial commit"`<br>

- Bütün versiyonları listelemek için ;<br>
`git log`<br>
`git log -p (ayrıntılı görmek için)`<br>
`git log --oneline (ayrıntısız görmek için)`<br>



### Git Status<br>
- git status komutu proje dosyalarında yapılan değişiklikleri ve staging areada bulunan dosyaları listeler.<br>
`git status`<br>


### Diff<br>
- Projede yapılan değişiklikleri karşılaştırmak için ;<br>
`git diff master branch-A`<br>
- Stage area'ya alınmış dosyalardaki farklılıkları görmek için ;<br>
`git diff --staged`<br>
 
 
 ### Stash (Geçici Kaydetme)<br>
 `git stash save "a.java düzenlendi"`<br>
 `git stash list (stashleri listeler)`<br>
- Stashteki dosyalarda yapılan değişiklikleri görmek için ;<br>
`git stash show -p 0(stash id)`<br>
- Stashleri silmek için ;<br>
`git stash drop 1(stash id)`<br>
- Stashleri geri döndürme ;<br>
`git stash pop (LIFO)`<br>
`git stash pop 1(stash_id)`<br>


### "git add" and "git rm"<br>
  - Değişiklikleri stage areaya eklemek için ;<br>
  `git add folder_name`<br>
  - Bir dosyayı silmek için ;<br>
  `git rm folder_name`<br>
  - Klasörü silmek için ;<br>
  `git rm -r folder_name`<br>
  
### Dosya isimlendirme ve Taşıma 
  `git mv a.java b.java`<br>
  `git mv a.java folder/`<br>
  
### Değişikliği geri alma (Working Copy)<br>
`git restore a.java`<br>
`git checkout a.java`<br>
 
 
### Değişikliği geri alma (Staging Area)<br>
`git restore --staged a.java`<br>
`git restore a.java`<br>
- Stage areadaki dosya çalışma dizinine tekrar gönderilir ve restore edip eski haline getirilebilir.<br>


### Commiti Geri Almak 
`git revert`<br>
`git reset`<br>
- Local tüm commitleri silip geri almak için ;<br>
`git revert --hard`<br>
`git reset --hard`<br>
- Local commitlerin korunması için ;<br>
`--keep`

### Son commiti Değiştirmek
- Son commite dosya eklemek için ; <br>
`git add .`<br>
`git commit --amend`<br>
- Commit mesajını değiştirme ;<br>
`git commit -amend -m "changed commit text"`<br>


### Versiyon Değiştirme 
`git checkout (version hash code(first 6 number)) --.`<br>

### Githuba Proje Göndermek

- Github remote link eklenir ;<br>
`git remote add nickname https://...`<br>
- Url'yi düzenlemek için ;<br>
`git remote set -url nickname https://...`<br>
- Proje push edilerek gönderilir ;<br>
`git push -u | -f nickname master`<br>


### Remote Proje Oluşturma

`git clone https:/github.com/fatihhduygu/...`<br>
- Projeyi clonelayınca fetch ve push değerleri gelir ve remote ismi varsayılan olarak origin'dir.<br>
- Projeyi push etmek için ;<br>
`git push origin master`<br>
- Uzak repository ile ilgili bilgiler ;<br>
`git remote -v`


### Fetch, Pull

- Remotedan güncelleme yapmak için ;<br>
`git fetch origin (güncellemeler indirildi)`<br>
`git diff origin (farklılıklar incelendi)`<br>
`git branch -a (fetch ile gelen bütün brancleri gösterir.)`<br>
`git merge master (projeye eklenir)`<br>
- git Fetch komutunda local branche merge etme işlemini kullanıcı yapmak zorundadır.<br>
- Pull komutunda yukarıdaki işlemler otomatik gerçekleşir.<br>
`git pull`<br>

### gitignore 
- Git tarafından takip edilmesini istemediğimiz dosyalar gitignore içine yazılır.<br>
`cat >> .gitignore`<br>
`veritabanı.txt`<br>
`.xlsx`<br>
`Ctrl+C`<br>
- add ve commit işlemi yapılır.<br>
- push işlemi yapılır.<br>
- gitignore dosyasını düzenlemek için ;<br>
` notepad .gitignore`<br>


### Git Branch
- Localdeki branchleri görmek için ;<br>
`git branch`<br>
- Remote branchleri görmek için ;<br>
`git branch --all`
- Yeni branch oluşturmak için ;<br>
`git branch newBranch`<br>
- Branch oluşturup gitmek için ;<br>
`git branch -b newBranch`<br>
- Branchler arası geçiş için ;<br>
`git checkout newBranch`<br>
- İki branch arasındaki farklılıkları görmek için ;<br>
`git diff master newBranch`<br>
- İki branchi birleştirmek için ;<br>
`git merge newBranch`<br>
- Branch'i silmek için ;<br>
`git branch -d | -D newBranch-2`<br>
- Remote'dan branch silmek için ;<br>
`git branch -dr newBranch`
- Yukarıdaki komut sadece localdeki remote'u siler Remote da geçeerli olmak için;<br>
`git push origin:newBranch`<br>

### Merge 

- İki branchi birleştirmek için ;<br>
`git merge newBranch`<br>
- Merge işlemini geri almak için ;<br>
`git merge --abort`<br>
- Merge alternativi ;<br>
`git rebase branchB`<br>

