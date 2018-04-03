# jQuery
On the test of jQuery （关于jQuery的测试）

项目结构代码：

   ![image](https://github.com/TouchDreamRen/jQuery/raw/master/screenshots/ProjectStructureCode.png)
    
有关jQuery的一些知识点：

        1.  第一个 jQuery 程序
        2.  jQuery 对象和 DOM 对象
        3.  基本选择器
        4.  层次选择器
        5.  基本过滤选择器
        6.  内容过滤选择器
        7.  可见性过滤选择器
        8.  属性过滤选择器
        9.  子元素过滤选择器
        10. 表单元素过滤选择器 
        11. 小结1
        12. 选择器练习
        13. 创建和插入节点
        14. 重写 JS 实验之分类添加内容
        15. 删除及清空节点
        16. 重写 JS 实验之员工管理
        17. 克隆和替换节点
        18. 包裹节点
        19. html() 方法 & val() 方法
        20. 小结2
        21. CSS DOM 操作
        22. 事件处理
        23. 动画  



例: 复选框全选全不选功能

        <!DOCTYPE html>
        <html>
          <head>  
            <meta charset="UTF-8">
            <title>Insert title here</title>
            <!-- 导入jQuery 库 -->
            <script type="text/javascript" src="script/jquery-1.7.2.js" ></script>
            <script type="text/javascript">
              //$(function(){})相当于window.onload，代码写在{}之间	
              $(function(){
                $("#checkedAll_2").click(function(){
                  var flag = this.checked;
                  $(":checkbox[name='items']").attr("checked",flag);
                });

                $(":checkbox[name='items']").click(function(){
                  $("#checkedAll_2").attr("checked",
                    $(":checkbox[name='items']").length == $(":checkbox[name='items']:checked").length)     
                });

              })
            </script>
          </head>
          <body>
            <form method="post" action="" >
              你爱好的运动是？<input type="checkbox" id="checkedAll_2"  />全选/全不选

              <br />
              <input type="checkbox" name="items" value="足球" />足球
              <input type="checkbox" name="items" value="篮球" />篮球
              <input type="checkbox" name="items" value="羽毛球" />羽毛球
              <input type="checkbox" name="items" value="排球" />排球
            </form>
          </body>
        </html>
      
效果图如下：

   ![image](https://github.com/TouchDreamRen/jQuery/raw/master/screenshots/test1.png)

