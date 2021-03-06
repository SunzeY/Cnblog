```javascript
<!-- menu html -->
<div class="container">
    <div class="menu-wrap optiscroll" id="menuWrap" style="display:none">
        <nav class="menu">

            <!-- 个人简介 -->
            <div class="introduce-box">
                <div class="introduce-head">
                    <div class="introduce-via" id="menuBlogAvatar"></div>
                </div>
                <div id="introduce"></div>
            </div>

            <!-- 导航 -->
            <div class="nav-title"></div>
            <div class="icon-list">
                <ul>
                    <li><a href="https://www.cnblogs.com/zery-blog/" target="_self">首页</a></li>
                    <li><a href="https://msg.cnblogs.com/send/zery-blog" target="_blank">联系</a></li>
                    <li><a href="https://www.cnblogs.com/zery-blog/rss" target="_blank">订阅</a></li>
                    <li><a href="https://i.cnblogs.com/" target="_blank">管理</a></li>
                    <li><a href="https://github.com/SunzeY/" target="_blank">GitHub</a></li>
                    <li><a href="https://www.cnblogs.com/" target="_blank">CNBlogs</a></li>
                </ul>
            </div>

            <!-- 最新随笔 -->
            <div class="m-list-title"><span>最新随笔</span></div>
            <div class="m-icon-list" id="sb-sidebarRecentposts"></div>

            <!-- 我的标签 -->
            <div class="m-list-title"><span>我的标签</span></div>
            <div class="m-icon-list" id="sb-toptags"></div>

            <!-- 随笔分类 -->
            <div class="m-list-title"><span>随笔分类</span></div>
            <div class="m-icon-list" id="sb-classify"></div>

            <!-- 随笔档案 -->
            <div class="m-list-title"><span>随笔档案</span></div>
            <div class="m-icon-list" id="sb-record"></div>

            <!-- 阅读排行 -->
            <div class="m-list-title"><span>阅读排行</span></div>
            <div class="m-icon-list" id="sb-topview"></div>

            <!-- 推荐排行 -->
            <div class="m-list-title"><span>推荐排行</span></div>
            <div class="m-icon-list" id="sb-topDiggPosts"></div>

            <!-- 自定义列表 -->
            <span id="menuCustomList"></span>
        </nav>
        <button class="close-button" id="close-button">Close Menu</button>
        <div class="morph-shape" id="morph-shape" data-morph-open="M-7.312,0H15c0,0,66,113.339,66,399.5C81,664.006,15,800,15,800H-7.312V0z;M-7.312,0H100c0,0,0,113.839,0,400c0,264.506,0,400,0,400H-7.312V0z">
            <svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" viewBox="0 0 100 800" preserveAspectRatio="none">
                <path d="M-7.312,0H0c0,0,0,113.839,0,400c0,264.506,0,400,0,400h-7.312V0z"/>
            </svg>
        </div>
    </div>
    <button class="menu-button" id="open-button">MENU</button>
    <div class="content-wrap" id="content-wrap"></div><!-- /content-wrap -->
</div>
<!-- menu html end -->

<!-- banner html -->
<div class="main-header">
    <canvas id="notHomeTopCanvas" style=" position: absolute;margin: auto;width: 100%;height: 100%;top: 0;bottom: 0;left: 0;right: 0;"></canvas>
    <div class="vertical">
        <div class="main-header-content inner">
            <link href="https://fonts.googleapis.com/css?family=Playball" rel="stylesheet">
            <h1 class="page-title" style="font-family: 'Playball', cursive;" id="homeTopTitle"></h1>
            <h2 class="page-description" id="hitokoto"></h2>
            <h3 class="page-author" id="hitokotoAuthor"></h3>
        </div>
    </div>
    <a class="scroll-down" href="javascript:void(0);" data-offset="-45">
        <span class="hidden">Scroll Down</span>
        <i class="scroll-down-icon iconfont icon-fanhui"></i>
    </a>
</div>
<!-- banner html end -->

<!-- global var -->
<script type="text/javascript">

    /*!
     * UPDATES AND DOCS AT: https://github.com/BNDong
     * https://www.cnblogs.com/bndong/
     * @author: BNDong, dbnuo@foxmail.com
     **/

    /**
     * 博客全局配置，请仔细配置！！
     */
    window.cnblogsConfig = {

        // ---- GitHub文件源配置 ----
        GhUserName: 'BNDong', // GitHub用户名(不是昵称)，注意大小写
        GhRepositories: 'Cnblogs-Theme-SimpleMemory', // GitHub主题仓库名称
        GhVersions : '81410deb9d6577d9244e842999ed2a407d433868', // GitHub提交版本哈希值，根据版本加载代码，我有时候会提交代码进行调试，大家最好加载我仓库代码此处的版本 https://github.com/BNDong/Cnblogs-Theme-SimpleMemory/commits/master

        // ---- 基础信息配置 ----custom
        blogUser      : "Zery", // 博主名称，文章后缀和主页图片上都会使用此名称
        blogAvatar    : "http://sun-zeyi.gitee.io/cnblog/pictures/head.png", // 用户头像URL
        blogStartDate : "2021-3-23", // 入园时间，年-月-日，入园时间查看方法：鼠标停留园龄时间上，会显示入园时间

        // ---- 菜单配置 ----
        menuCustomList: { // 自定义菜单数据，显示在正常数据下方
        },

        // ---- 网站配置 ----
        webpageTitleOnblur        : "Hi, this is Zery", // 当前页失去焦点，页面title显示文字
        webpageTitleOnblurTimeOut : 500, // 当前页失去焦点，页面title变化，延时时间，单位毫秒
        webpageTitleFocus         : "welcome back", // 当前页获取焦点，页面title显示文字，显示后延时恢复原title
        webpageTitleFocusTimeOut  : 1000, // 当前页获取焦点，页面title变化，延时时间，单位毫秒
        webpageIcon : "http://sun-zeyi.gitee.io/cnblog/pictures/favicon.ico", // 网站图标

        // ---- 进度条配置 ----
        progressBar: {
            id      : 'top-progress-bar',
            color   : '#77b6ff',
            height  : '2px',
            duration: 0.2
        },

        // ---- Loading配置 ----
        loading: {
            rebound: {
                tension: 16,
                friction: 5
            },
            spinner: {
                id: 'spinner',
                radius: 90,
                sides: 3,
                depth: 4,
                colors: {
                    background: '#f0f0f0',
                    stroke: '#272633',
                    base: null,
                    child: '#272633'
                },
                alwaysForward: true, // When false the spring will reverse normally.
                restAt: 0.5,         // A number from 0.1 to 0.9 || null for full rotation
                renderBase: false
            }
        },


        // ---- 页面动效配置 ----
        homeTopAnimationRendered: true, // true || false ,是否渲染主页头图动效
        homeTopAnimation: { // 主页头图动效设置
            radius: 15,
            density: 0.2,
            color: 'rgba(255,255,255, .2)', // 颜色设置，“random” 为随机颜色
            clearOffset: 0.3
        },

        essayTopAnimationRendered: true, // true || false ,是否渲染随笔页头图动效
        essayTopAnimation: { // 随笔页头图动效设置
            triW : 14,
            triH : 20,
            neighbours : ["side", "top", "bottom"],
            speedTrailAppear : .1,
            speedTrailDisappear : .1,
            speedTriOpen : 1,
            trailMaxLength : 30,
            trailIntervalCreation : 100,
            delayBeforeDisappear : 2,
            colors: [
                '#96EDA6', '#5BC6A9',
                '#38668C', '#374D84',
                '#BED5CB', '#62ADC6',
                '#8EE5DE', '#304E7B'
            ]
        },

        bgAnimationRendered: true, // true || false ,是否渲染背景动效
        backgroundAnimation : { // 背景动效设置
            colorSaturation: "60%",
            colorBrightness: "50%",
            colorAlpha: 0.5,
            colorCycleSpeed: 5,
            verticalPosition: "random",
            horizontalSpeed: 200,
            ribbonCount: 3,
            strokeSize: 0,
            parallaxAmount: -0.2,
            animateSections: true
        },

        // ---- 主页配置 ----
        homeTopImg    : [ // 主页图片Url，推荐尺寸>= 1920*1080，支持多张，每次刷新随机设置一张
            "http://sun-zeyi.gitee.io/cnblog/pictures/liyue.jpg",
            "http://sun-zeyi.gitee.io/cnblog/pictures/mengde.jpg",
            "http://sun-zeyi.gitee.io/cnblog/pictures/bar.jpg"
        ],
        homeBannerText: "Zery's learning notes about computer science", // 主页头图上的标语，设置此选项会固定显示文字，默认为空，自动获取一句。

        // ---- 随笔页配置 ----
        essayTopImg: [ // 随笔页图片Url，支持多张，每次刷新随机设置一张
            "http://sun-zeyi.gitee.io/cnblog/pictures/liyue.jpg",
            "http://sun-zeyi.gitee.io/cnblog/pictures/mengde.jpg",
            "http://sun-zeyi.gitee.io/cnblog/pictures/bar.jpg"
        ],
        essayCodeHighlightingType: 'cnblogs', // 代码主题插件类型：cnblogs || highlightjs || prettify
        essayCodeHighlighting: 'cnblogs', // 代码高亮主题，具体主题参考文档
        essaySuffix:{ // 随笔后缀处配置
            aboutHtml    : 'undergraduate major in CS', // 关于博主，不配置使用默认
            copyrightHtml: '', // 版权声明，不配置使用默认
            supportHtml  : ''  // 声援博主，不配置使用默认
        },

        // ---- 页脚配置 ----
        bottomBlogroll: [ // 友情链接，[[链接名,链接]....]
        ],
        bottomText: {  // 页脚标语
            icon: "", // 图标
            left : "**其斩棘自伤、踏铁疲困痛乎 ？", // 图标左侧文字
            right: "其事后自责，悔之不及痛乎？"  // 图标右侧文字
        },

        // ---- 控制台输出 ----
        consoleList: [
            ['BNDong CNBlogs', 'https://www.cnblogs.com/zery-blog/'],
            ['BNDong GitHub', 'https://github.com/SunzeY/Cnblog'],
            ['BNDong Email', '983499284@qq.com']
        ],
        themeAuthor: false // 是否显示主题作者（原谅我的臭屁，O(∩_∩)O哈哈~）
    };

    // start cache
    $.ajaxSetup({cache: true});

    // load loadingJs
    $.getScript(getJsDelivrUrl('loading.js'), function () {

        // Loading start
        pageLoading.initRebound();
        pageLoading.initSpinner();
        pageLoading.spinner.init(pageLoading.spring, true);

        $.getScript(getJsDelivrUrl('jquery.mCustomScrollbar.min.js'), function () {
            $.getScript(getJsDelivrUrl('require.min.js'), function () {
                $.getScript(getJsDelivrUrl('config.js'), function () {
                    var staticResource = [
                        'optiscroll', 'ToProgress', 'rotate',
                        'snapSvg', 'classie', 'main4', 'tools'];
                    require(staticResource, function() {
                        require(['base'], function() {
                            (new Base).init();
                        });
                    });
                });
            });
        });
    });

    // get file url
    function getJsDelivrUrl(file, directory) {
        file = setFileNameMin(file, directory);
        return 'https://cdn.jsdelivr.net/gh/'+(window.cnblogsConfig.GhUserName)+'/'+(window.cnblogsConfig.GhRepositories)+'@'+(window.cnblogsConfig.GhVersions)+'/' + (file ? file : '');
    }

    // optimization file name
    function setFileNameMin(file, directory) {
        if (typeof file == 'undefined') return '';
        var suffix  = null,fileArr = file.split('.');
        if (fileArr.length > 0 && $.inArray(fileArr[(fileArr.length -1)], ['js', 'css']) != -1)
            {suffix    = fileArr.pop(); directory = suffix;}
        file.search('.min') == -1 && fileArr.push('min');
        suffix != null && fileArr.push(suffix);
        return (typeof directory !== 'undefined' ? (directory + '/' + fileArr.join('.')) : (fileArr.join('.')));
    }
</script>
<!-- global var end -->
```



