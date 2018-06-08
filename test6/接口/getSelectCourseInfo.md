<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getSelectCourseInfo  [返回](../README.md)
用例： [查看选课](../用例/查看选课信息.md)[选课](../用例/选课.md)

- 功能：
    查看用户的选课信息。
    
- 权限：
    学生/老师：查看自己的信息，必须先登录，不能查看其他用户的信息。    
    
- API请求地址： 
    接口基本地址/v1/api/getSelectCourseInfo/<user_id>

- 请求方式 ：
    GET
      
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|用户的ID号。对应表USERS.USER_ID的值|
  
- 返回实例：

        {         
            "status": true,
            "info": null,
            "data": [
                          {
                            "course_id":"03051",
                            "course_name": "计算机网络", 
                            "semester":"大三上学期"
                            "name":"王五"
                            }, 
                           {
                            ...其他选课信息
                           }
                     ]            
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |ID|学号或者工号|
  |course_id|课程编号，一门课程的唯一标识|
  |course_name|课程名| 
  |semester|课程学期|                          
  |name|此课程的教师姓名，只有user_id对应的用户是学生才会存在此参数|                            

