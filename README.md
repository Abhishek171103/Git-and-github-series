# Git and Github notes
---

## 🔰 1. Project start karne ke liye (Daily use)
```js
git init
```
➡️ New project me Git start karta hai
```js
git clone <repo-url>
```
➡️ Company / GitHub ka project download karna

---

## 📂 2. Changes dekhna & add karna
```js
git status
```
➡️ Kaun si file change hui hai, kaun si staged hai
```js
git add .
```
➡️ Saari changed files stage karna
```js
git add fileName
```
➡️ Sirf ek file stage karni ho

---

## 📝 3. Commit (VERY IMPORTANT)
```js
git commit -m "login page completed"
```
➡️ Change ko save karna (history ban jaati hai)

> 📌 Rule:

- add → commit → push (yaad rakhna)

---

## 🌿 4. Branch ka kaam (Company level ka must)
```js
git branch
```
➡️ Kitni branches hain
```js
git branch new-branch
```
➡️ New branch banana
```js
git switch new-branch
```
➡️ Branch change karna
(Old way: git checkout)
```js
git switch -c feature-login
```
➡️ New branch + switch ek saath

---

## 🔀 5. Code merge karna
```js
git merge feature-login
```
➡️ Feature branch ka code main branch me lana

- (Conflict aaye to rukna nahi 😄 — solve karke commit)

---

## 🌍 6. Remote (GitHub / GitLab ke saath kaam)
```js
git remote -v
```
➡️ Repo ka remote URL check
```js
git pull origin main
```
➡️ Latest code lena (roz use hota hai)
```js
git push origin main
```
➡️ Apna code GitHub pe bhejna

### 📌 Internship mantra:
> Push karne se pehle hamesha git pull

---

## ⏪ 7. Galti ho jaaye to (Life saver commands)
```js
git restore fileName
```
➡️ File ko last commit jaisa bana dena
```js
git reset --soft HEAD~1
```
➡️ Last commit undo (code safe rahega)
```js
git reset --hard HEAD~1
```
➡️ ⚠️ Danger: last commit + code dono delete

---

## 📜 8. History dekhna
```js
git log
```
➡️ Commit history
```js
git log --oneline
```
➡️ Short & clean history (zyada useful)

---

## 🔖 9. Stash (Temporary save)
```js
git stash
```
➡️ Bina commit kiye changes side me rakhna
```js
git stash pop
```
➡️ Wapas laana


## ✅ git revert (SAFE – Company friendly)
```js
git revert <commit-id>
```
- Purane commit ko undo karta hai
- New commit banata hai
- History safe rehti hai ✅

- 📌 Use kab?
    - ➡️ Jab commit GitHub pe push ho chuka ho
    - ➡️ Team project me

## ⚠️ git restore (File level undo)
```js
git restore fileName
```
- Sirf file ko previous state me laata hai
- Branch / history change nahi hoti

- 📌 Use kab?
    - ➡️ Galti se file edit ho gayi
    - ➡️ Commit nahi kiya abhi

## ⚠️ git reset (History change karta hai)
```js
git reset --soft HEAD~1
git reset --hard HEAD~1
```
- Commit ko hata deta hai
- History change hoti hai

- 📌 Use kab?
    - ➡️ Jab commit push nahi hua ho
    - ➡️ Personal / local work
