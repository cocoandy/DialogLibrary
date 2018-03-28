# DialogLibrary
先上传个小小的时间选择器和日期选择器

## 使用的方法

### 先依赖：

* Project: build.gradle:

```
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  ```
  * Module: build.gradle:
  
  ```
	dependencies {
	        compile 'com.github.cocoandy:DialogLibrary:1.0.1'
	}
  ```
  
### 然后使用：

* 时间选择  

```
        customDatePicker1 = new CustomDatePicker(this, new CustomDatePicker.ResultHandler() {
            @Override
            public void handle(String time) { // 回调接口，获得选中的时间
                currentDate.setText(time.split(" ")[0]);
            }
        }, "2010-01-01 00:00", now); // 初始化日期格式请用：yyyy-MM-dd HH:mm，否则不能正常运行
        
         //显示
         customDatePicker1.show(currentDate.getText().toString());
```
* 日期选择
```
        customDatePicker1 = new CustomDatePicker(this, new CustomDatePicker.ResultHandler() {
            @Override
            public void handle(String time) { // 回调接口，获得选中的时间
                currentDate.setText(time.split(" ")[0]);
            }
        }, "2010-01-01 00:00", now); // 初始化日期格式请用：yyyy-MM-dd HH:mm，否则不能正常运行
        
        //显示
        customDatePicker2.show(currentTime.getText().toString());
```
