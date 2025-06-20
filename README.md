# FBA美区亚马逊运费计算器

专业的FBA美区亚马逊运费计算器，免费计算亚马逊物流配送费用。支持公制英制单位转换，准确计算体积重量、计费重量和配送成本。

## 功能特点

- 🚚 **FBA运费计算** - 精准计算亚马逊物流费用
- 📏 **体积重量计算** - 自动计算体积重量和计费重量
- 🔄 **单位转换** - 支持公制（厘米/公斤）和英制（英寸/磅）
- 📊 **计算历史** - 自动保存计算记录
- 📱 **响应式设计** - 完美适配各种设备
- 🆓 **完全免费** - 无需注册，即用即走

## SEO优化配置

### 已实施的SEO优化

1. **页面标题优化**
   - 主要关键词："FBA美区亚马逊运费计算器"
   - 长尾关键词："免费在线物流配送费用计算工具"

2. **Meta标签完善**
   - Description: 包含核心关键词和功能描述
   - Keywords: 涵盖FBA运费、亚马逊物流、体积重量等相关词汇
   - 社交媒体优化 (Open Graph, Twitter Cards)

3. **结构化数据**
   - JSON-LD格式的Schema.org标记
   - WebApplication类型，便于搜索引擎理解

4. **网站资源文件**
   - `robots.txt` - 搜索引擎爬虫指导
   - `sitemap.xml` - 网站地图
   - `site.webmanifest` - PWA支持

5. **内容优化**
   - 语义化HTML结构
   - 关键词密度优化的页脚内容
   - 相关性强的内链结构

### 部署后需要做的事情

1. **更新域名**
   - 将所有文件中的 `https://your-domain.com` 替换为实际域名
   - 更新 `sitemap.xml` 中的URL
   - 更新HTML中的Open Graph URL

2. **Google Search Console配置**
   ```
   - 验证网站所有权
   - 提交sitemap.xml
   - 监控索引状态
   ```

3. **Google Analytics设置**
   ```html
   <!-- 在</head>前添加GA代码 -->
   <script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
   <script>
     window.dataLayer = window.dataLayer || [];
     function gtag(){dataLayer.push(arguments);}
     gtag('js', new Date());
     gtag('config', 'GA_MEASUREMENT_ID');
   </script>
   ```

4. **性能优化**
   - 启用Cloudflare的压缩和缓存
   - 配置CDN加速
   - 启用HTTP/2

### 关键词策略

**主要关键词：**
- FBA运费计算器
- 亚马逊运费计算
- FBA美区费用
- Amazon FBA Calculator

**长尾关键词：**
- FBA美区亚马逊运费计算器
- 亚马逊物流费用计算工具
- 体积重量计算器
- 跨境电商运费计算

**相关关键词：**
- 亚马逊物流
- FBA配送费
- 电商物流
- 运费计算工具

## 技术栈

- **前端**: HTML5, CSS3, JavaScript
- **样式**: 响应式设计，渐变背景
- **图标**: SVG favicon
- **SEO**: 完整的meta标签和结构化数据

## 文件结构

```
demoFBA/
├── index.html          # 主页面
├── styles.css          # 样式表
├── calculator.js       # 计算逻辑
├── favicon.svg         # SVG图标
├── site.webmanifest    # PWA清单
├── robots.txt          # 爬虫指导
├── sitemap.xml         # 网站地图
└── README.md           # 说明文档
```

## 使用方法

1. 选择单位制（公制或英制）
2. 输入商品尺寸（长、宽、高）
3. 输入实际重量
4. 点击"计算运费"按钮
5. 查看计算结果和历史记录

## 部署说明

### Cloudflare Pages部署

1. 将代码推送到GitHub仓库
2. 在Cloudflare Pages中连接GitHub仓库
3. 设置构建命令（静态站点无需构建）
4. 部署完成后配置自定义域名

### 自定义域名配置

1. 在Cloudflare中添加域名
2. 更新DNS记录指向Cloudflare
3. 配置SSL证书
4. 启用页面规则和性能优化

## License

MIT License - 可自由使用和修改
# FBA运费计算器

一个用于计算亚马逊物流配送费用的本地应用程序。

## 功能特点

- 🧮 **精确计算**：基于亚马逊官方费用标准进行计算
- 📏 **双单位制**：支持公制（厘米/公斤）和英制（英寸/磅）
- 📦 **智能分类**：自动判断商品尺寸分类
- 💾 **历史记录**：保存计算历史，支持查看和清空
- 🎨 **简洁界面**：现代化的用户界面设计
- 🖥️ **本地运行**：无需网络连接，保护数据隐私

## 使用方法

1. 打开 `index.html` 文件（可以直接双击打开，或用浏览器打开）
2. 选择单位制（公制或英制）
3. 输入商品的长、宽、高尺寸
4. 输入商品的实际重量
5. 点击"计算运费"按钮或自动计算
6. 查看计算结果和历史记录

## 计算原理（2024年2月后标准）

### 体积重计算
- **公制**：长×宽×高（cm）÷ 6000 = 体积重（kg）
- **英制**：长×宽×高（inch）÷ 139 = 体积重（lbs）

### 计费重量
取实际重量和体积重中的较大值作为计费重量

### 重要计费规则
- **重量取整**：所有超重计费都需要向上取整到整数磅
- **最小计费单位**：超出部分最小计费单位为1磅
- **小号标准**：按盎司计算，但不需要取整
- **大号大件**：超出3磅3部分按每4盎司向上取整计费

### 商品分类标准

1. **小号标准尺寸**：重量≤16磅，最长边≤15英寸，中边≤12英寸，最短边≤0.75英寸
2. **大号标准尺寸**：重量≤20磅，最长边≤18英寸，中边≤14英寸，最短边≤8英寸
3. **大而笨重**：重量≤50磅，最长边≤59英寸，中边≤33英寸，最短边≤33英寸，长度+周长≤130英寸
4. **超大号分类**：根据重量进一步细分

## 技术特点

- 纯前端实现，无需服务器
- 使用 HTML5 + CSS3 + JavaScript
- 响应式设计，支持移动设备
- 数据本地存储，保护隐私

## 文件结构

```
demoFBA/
├── index.html      # 主页面
├── styles.css      # 样式文件
├── calculator.js   # 计算逻辑
└── README.md       # 说明文档
```

## 浏览器兼容性

支持所有现代浏览器：
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 更新日志

### v1.1.0
- 修正计费逻辑，采用2024年2月后标准
- 实现重量向上取整功能
- 修正超重计费逻辑（最小1磅）
- 优化小号标准尺寸盎司计算

### v1.0.0
- 初始版本发布
- 支持双单位制计算
- 历史记录功能
- 响应式界面设计