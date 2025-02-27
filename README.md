# Để tự động đẩy (push) từ một private repo sang một public repo trên Git.

## 1. Thêm public repo như một remote repository trong private repo
git remote add public-repo https://github.com/congneb/example.git

## 2
git rm --cached -r .github

## 3
git commit -m "Auto sync from private into public"

## 4
git push public-repo master

## 5. Nếu không push được, mà bị lỗi này
![image](https://github.com/user-attachments/assets/0e270e29-116f-4bb2-8325-2fa667b84454)

Thì: git push -f public-repo master

# Cách 2
Không muốn xóa folder .github đi, mà ta chỉ ignore nó đi bằng cách. <br>
  git remote add public-repo https://github.com/congneb/example.git <br>
  git update-index --assume-unchanged .github/workflows/* <br>
  git push -f public-repo master

- Lệnh này sẽ thông báo cho Git rằng các file trong thư mục .github không thay đổi, vì vậy chúng sẽ không được đẩy đến public repo.
