# rggfhjkthgj
git init
echo "# My Project" >> http://README.md
git add http://README.md
git commit -m "Initial commit"

for i in {1..10}; do
    echo "Commit $i line" >> http://README.md
    git add http://README.md
    # 生成随机时间（2025年6月内）
    day=$((10 + RANDOM % 10))
    hour=$((RANDOM % 24))
    min=$((RANDOM % 60))
    sec=$((RANDOM % 60))
    export GIT_AUTHOR_DATE="2025-06-${day}T${hour}:${min}:${sec}"
    export GIT_COMMITTER_DATE="$GIT_AUTHOR_DATE"
    git commit -m "commit $i"
    echo "提交 $i 时间: $GIT_AUTHOR_DATE"
done


