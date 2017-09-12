## mall-tuangou

仿百度糯米的O2O商城——MALL团购网

> 正在更新...

## 整理和优化

1. 扩展类库目录`extend`下封装个人类库

	* 地图服务类`extend/Map.php`：使用[百度地图API](http://lbsyun.baidu.com/)实现
	* 邮件服务类`extend/Mail.php`：使用[PHPMailer](https://github.com/PHPMailer/PHPMailer)）实现

2. 使用到的`PHP`第三方依赖均使用`Composer`管理

	* [PHPMailer](https://github.com/PHPMailer/PHPMailer)

3. 过滤非法数据
	
	* 几乎所有`CRUD`操作均使用了验证器`Validate`，统一整合在公共验证器`application/common/validate.php`文件

3. SQL优化

	* 数据表操作主要使用`DB`的方法
	* 字段过滤查询，主要使用`DB`的`field`方法

4. 个人的所有自定义函数在`application/common.php`文件

5. 商户模块的`Session`用`Redis`存储，配置参数在`application/bis/config.php`文件

## 必要的说明

1. 邮件服务类相关配置

	* `application/extra/mail.php.example` 是邮件服务的参数配置文件，拷贝后去掉`.example`后缀。详细配置参考[点这里](https://github.com/PHPMailer/PHPMailer/blob/master/class.phpmailer.php)

2. 部分前端资源现未上传

	* 后台模板框架`H-ui.admin`所需文件未上传（太大），所以`public/static/admin/h-ui-admin`目录下为空

## 测试账号密码

	| 账号 | 密码 | 角色 |
	|------|-----------|------|
	| 李雷 | ll11111111 | 商户 |
	| 韩梅梅 | hmm11111111 | 商户 |
	| 王雪 | wx11111111 | 商户 |
	| 林立 | ll11111111 | 商户 |
