# lfs_case1

git init
git remote add origin http://~
git add 200MB.zip
git commit -m "Add 200MB.zip"
git push origin master
(에러)
git lfs track 200MB.zip
git add 200MB.zip
git commit -m "Track 200MB.zip"
git push origin master
(에러) / 현재 파일은 git lfs로 인해 track 하지만, 이전의 Add 커밋 로그의 200MB 파일은 track이 안되어있음.
git repack && git gc
java -jar bfg-1.12.15.jar --strip-blobs-bigger-than 100M
git push origin master (bfg가 커밋로그를 수정하기 때문에 추가적으로 커밋하면 안됨.)
