Để tự động đẩy (push) từ một private repo sang một public repo trên Git.

## 1. Thêm public repo như một remote repository trong private repo
git remote add public-repo https://github.com/congneb/example.git

## 2
git rm --cached -r .github

## 3
git commit -m "Auto sync from private into public"

## 4
git push public-repo master
