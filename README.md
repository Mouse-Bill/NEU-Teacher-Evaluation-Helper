# NEU-Teacher-Evaluation-Helper
NEU教学质量监控与评估中心教学质量评价一键全优脚本  
在教评页面将如下代码复制到浏览器开发工具的控制台中，回车执行即可：
``` javascript
(async function() {
  for (let i = 2; i <= 11; i++) {
    let c = document.getElementById("evlTable").rows[i].cells[3];
    var button = c.querySelector('input[type="radio"]:first-child');
    button.click();
  }


  let s = document.getElementById("btn-saveResult");
  s.click();


  await new Promise(resolve => setTimeout(resolve, 1000));


  let submit_b = document.querySelector("body > div.sweet-alert.showSweetAlert.visible > div.sa-button-container > button.confirm");
  submit_b.click();
})();
```
