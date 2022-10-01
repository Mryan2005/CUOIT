## 用GitHub Action将GitHub的提交同步至Gitee
```yml
sync:
	runs-on: ubuntu-latest
	steps:
		- name: Sync to Gitee
		uses: wearerequired/git-mirror-action@master
		env:
			SSH_PRIVATE_KEY: ${{ secrets.GITEE_RSA_PRIVATE_KEY }}
		with:
			# 来源仓库
			source-repo: "git@github.com:Mryan2005/CUOIT.git"
			# 目标仓库
			destination-repo: "git@gitee.com:Mryan2005/CUOIT.git"
```