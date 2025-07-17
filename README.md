# giter - my git command best practise
### 解决中文文件名被编码成\XXX数字的情况：
```shell
git config --global core.quotepath false
git config --global i18n.commitencoding utf-8
```

### 推送本地提交到特定远程分支
```shell
git push origin HEAD:remote_branch_name
git push origin your_local_branch_name:remote_branch_name
```

### 我的git快捷键设置
```shell
[alias]
	app = apply
	apc = apply --check
	br = branch
	brr = branch -r
	brv = branch -vv
	brd = branch -D
	brm = branch -m
	bra = branch -a
	bsut = "!f() { git branch --set-upstream-to origin/$1; }; f"
	bu = branch -u 
	s = status
	st = status
	cm = commit
	cma = commit --amend
	cmm = commit -m
	ckb = checkout -b
	ck = checkout
	df = diff
	dfg = diff --staged
	rt = restore
	rtg = restore --staged
	pl = pull
	plo = pull origin dev
	puo = pull origin dev:dev
	plr = pull remote
	ph = push
	phf = push -f
	p2502 = "!f() { git push origin HEAD:ft-202502.00.000-$1; }; f"
	st = stash
	stl = stash list
	std = stash drop
[commit]
	template = D:/ProgramFiles/Git/.githooks/commit-template.txt
```

