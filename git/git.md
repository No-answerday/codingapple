# powershell
$git config --global user.email "홍길동@naver.com"
$git config --global user "홍길동"


# 작업폴더에서 git 사용
$git init

# 파일 현재상태 기록
$git add 파일명

# 파일 현재상태 기록
$git add 파일명
$git commit -m '메모'

# staging
작업폴더 - [git add] - staging area - [git commit] - repository(저장소)

# 여러 파일 스테이징
$git add 파일1 파일2 ...

# 모든 파일 스테이징
$git add.

# git 상태 확인
$git status

# 스테이징된 파일 취소
$git restore --staged 파일명

# commit 내역 조회
$git log --all --oneline
$git log --all --oneline --graph


# 최근 commit과 현재파일 차이점 
$git diff
$git difftool

# 특정커밋 비교가능
$git difftool 커밋id
$git difftool 커밋id1 커밋id2

# 브랜치 생성
$git branch 브랜치명

# 브랜치로 이동
$git switch

# merge
$git merge