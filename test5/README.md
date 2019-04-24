# 实验5：图书管理系统数据库设计与界面设计
## 1.数据库表设计
### 1.1. Reader表
<table border="1px" cellspacing="0">
    <tr align="center">
        <td>字段</td>
        <td>类型</td>
        <td>主键，外键</td>
        <td>可以为空</td>
        <td>默认值</td>
        <td>约束</td>
        <td>说明</td>
    </tr>
    <tr align="center">
        <td>reader_id</td>
        <td>int(25)</td>
        <td>主键</td>
        <td>否</td>
        <td></td>
        <td>约束</td>
        <td>用于读者的唯一标识</td>
    </tr>
    <tr align="center">
        <td>reader_name</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>读者姓名</td>
    </tr>
    <tr align="center">
        <td>book_number</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td>0</td>
        <td></td>
        <td>已借书数量</td>
    </tr>
    <tr align="center">
        <td>out_date_book_num</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>逾期未还数量</td>
    </tr>
    <tr align="center">
        <td>limit_book_date_num</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>最大可借期限</td>
    </tr>
    <tr align="center">
        <td>limit_book_num</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>最大可借数量</td>
    </tr>
</table>

### 1.2. Manager表

<table border="1px" cellspacing="0">
    <tr align="center">
        <td>字段</td>
        <td>类型</td>
        <td>主键，外键</td>
        <td>可以为空</td>
        <td>默认值</td>
        <td>约束</td>
        <td>说明</td>
    </tr>
    <tr align="center">
        <td>manager_id</td>
        <td>int(25)</td>
        <td>主键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>管理员编号id</td>
    </tr>
    <tr align="center">
        <td>manager_name	</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>管理员姓名</td>
    </tr>
    <tr align="center">
        <td>manager_password	</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td>111111</td>
        <td></td>
        <td>密码</td>
    </tr>
    <tr align="center">
        <td>manager_mail	</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>邮箱</td>
    </tr>
    <tr align="center">
        <td>manager_address</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>地址</td>
    </tr>
</table>

### 1.3. Book表
<table border="1px" cellspacing="0">
    <tr align="center">
        <td>字段</td>
        <td>类型</td>
        <td>主键，外键</td>
        <td>可以为空</td>
        <td>默认值</td>
        <td>约束</td>
        <td>说明</td>
    </tr>
    <tr align="center">
        <td>book_id	</td>
        <td>int(25)</td>
        <td>主键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>图书编号id</td>
    </tr>
    <tr align="center">
        <td>left_quantity		</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td>0</td>
        <td></td>
        <td>剩余数量</td>
    </tr>
    <tr align="center">
        <td>type		</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>种类</td>
    </tr>
    <tr align="center">
        <td>book_name		</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>书名</td>
    </tr>
    <tr align="center">
        <td>author	</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>作者</td>
    </tr>
    <tr align="center">
        <td>press		</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>出版社</td>
    </tr>
</table>

### 1.4. Borrow_Record表
<table border="1px" cellspacing="0">
    <tr align="center">
        <td>字段</td>
        <td>类型</td>
        <td>主键，外键</td>
        <td>可以为空</td>
        <td>默认值</td>
        <td>约束</td>
        <td>说明</td>
    </tr>
    <tr align="center">
        <td>record_id		</td>
        <td>int(25)</td>
        <td>主键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>记录唯一标识</td>
    </tr>
    <tr align="center">
        <td>reader_id	</td>
        <td>int(25)</td>
        <td>外键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>读者编号id（参照表：Reader）</td>
    </tr>
    <tr align="center">
        <td>book_id	</td>
        <td>int(25)</td>
        <td>外键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>图书编号id(参照表Book)</td>
    </tr>
    <tr align="center">
        <td>manager_id		</td>
        <td>int(25)</td>
        <td>外键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>管理员id（参照表：Manager）</td>
    </tr>
    <tr align="center">
        <td>unusual_return_id	</td>
        <td>int(25)</td>
        <td>外键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>异常还书id（参照表：Unusual_Return）</td>
    </tr>
    <tr align="center">
        <td>borrowed_time</td>
        <td>varchar(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>已借阅时长</td>
    </tr>
</table>

### 1.5. Leave_Word表

<table border="1px" cellspacing="0">
    <tr align="center">
        <td>字段</td>
        <td>类型</td>
        <td>主键，外键</td>
        <td>可以为空</td>
        <td>默认值</td>
        <td>约束</td>
        <td>说明</td>
    </tr>
    <tr align="center">
        <td>word_id	</td>
        <td>int(25)</td>
        <td>主键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>订阅id</td>
    </tr>
    <tr align="center">
        <td>book_name			</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>书名</td>
    </tr>
    <tr align="center">
        <td>author	</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>作者</td>
    </tr>
    <tr align="center">
        <td>press		</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>出版社	</td>
    </tr>
    <tr align="center">
        <td>desc		</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>描述</td>
    </tr>
</table>

### 1.6. Unusual_Return 表

<table border="1px" cellspacing="0">
    <tr align="center">
        <td>字段</td>
        <td>类型</td>
        <td>主键，外键</td>
        <td>可以为空</td>
        <td>默认值</td>
        <td>约束</td>
        <td>说明</td>
    </tr>
    <tr align="center">
        <td>unusual_return_id		</td>
        <td>int(25)</td>
        <td>主键</td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>异常还书id</td>
    </tr>
    <tr align="center">
        <td>unusual_return_fine		</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>罚款金额</td>
    </tr>
    <tr align="center">
        <td>desc		</td>
        <td>varchar2(100)</td>
        <td></td>
        <td>否</td>
        <td></td>
        <td></td>
        <td>描述</td>
    </tr>
</table>

## 2. 界面设计
### 2.1. 借书界面设计
#### 图一
![binaryTree](https://github.com/Ryanaa/is_analysis/blob/master/test5/a.png)
#### 图二
![binaryTree](https://github.com/Ryanaa/is_analysis/blob/master/test5/b.png)


#### 用例图参见：借书用例
#### 类图参见：借书类，读者类
#### 顺序图参见：借书顺序图
#### API接口如下：

#### 1.查找图书
#### 功能：用于获取所查询的图书
#### 请求地址： http://myBook/v1/selectBookByName
#### 请求方法：POST
#### 请求参数：
<table border="1px" cellspacing="0">
    <tr align="center">
        <td>参数名称</td>
        <td>必填</td>
        <td>说明</td>
    </tr>
    <tr align="center">
        <td>access_token</td>
        <td>是</td>
        <td>用于验证请求合法性的认证信息。</td>
    </tr>
    <tr align="center">
        <td>book_name</td>
        <td>是</td>
        <td>用于查询图书信息的关键词。</td>
    </tr>
    
</table>

#### 返回实例：

{
    "info": "查询活着。",
    "data": {
        "book_id": "1",
        "left_quantity": "20",
        "type": "战争",
        "book_name": "活着",
        "author": "余华",
        "press": "新华出版社",
    },
    "code": 200
}
#### 返回参数说明：
<table border="1px" cellspacing="0">
    <tr align="center">
        <td>参数名称</td>
        <td>说明</td>
    </tr>
    <tr align="center">
        <td>info</td>
        <td>返回信息</td>
    </tr>
    <tr align="center">
        <td>data</td>
        <td>所查询的书籍信息</td>
    </tr>
    <tr align="center">
        <td>code</td>
        <td>返回码</td>
    </tr>
</table>




#### 2.提交借阅
#### 功能：借阅当前所选择的图书
#### 请求地址：http://myBook/v1/borrow
#### 请求方法：POST
#### 请求参数：
<table border="1px" cellspacing="0">
    <tr align="center">
        <td>参数名称</td>
        <td>必填</td>
        <td>说明</td>
    </tr>
    <tr align="center">
        <td>access_token</td>
        <td>是</td>
        <td>用于验证请求合法性的认证信息。</td>
    </tr>
    <tr align="center">
        <td>book_id</td>
        <td>是</td>
        <td>用于表示当前所借阅图书id。</td>
    </tr>
       <tr align="center">
            <td>reader_id</td>
            <td>是</td>
            <td>用于表示当前读者的id</td>
        </tr>
</table>

#### 返回实例：

{
    "info": "借阅成功。",
    "code": 200
}
#### 返回参数说明：
<table border="1px" cellspacing="0">
    <tr align="center">
        <td>参数名称</td>
        <td>说明</td>
    </tr>
    <tr align="center">
        <td>info</td>
        <td>返回信息</td>
    </tr>
    <tr align="center">
        <td>code</td>
        <td>返回码</td>
    </tr>
</table>