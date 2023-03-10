# 一· 函数组件 与 类组件的使用

## 1. 高阶组件 表达的意思就是 可以拦截 组件的渲染 需要做出一些事情 比如有的页面需要登录才可以显示页面

## 1.1 什么是高阶组件

```sh
  1.11 把组件当做参数传 就是高阶组件
        或 返回return 一个组件 也是高阶组件
  1.12 详情login_ayth.jsx文件
```

# 二· react 的 styley(css 样式)编写 使用 styled-components 第三方库 (css in js)

### 详情请看 detail—style.js 文件

```sh
  安装 npm install styled-components
```

# 三· 动态添加 className 使用第三方库 classnames

### 详情请看 detail.jsx 文件 第 57 行 通过布尔值 动态添加 className

```sh
安装 npm install classnames

```

# 四· 安装路由

```sh
1. 安装 npm install react-router-dom

2. index.js 文件中 得把App组件标签包裹 路由模式(哈希等模式)

2.1 类组件使用 router 详情在 App类组件使用router.jsx文件中 或下面的 4.1 class 组件中使用 router

3. 函数组件 router 统一使用一个文件管理 并且使用了懒加载模式打包发布的时候就是一个个js文件
    (详情在router文件中)
    就得在使用 Suspense 进行包裹
    路由懒加载发布后浏览网页 下载路由懒加载单独包的时候会有缓冲 就让界面显示 fallback 里的内容

    列如：
      root.render(
        <HashRouter>
          <Suspense fallback={<h1>loading...</h1>}>
            <App />
          </Suspense>
        </HashRouter>
      )
  Tips：
    使用懒加载 router 需要 转化为 组件标签
```

## 4.1 class 组件中使用 router

```sh
 站位符没有 直接使用
        <Routes>
          <Route path="/" element={<Navigate to="/home" />} />
          <Route path="/home" element={<Homet />} />
          <Route path="/detail" element={<Detail />}>
            {/* 二级路由 */}
            <Route path="/detail" element={<Navigate to="/detail/rom" />} />
            <Route path="/detail/rom" element={<DetailRom />} />
            <Route path="/detail/song" element={<DetailSong />} />
          </Route>
          <Route path="/page" element={<Home />} />
          <Route path="*" element={<NotFound />} />
        </Routes>
```

## 4.2 函数组件中使用 router

```sh
{useRoutes(routes)} //只能在函数组件中使用
详情 在02文件夹中 App函数组件的router使用.jsx 文件中

使用 子路由 需要占位符 <Outlet />

```

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
