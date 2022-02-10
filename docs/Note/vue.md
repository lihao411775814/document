### package.json配置说明

#### 版本说明

> ```vue
> "vue": "^2.5.2",
> “2.5.2” 大版本.次要版本.小版本
> "^3.6.5" 不能低于3.6.5，但是不能修改大版本
> "~3.6.5" 不能低于3.6.5，但是不能修改大版本和次要版本号
> ```

#### dependencies 与 devDependencies

> devDependencies中的插件适用于开发环境使用，dependencies则是要发布到生产环境下

### main.js 配置说明

#### 路径说明

|  ./  |  同级目录  |
| :--: | :--------: |
| ../  | 上一级目录 |
|  @/  | src根目录  |

### Vuex组成

1. State： 数据仓库
2. getter：用来获取数据
3. Mutation：用来修改数据
4. Action：用来提交修改（Mutation）
