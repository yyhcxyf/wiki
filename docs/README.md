---
标题：主页
---

#编程入门(C/C++)

<小的>
2023年秋季，讲师：张焕晨
</小的>

！！！注意“”

    <span id="正在进行"降价样式="显示：无；">
    ：火：进行中
    </span>
    <span id="incoming"markdown style="display:none；">
    ：alarm_clock:incoming
    </span>
    <br/>
    <big style="font-size:2EM；"><bold id="hw-title">工作分配2</bold>&mdash；<span id="rest-time"></span></big><br/>
    <small><span id="time-type">到期时间：</span><span id="到期时间"></span></small>

<脚本>
Const计划表={
'作业1':['2023/09/2400:00:00GMT+08:00','2023/10/0823:59:00GMT+08:00'],
'作业2':['2023/10/0800:00:00GMT+08:00','2023/10/2223:59:00GMT+08:00'],
'任务3':['2023/10/2200:00:00GMT+08:00','2023/11/0523:59:00GMT+08:00'],
'作业4':['2023/11/0500:00:00GMT+08:00','2023/11/1923:59:00GMT+08:00'],
'项目1':['2023/11/1923:00:00GMT+08:00','2023/12/1723:59:00GMT+08:00'],
'项目2':['2023/12/2723:00:00GMT+08:00','2024/01/2123:59:00GMT+08:00'],
};
功能setime(){
常数cur_date=新的日期()；
让到期日(_D)=无效的；
让 标题='';
让 状态='已完成';
为(让[k，[开始,结束]] …… 的对象。 条目(计划表)) {
开始=新的日期(开始);
end=新的日期(结束)；
如果(开始时间<cur_date&&cur_date<结束时间){
due_date=end；
title=k；
状态='正在进行';
打破;
}其他如果(cur_date>end&&(end>due_date||due_date===无效的)){
title=k；
due_date=end；
}其他如果(cur_date<开始&&(开始时间<due_date||due_date===无效的)){
title=k；
到期日=开始；
;
}
}
if(状态==='正在进行'){
文件。getElementById(“正在进行”)。风格。显示='inline'；
文件。getElementById('incoming')。风格。显示='无'；
文件。getElementById('time-type')。innerHTML='到期时间：'；
}else if(状态==='incoming'){
文件。getElementById('incoming')。风格。显示='inline'；
文件。getElementById(“正在进行”)。风格。显示='无'；
文件。getElementById('time-type')。innerHTML='释放时间：'；
}
document.getElementById('due-time').innerHTML=due_date.toLocaleString()；
document.getElementById('hw-title').innerHTML=title；
让diff=due_date.getTime()-cur_date.getTime()；
设str="；
            if (diff < 0) {
                str = 'Finished';
            } else {
                let s = diff / 1000;
                let m = s / 60;
                let h = m / 60;
                let d = h / 24;
                if (d == 1) {
                    str += '1 day ';
                } else if (d > 1) {
                    str += Math.floor(d) + ' days ';
                }
                str += `${Math.floor(h)%24}h ${Math.floor(m)%60}m ${Math.floor(s)%60}s`;
            }
            let el = document.getElementById('rest-time');
            el.innerHTML = str;
        }
        setTime();
        setInterval(setTime, 500);
</script>

## Tentative Schedule

<table markdown>
<tbody markdown>
<tr>
<th>Week</th><th>Date</th><th>Lecture</th><th>Date</th><th>Homework & Projects</th>
</tr>
<tr markdown>
<td>1</td><td>09/19</td><td>Course Overview & Introduction to C</td><td><time datetime="2023-09-24">09/24</time></td><td markdown>HW1 release</td>
</tr>
<tr>
<td>2</td><td>09/26</td><td>C Basics</td><td></td><td></td>
</tr>
<tr>
<td>3</td><td>10/03</td><td><strong>Holiday⛱️</strong></td><td>10/08</td><td>HW1 <strong>due</strong>, HW2 release</td>
</tr>
<tr markdown>
<td>4</td><td>10/10</td><td>C Memory</td><td></td><td></td>
</tr>
<tr>
<td>5</td><td>10/17</td><td>C Advanced</td><td>10/22</td><td>HW2 <strong>due</strong>, HW3 release</td>
</tr>
<tr markdown>
<td>6</td><td>10/24</td><td>Object-Oriented Programming & C++</td><td></td><td></td>
</tr>
<tr>
<td>7</td><td>10/31</td><td>Inheritance & Polymorphism</td><td>11/05</td><td>HW3 <strong>due</strong>, HW4 release</td>
</tr>
<tr markdown>
<td>8</td><td>11/07</td><td>STL & Modern C++</td><td></td><td></td>
</tr>
<tr markdown>
<td>9</td><td>11/07</td><td>C++ Design Patterns</td><td>11/19</td><td>HW4 <strong>due</strong>, P1 release</td>
</tr>
<tr markdown>
<td>10</td><td>11/14</td><td>Performance Fun!</td><td></td><td></td>
</tr>
<tr markdown>
<td><strong>13</strong></td><td></td><td></td><td>12/17</td><td>P1 <strong>due</strong>, P2 release</td>
</tr>
<tr markdown>
<td><strong>18</strong></td><td></td><td></td><td>01/21</td><td markdown>P2 <strong>due</strong></td>
</tr>
</tbody>
</table>

## About

This site would not have been possible without the effort from Prof. Huanchen Zhang, the TA team, the amazing open source projects:

* [MkDocs](https://www.mkdocs.org/) and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
* Clang/LLD in WebAssembly: [binji/wasm-clang](https://github.com/binji/wasm-clang)
* [Mathjax](https://www.mathjax.org/)
* [Asciinema](https://asciinema.org/)
* [Ace Editor](https://ace.c9.io/)

...and you! Submit bugs, thoughts, advice, to [the issue tracker](https://github.com/Yao-class-cpp-studio/wiki/issues).
Or even better, submit a pull request by clicking the edit:material-file-edit: button on the top right corner of each page.
