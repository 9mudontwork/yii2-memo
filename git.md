# Git

โหลด zip เฉพาะไฟล์ที่เปลี่ยนใน branch

```text
git archive -o srb-update.zip HEAD $(git diff --name-only 7eeb43c..4ced96c)
```

