##### 发版流程

1. 提交代码
2. 修改版本号
3. 生成changelog
4. 新建tag
5. release提交、tag提交
6. 发布

```bash
git commit -m 'feat: XXX'
npm version // 根据情况使用，也可手动修改版本号
yarn changelog
git commit -m 'release: v1.0.0'
git push
git tag -a v1.0.0 -m 'chore: release v1.0.0'
git push --tags
yarn deploy
```

