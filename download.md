---
layout: v2
title: Download
bodyclass: download-page
---

## 下载 Leaflet

<table>
	<tr>
		<th>版本</th>
		<th>说明</th>
	</tr>
	<tr>
		<td class="width100"><a href="http://cdn.leafletjs.com/downloads/leaflet-0.7.3.zip">Leaflet 0.7.3</a></td>
		<td>稳定版本, 发布于2013年11月18日，最后一次更新于2014年5月23日。</td>
	</tr>
	<!--<tr>
		<td class="width100"><a href="http://leaflet-cdn.s3.amazonaws.com/build/leaflet-0.6.4.zip">Leaflet 0.6.4</a></td>
		<td>Previous stable version, released on June 26, 2013 and last updated on July 25, 2013.</td>
	</tr>-->
	<tr>
		<td><a href="http://cdn.leafletjs.com/downloads/leaflet-1.0.0-b1.zip">Leaflet 1.0 beta 1</a></td>
		<td>1.0 beta 测试版本, 发布于2015年7月14日。</td>
	</tr>
	<tr>
		<td><a href="https://leafletjs-cdn.s3.amazonaws.com/content/build/master/dist/leaflet.zip">Leaflet 1.0-dev</a></td>
		<td>开发版本, 位于 <code>master</code> 分支</td>
	</tr>
</table>

[View Changelog](https://github.com/Leaflet/Leaflet/blob/master/CHANGELOG.md)

Note that the master version can contain incompatible changes,
so please read the changelog carefully when upgrading to it.

### 使用 CDN 服务器上的 Leaflet 版本

The latest stable Leaflet release is hosted on a CDN &mdash; to start using
it straight away, place this in the `head` of your HTML code:

    <link rel="stylesheet" href="http://cdn.leafletjs.com/leaflet-0.7.3/leaflet.css" />
    <script src="http://cdn.leafletjs.com/leaflet-0.7.3/leaflet.js"></script>

### 使用 Leaflet 下载版本

Inside the archives downloaded from the above links, you will see four things:

- `leaflet.js` - This is the minified Leaflet JavaScript code.
- `leaflet-src.js` - This is the readable, unminified Leaflet JavaScript, which is sometimes helpful for debugging.
- `leaflet.css` - This is the stylesheet for Leaflet.
- `images` - This is a folder that contains images referenced by `leaflet.css`. It must be in the same directory as `leaflet.css`.

Unzip the downloaded archive to your website's directory and add this to the `head` of your HTML code:

    <link rel="stylesheet" href="/path/to/leaflet.css" />
    <script src="/path/to/leaflet.js"></script> <!-- or use leaflet-src.js --!>

### Leaflet 源代码

These download packages above only contain the library itself.
If you want to download the full source code, including unit tests, files for debugging, build scripts, etc.,
you can <a href="https://github.com/Leaflet/Leaflet/releases">下载</a>
from the <a href="https://github.com/Leaflet/Leaflet">GitHub repository</a>.

### 从源代码编译 Leaflet

Leaflet build system is powered by the [Node.js](http://nodejs.org) platform,
which installs easily and works well across all major platforms.
Here are the steps to set it up:

 1. [下载并安装 Node](http://nodejs.org)
 2. Run the following commands in the command line:

 <pre><code>npm install -g jake
npm install</code></pre>

Now that you have everything installed, run `jake build` inside the Leaflet directory.
This will combine and compress the Leaflet source files, saving the build to the `dist` folder.

### 编译自定义版本的 Leaflet

To make a custom build of the library with only the things you need,
open `build/build.html` page of the Leaflet source code contents, choose the components
(it figures out dependencies for you) and then run the command generated with it.
