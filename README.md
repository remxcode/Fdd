# Fdd
### 方法清单
#### 1注册账号 accountRegister
#####1)此接口针对接入平台已有账号体系,判断open_id是否存在,存在则返回对应账号。否则随机生成账号并返回账号
#####2)open_id是接入方给用户定义的唯一标识,注册成功返回的customer_id客户编号是用户在法大大的唯一标识
#####3)一个用户只需要注册一次即可,open_id已存在则返回对应customer_id,否则随机生成customer_id返回。
#### 参数可查看文档或进方法实体查看

#### 2获取企业实名认证地址 getCompanyVerifyUrl
####1)此接口返回法大大实名认证页面url,接入方拿到url后在浏览器中打开认证页面。
####2)一个用户只获取一笔认证链接进行一次认证即可,如果用户信息存在变更的情况(证件号除外的企业名称、法人等),可以使用同一个customer_id客户编号再次请求获取新的认证链接进行实名认证,每次请求返回的都是新的认证交易号和认证链接url
####3)customer_id绑定信息是在申请证书这一步,指定对应认证交易号申请实名证书进行绑定。
####4) 一个customer_id只能绑定一个用户主体,判断用户主体的唯一标识是证件号,申请实名证书后该customer_id无法再次绑定其它不同用户认证交易号去申请证书。
#### 参数可查看文档或进方法实体查看

#### 3获取个人实名认证地址 getPersonVerifyUrl
####1)此接口返回法大大实名认证页面url,接入方拿到url后在浏览器中打开认证页面。
####2)一个用户只获取一笔认证链接进行一次认证即可,如果用户信息存在变更的情况(证件号除外的企业名称、法人等),可以使用同一个customer_id客户编号再次请求获取新的认证链接进行实名认证,每次请求返回的都是新的认证交易号和认证链接url
####3)customer_id绑定信息是在申请证书这一步,指定对应认证交易号申请实名证书进行绑定。
####4) 一个customer_id只能绑定一个用户主体,判断用户主体的唯一标识是证件号,申请实名证书后该customer_id无法再次绑定其它不同用户认证交易号去申请证书。
#### 参数可查看文档或进方法实体查看

#### 4实名证书申请 applyCert
####1)调用此接口可以给相关账号颁发证书。
#### 参数可查看文档或进方法实体查看

#### 5印章上传 addSignature
####1)新增用户签章图片
#### 参数可查看文档或进方法实体查看

#### 6自定义印章 customSignature
####1)获取用户自定义签章图片
#### 参数可查看文档或进方法实体查看

#### 7合同上传 uploadDocs
####1)接入平台将待签署的pdf文档通过此接口将文档传输到法大大
#### 参数可查看文档或进方法实体查看

#### 8模板上传 uploadTemplate
####1)此接口与模板填充接口配合使用,接入方预先将制作好的PDF模板通过此接口上传到法大大
#### 参数可查看文档或进方法实体查看

#### 9模板查看 viewTemplate
####1)模板预览
#### 参数可查看文档或进方法实体查看

#### 10模板下载 templateDownload
####1)模板下载
#### 参数可查看文档或进方法实体查看

#### 11模板删除 templateDelete
####1)模板删除
#### 参数可查看文档或进方法实体查看

#### 12模板填充 generateContract
####1)将需填充的内容通过模板填充接口传入,即可生成合同供签署操作
#### 参数可查看文档或进方法实体查看

#### 13自动签署 extSignAuto
####1)自动签接口不需要用户亲自操作,当接入平台调用此接口时,就会在指定的电子合同上签上指定用户的电子章,省略了用户交互的步骤。
#### 参数可查看文档或进方法实体查看

#### 14手动签署 extSign
####1)该接口为页面接口,接入方平台可以在合适的业务场景嵌入该接口链接,引导客户至法大大进行文档签署(比如可以在接入方平台网站上放置一个按钮,该按钮触发跳转至法大大 或将法大大签章页面嵌入接入方流程)。法大大根据浏览器UA信息,自动加载签章界面对应的PC web版本或移动HTML5版本。用户在法大大的签署页面中进行签署操作。
#### 参数可查看文档或进方法实体查看

#### 15查看合同 viewContract
####1)合同预览
#### 参数可查看文档或进方法实体查看

#### 16合同下载 downLoadContract
####1)获取下载文件或者文件链接
#### 参数可查看文档或进方法实体查看

#### 17合同归档 contractFiling
####1)接入平台更新合同签署状态为-签署完成,法大大将把合同所有相关操作记录进行归档存证。归档后将不能再对文档再进行签署操作。
#### 参数可查看文档或进方法实体查看

#### 18通过uuid下载文件getFile
####1)提供通过uuid下载文件功能接口,请求参数一律用字符串表示。
#### 参数可查看文档或进方法实体查看

#### 19查询个人实名认证信息 findPersonCertInfo
####1)接入方主动发起实名认证信息查询。
#### 参数可查看文档或进方法实体查看

#### 查询企业实名认证信息 findCompanyCertInfo
####1)接入方主动发起实名认证信息查询。
#### 参数可查看文档或进方法实体查看
