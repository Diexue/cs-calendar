# cs-calendar

##一、install 临时安装
npm install cs-calendar \<br>
添加进项目dependencies \<br>
npm install cs-calendar -s \<br>

##二、 项目中引用
        <calendar :calendarData="calendarData"@selectDate="selectDate"></calendar>
        import {calendar} from 'cs-calendar'
        import 'cs-calendar/dist/cs-calendar.min.css'
##三、注册
```Javascript
components:{
    calendar
}
```
##四、传递组件的对象参数calendarData
如：
```Javascript
    data() {
       return {
         calendarData:{
           width:375,//必填
           bg:"green",
         }
       }
     }

```
####calendarData具体参数
        * 1.width:整个日历组件的宽度----//必填
        * 2.moreSelect，是否显示两个日期选择的范围
        * 3.preColor：今天之前的日期的颜色
        * 4.preBan：今天之前的日期是否可以选择
        * 5.bg：选中后的背景色（未设置背景图片）
        * 6.color：选中后的文字颜色
        * 7.selectDate：单一选择的日期（格式：{year:2018,month:7,date:1}）
        * 8.selectMinDate：范围选中的第一天的日期对象{year,month,date}
        * 9.selectMaxDate：范围选中的最后一天的日期对象{year,month,date}
##五、选中时间返回父组件事件及参数
```Javascript
selectDate(e){
单一选择时：2018/6/29
范围选择时：2018/6/29-2018/6/29
}
```
