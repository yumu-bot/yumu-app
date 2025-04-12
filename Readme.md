## 贡献指南
1. 项目主要在 HBuilder X 上开发, 如需在 Vs Code 上开发请参考[文档](https://ask.dcloud.net.cn/article/36286)
2. 开发插件:
	- [Easy-git](https://easy-git.github.io/home/install) (非必需,可用 GitHub Desktop 等项目管理工具代替)
	- dart-sass 编译 (HBuilder X 内置,可直接安装)
	- [Prettier](https://ext.dcloud.net.cn/plugin?id=2025) (uni-app 插件市场安装)
```javascript
	// Prettier配置文档：https://prettier.io/docs/en/options.html
	module.exports = {
		printWidth: 180,
		tabWidth: 4,
		useTabs: false,
		semi: true,
		singleQuote: true,
		quoteProps: "as-needed",
		jsxSingleQuote: false,
		trailingComma: "all",
		bracketSpacing: true,
		bracketSameLine: true,
		arrowParens: "always",
		proseWrap: "preserve",
		htmlWhitespaceSensitivity: "ignore",
		vueIndentScriptAndStyle: false,
		endOfLine: "lf",
		embeddedLanguageFormatting: "auto",
		singleAttributePerLine: false,
		//自定义文件后缀对应的parser
		parsers: {
			".nvue": "vue",
			".ux": "vue",
			".uvue": "vue",
			".uts": "typescript",
			".js": "javascript"
		}
	}
```