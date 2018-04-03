# mip-linktion-fortune-consults

mip-linktion-fortune-consults ajax移动端弹框提交表单，pc端下滑卡片

标题|内容
----|----
类型|通用
支持布局|responsive,fixed-height,fill,container,fixed
所需脚本|https://c.mipcdn.com/static/v1/mip-linktion-fortune-consults/mip-linktion-fortune-consults.js<br>https://c.mipcdn.com/static/v1/mip-lightbox/mip-lightbox.js<br>https://c.mipcdn.com/static/v1/mip-vd-tabs/mip-vd-tabs.js

## 示例
```html
<mip-linktion-fortune-consults>
    <div class="col-lg-4 col-xs-12 col-sm-4">
    <div class="person-card consult-box" data-plannerid="1" data-productid="2" data-consulturl="http://47.100.7.250:8080/product/consult">
      <div class="click-lightbox slide-up">
        <button type="button" class="click-hidden">&times;</button>
        <h3>咨询TA</h3>
        <p class="consult-describe">请留下您的信息，方便这位理财师联系您。</p>
        <form class="consult-form pc-form">
          <div class="form-group-input">
            <label>姓名</label>
            <input type="text" name="name" placeholder="请输入姓名" required="required">
          </div>
          <div class="form-group-input">
            <label>手机</label>
            <input type="number" name="phone" placeholder="请输入手机号" required="required">
          </div>
          <h4 class="checkbox-head">首选联系时间</h4>
          <div class="checkbox-flex">
            <div class="form-group-checkbox">
              <input type="radio" name="times" id="times-am" value="1" required="required">
              <label for="times-am">白天</label>
            </div>
            <div class="form-group-checkbox">
              <input type="radio" name="times" id="times-pm" value="2" required="required">
              <label for="times-pm">晚间</label>
            </div>
            <div class="form-group-checkbox">
              <input type="radio" name="times" id="anytimes" value="3" required="required">
              <label for="anytimes">任何时刻</label>
            </div>
          </div>
          <button type="button" class="but-submit consult-submit">提交</button>
        </form>
      </div>
      <div class="recommend-icon">
        <mip-img src=""></mip-img>
      </div>
      <div class="card-box">
        <div class="person-icon">
          <mip-img src=""></mip-img>
        </div>
        <div class="info-text">
          <div class="text-name">
            <p class="person-name">王琨越</p>
            <p class="person-info">咨询顾问</p>
          </div>
          <div class="info-label">
            <p class="txt-major">专业领域</p>
            <p class="card-label">重疾险重</p>
            <p class="card-label">意外险</p>
            <p class="card-label">少儿险</p>
            <p class="card-label">重疾险</p>
          </div>
        </div>
        <div class="person-info-txt">
          <p>推荐理财师的范围均为购买了此营销视频的理财师；若，15天内，此理财师已经</p>
        </div>
      </div>
      <div class="card-but">
        <a href="javascript:;" class="but-about">了解TA</a>
        <!-- <a class="but-advisory " href="javascript:return false;" onclick="return false;">咨询中</a> -->
        <!-- 这部分是咨询TA按钮，分不同的状态。把ID改成modal-consult是登录后的弹框，现在是未登录的咨询TA弹框-->
        <a class="but-advisory" on="tap:modal-consult-visitor.toggle" id="btn-open" role="button" tabindex="0">咨询TA</a>
      </div>
      <div class="card-phone-but">
        <a href="javascript:;" class="but-about" on="tap:modal-consult.toggle" id="btn-open" role="button" tabindex="0">咨询TA</a>
        <!-- 未登录用户的咨询TA弹框 -->
        <!-- <a href=javascript:;"" class="but-about" on="tap:modal-consult-visitor.toggle" id="btn-open" role="button" tabindex="0">咨询TA</a> -->
        <a href="javascript:;" on="tap:planner-more.toggle" id="btn-open" role="button" tabindex="0"  class="but-advisory">换一位理财师</a>
      </div>
    </div>
  </div>
  <mip-lightbox id="modal-consult" layout="nodisplay" class="mip-hidden">
    <div class="modal-dialog modal-consult modal-blue-top" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <p>咨询TA</p>
          <button type="button" class="close" on="tap:modal-consult.toggle">&times;</button>
        </div>
        <div class="modal-body click-lightbox-phone clearfix consult-box" data-plannerid="3" data-productid="4" data-consulturl="http://47.100.7.250:8080/product/consult">
          <p class="consult-describe">请留下您的信息，方便这位理财师联系您。</p>
          <form class="consult-form phone-form">
            <div class="form-group-input">
              <label>姓名</label>
              <input type="text" name="name" placeholder="请输入姓名" required="required">
            </div>
            <div class="form-group-input">
              <label>手机</label>
              <input type="number" name="phone" placeholder="请输入手机号" required="required">
            </div>
            <h4 class="checkbox-head">首选联系时间</h4>
            <div class="checkbox-flex">
              <div class="form-group-checkbox">
                <input type="radio" name="times" id="am" required="required" value="1">
                <label for="am">白天</label>
              </div>
              <div class="form-group-checkbox">
                <input type="radio" name="times" id="pm" required="required" value="2">
                <label for="pm">晚间</label>
              </div>
              <div class="form-group-checkbox">
                <input type="radio" name="times" id="anytime" required="required" value="3">
                <label for="anytime">任何时刻</label>
              </div>
            </div>
            <button type="button" class="but-submit consult-submit">提交</button>
          </form>
        </div>
      </div>
    </div>
  </mip-lightbox>
</mip-linktion-fortune-consults>
```