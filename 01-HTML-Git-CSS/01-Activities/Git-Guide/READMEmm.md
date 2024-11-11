# မိမိကွန်ပြူတာ၌(Local) Git-ဖြင့် Repository(ပရောဂျက်) တည်ဆောက်ခြင်း

အခုသင်ခန်းစာမှာ မိမိကွန်ပြူတာမှာ Git-Branchကို `main` လို့ပေးမယ်။ `git init`သုံးပြီး repo တည်ဆောက်မယ်။ `git pull`အကြောင်းကို လေ့လာမယ်။

Git ဟာ ပရိုဂရမ်ရေးသူတွေအတွက် အလွန်အရေးပါတယ်။ ကိုယ့်ရဲ့ အချိန်တိုင်းမှာ ရေးထားတဲ့အချက်အလက်တွေ မပျောက်ဖို့လိုတယ်။ ကိုယ်နဲ့ လုပ်ဖေါ်ကိုင်ဘက်တွေ တစ်နေရာစီက အလုပ်တွေ မထပ်မိဘို့လဲ လိုသေးတယ်။ သင်တန်းကပေးမယ့် Repo တွေကို ယူထားဖို့လိုတယ်။ အိမ်စာတိုင်းအတွက် ဆရာ့ဆီကို GitHub ကတစ်ဆင့် ပေးပို့ရပါမယ်။

အပြည့်အစုံဖတ်ရန်
[Full-Stack Blog guide on getting started with Git](https://coding-boot-camp.github.io/full-stack/git/getting-started-with-git).

## မိမိကွန်ပြူတာရဲ့ မူလ-branch ကို main-ဟုထားခြင်း

မူလ branch နာမည်ကို `master`လို့ပေးကြသော်လဲ `main`လို့ပေးတဲ့သူက ပိုများပါတယ်။ ဒါ့ကြောင့် `main`လို့ပေးကြမယ်။

> **သတိ:** အစကတည်းက `main`ဖြစ်ပြီးသားဆိုယင် ဘာမှထပ်လုပ်စရာမလိုပါဘူး။

Git-ကို install လုပ်ထားပြီးပြီလားဆိုတာကို သိအောင်

  ```bash
  git --version
  ```

Git 2.42 သို့ အသစ်ဖြစ်နေယင်, ထပ်ပြီးတိုးမြှင့်ဘို့လိုတယ်လိုယင် တိုးမြှင့်ထားပါ

* Windows အသုံးပြုသူများအတွက် [Downloading Git website](https://git-scm.com/download/win) and download the latest "64-bit Git for Windows Setup" file.

* Mac အသုံးပြုသူများအတွက်:

  ```bash
  brew upgrade git
  ```

`main` branch လုပ်ဖို့ အောက်ပါအတိုင်းရေးပါ

  ```bash
  git config --global init.defaultBranch main
  ```

ဘာစကားပြန်မှ မလာတော့ရင် အောင်မြင်သွားလို့ပါ။

## Local Repo စတင်ခြင်း

GitHub မှာ remote repo လုပ်မယ်၊ ပြီးယင် Local မှာ clone လုပ်မယ်။
Clone လုပ်ထားတဲ့ဖိုင်တွဲမှာ `git init`လုပ်မယ်။ `git init`လုပ်ထားလိုက်တော့ remote repo-နဲ့ အလုပ်လုပ်ရတာ အဆင်ပြေသွားတာပေါ့

အခုသင်မယ့်သင်တန်းစာတွေအတွက် `CodeCamp`ဆိုတဲ့ ဖိုင်တွဲတစ်ခု တည်ဆောက်မယ်၊ အဲ့ဒီထဲမှာ `git-init-sample`ဆိုတဲ့ ဖိုင်တွဲတစ်ခု ထပ်တည်ဆောက်မယ်။

  ```bash
  mkdir git-init-sample
  ```

နောက်ပြီး `cd`နဲ့ ဖိုင်တွဲဆီသွား၊ `touch`နဲ့ `index.html`ဖိုင်ကို တည်ဆောက်။

  ```bash
  cd git-init-sample
  touch index.html
  ```

Git repo လို့ အသိမှတ်ပြုဖို့ `git init`နဲ့ ဖိုင်တွဲကို သတ်မှတ်လိုက်မယ်

  ```bash
  git init
  ```

အဲ့ဒီမှာ `.git`ဆိုပြီး ထပ်ဆင့်ဖိုင်တွဲတစ်ခုနဲ့ လိုအပ်တဲ့အရာတွေအားလုံး တည်ဆောက်သွားလိမ့်မယ်၊ အဲ့ဒါမှ လုပ်လိုက်တဲ့အလုပ်အားလုံးကို တစ်ခုစီ လိုက်ကြည့်လို့ရသွားမှာပါ။ ဒီတော့ `git status`နဲ့ ကြည့်လိုက်ရအောင်

  ```bash
  git status
  ```

အခု `index.html`က အနီရောင်အဆင့်နဲ့ ရွေးချယ်မခံရသေးပါဘူး၊ ဒါဆို အခုလိုလေး ရွေးချယ်လိုက်ရအောင်

  ```bash
  git add .
  ```

အခုဆိုရင် `git status`နဲ့ပြန်ကြည့်လိုက်ယင် အစိမ်းရောင်လေးနဲ့ ရွေးချယ်ပြီးဖြစ်သွားပါလိမ့်မယ်၊ အလုပ်တစ်ခုပြီးစီးအကြောင်း မှတ်တမ်းတင်လိုက်ရအောင်

  ```bash
  git commit -m "initial commit"
  ```

အခုအနေအထားမှာ local repo-ကနေ remote repo-နဲ့ ဆက်သွယ်ရမယ့်အချိန်ရောက်ပါပြီ

ဒါဆို remote repo-ဆီကို သွားမယ်
[GitHub](https://github.com/) 
ပြီးယင် အသစ်remote repo-တည်ဆောက်မယ်၊ နာမည်တူအောင်ပေးကြမယ် `git-init-sample`

> **သတိ**: အသစ်remote repo-တည်ဆောက်တဲ့အခါ ဘာဖိုင်ကိုမှ ထည့်ဘို့မလုပ်လိုက်ပါနဲ့။

ပြီးယင် "Create Repository"ကို နှိပ်လိုက်ပါ၊ ပြီးယင် ညွှန်ကြားချက်ကြည့်ပြီး ဆက်လုပ်ရပါမယ်။

  ```bash
  git remote add origin <the HTTPS or SSH URL ending in .git>
  git branch -M main
  git push -u origin main
  ```

> **မှတ်ချက်**: ကိုယ့်မှာ local default branch ကို `main`လို့ပြောင်းထားပြီးယင် `git branch -M main` လုပ်ဖို့မလိုပါဘူး။

commands-တွေကို copy လုပ်ပြီး Enter-နှိပ်လိုက်ပါ

အောင်မြင်ခဲ့ယင် အောက်ပါအတိုင် မြင်တွေ့ရပါလိမ့်မယ်

![A message indicates that the project directory has been successfully imported.](./assets/image-8.png)

## Remote Repo-မှာပြင်ထားတာကို Pull လုပ်ရမှာပါ

သင်တန်းမစမီ ကျောင်းသားဆိုင်ရာ ဖိုင်တွေကို `git pull` လုပ်ရပါမယ်၊ 
ပထမဆုံး မိမိဆိုင်ရာဖိုင်ဆီသွားပါ-ဥပမာ

  ```bash
  cd git-init-sample
  ```

နောက်ပြီး `git push`လုပ်တုန်းကလို အောက်ပါအတိုင်း `git pull`လုပ်ပါ၊ 

  ```bash
  git pull origin main
  ```

အခုဆိုယင် local repo-မှာ remote repo-နဲ့အတူတူ ရောက်သွားပါပြီ၊

remote repo-မှာပြောင်းလိုက်တိုင်း အသိပေးစာသားတွေကို မြင်ရမှာပါ

![A message indicates that changes have been made from the remote repository.](./assets/image-9.png)

`git pull`လုပ်ပြီးသွားယင်လဲ အောင်မြင်စွာပြီးဆုံးသွားကြောင်း ပြောပြပါလိမ့်မယ်။

ပြောင်းထားတဲ့ဖိုင်တွေကို VS Code-နဲ့ဖွင့်ကြည့်လို့ရပါတယ်

## Remote Repo URL ကို ဝေငှခြင်း

မိမိတို့ရဲ့ အိမ်စာတွေကို ပြန်လည်ဝေငှပေးလို့ရပါတယ်
address bar-က URL-ကို copy-လုပ်ပါ၊ ပေးလိုတဲ့သူရဲ့ Slack-ထဲမှာ ထည့်ပေးလိုက်ရုံပါပဲ။

## မှတ်ချက်

တစ်ခုခုလိုအပ်ယင် ဆရာဆီကိုဖြစ်စေ၊ ဆရာကူများသို့ဖြစ်စေ အကူအညီ တောင်းနိုင်ပါတယ်

ထပ်၍သိရှိလိုပါက [Atlassian guide on setting up a repository](https://www.atlassian.com/git/tutorials/setting-up-a-repository).

ထပ်၍သိရှိလိုပါက [Atlassian guide on git pull](https://www.atlassian.com/git/tutorials/setting-up-a-repository/git-config).

---
© 2024 PannaCollege
