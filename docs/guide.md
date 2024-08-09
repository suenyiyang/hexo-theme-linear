# USER GUIDE

## 安装

### 克隆主题仓库

```bash
cd <path/to/your/hexo/blog>
cd themes
git clone git@github.com:syy11cn/hexo-theme-linear.git linear
```

### 启用主题

在 **博客根目录** 下的 `_config.yml` 文件中：

```yml
# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
theme: linear
```

在 `themes/linear/_config.yml` 中：

```yml
# `favicon` 地址，建议使用在线地址
favicon:

# 是否显示署名-相同方式共享 4.0 国际协议
declaration: true

# 个人链接 - 将展示在页面上方，博客标题和副标题之下
## 图标基础地址（如果部署在 https://username.github.io/repo/ 下，需要改为 `/repo/images/links/`）
linkiconbase: /images/links/
## 个人链接数组
links:
  - name: # 图标挂掉时显示的文字
    link: # 链接地址
    icon: # 图标名称，`themes/linear/source/images/links/` 文件夹下提供图标文件，有需要也可以自行添加。图标文件来源：

# comment
valine:
  enabled: true
  appId:
  appKey:
  placeholder:
  avatar:

# footer
## for users in China
icp:
## visitor counter
counter:
  enabled: true
  ### refer to https://github.com/syy11cn/hexo-theme-linear/blob/main/docs/guide.md
  url:
```

## 数学公式支持

默认情况下，hexo装载的渲染器为`hexo-renderer-marked`, 仅支持行间公式语法的数学公式渲染，而行内公式的渲染则不能实现。使用`hexo-renderer-markdown-it-plus`即可完全支持行内、行间的数学公式渲染。具体操作如下：

1. 在**博客根目录**下，运行如下指令：
   ```bash
    npm un hexo-renderer-marked --save #卸载默认的渲染器
    npm i hexo-renderer-markdown-it-plus --save # 高级的渲染器
   ``` 