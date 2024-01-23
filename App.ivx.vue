<template>
  <ivx-stage _id="cejn4f1a3j500007f3ng" _name="前台" backgroundColor="#FFFFFF" :fonts="{}" height="100%" :pageCustomIdList="[null,null]" width="100%">
    <ivx-system _id="cejn4f1a3j500007f3n0" _name="应用系统"/>
    <ivx-page _id="cejn4gaa3j500007f3qg" _name="提交页" horizon="center">
      <ivx-input _id="cejn4mja3j500007f3r0" _name="输入框1" :marginTop="100" shadowType="box"/>
      <ivx-button _id="cejn4qja3j500007f3rg" _name="提交" bgColor="#0096FF" borderRadius="25px" :borderWidth="0" disabledBgColor="#97D4FF" fontColor="#FFFFFF" :fontSize="20" :marginTop="20" shadowType="box" text="提交" __events="cejn4qja3j500007f3rg,tap" @tap="cejn4qja3j500007f3rg_tap"/>
      <ivx-button _id="cpqpsf5a3j50000px7sg" _name="留言列表" text="留言列表" fontColor="#6D6565" :fontSize="20" :marginBottom="0" :marginTop="40" :borderWidth="1" bgColor="" __events="cpqpsf5a3j50000px7sg,tap" @tap="cpqpsf5a3j50000px7sg_tap"/>
    </ivx-page>
    <ivx-page _id="cpqpq7ca3j50000px7pg" _name="留言展示" horizon="center" @show="cpqpq7ca3j50000px7pg_show">
      <ivx-layoutrow _id="cpqpqeda3j50000px7q0" _name="返回" :verticalStretch="false" height="60px" bgColor="" vertical="center" :paddingLeft="20">
        <ivx-icon _id="cpqpqy7a3j50000px7qg" _name="左箭头" iconType="c11b584b4606a0f848853d9ce80c342e_270.svg" :width="30" :height="30" __events="cpqpqy7a3j50000px7qg,tap" @tap="cpqpqy7a3j50000px7qg_tap"/>
      </ivx-layoutrow>
      <ivx-text _id="cpqpr9ha3j50000px7r0" _name="留言展示" value="留言展示" :fontSize="22" fontColor="#1C1919" :textStyle="4" fontWeight="bold" fontStyle="" textDecoration=""/>
      <ivx-layoutcol _id="cpqprpja3j50000px7rg" _name="留言列表" :horizonStretch="false" width="300px" largeSize="300px" mediumSize="300px" smallSize="300px" padSize="300px" xsmallSize="300px" :verticalStretch="true" height="auto" bgColor="" horizon="center" :marginTop="20">
        <data-for _id="cpqpv7ma3j50000px7zg" _name="循环创建1" :value="$var.cpqpt8sa3j50000px7t0.value" :useKey="true">
          <ivx-text _id="cpqps5ca3j50000px7s0" _name="文本1" :value="$item.cpqpv7ma3j50000px7zg['留言']" fontColor="#615555" :fontSize="18" :marginBottom="12"/>
        </data-for>
      </ivx-layoutcol>
      <data-obj-arr _id="cpqpt8sa3j50000px7t0" _name="留言列表" :value="cpqpt8sa3j50000px7t0_value" :headers="[{&quot;type&quot;:&quot;number&quot;,&quot;title&quot;:&quot;数据ID&quot;,&quot;name&quot;:&quot;_id&quot;},{&quot;type&quot;:&quot;string&quot;,&quot;title&quot;:&quot;留言&quot;,&quot;name&quot;:&quot;留言&quot;},{&quot;type&quot;:&quot;string&quot;,&quot;title&quot;:&quot;提交用户&quot;,&quot;name&quot;:&quot;_user&quot;},{&quot;type&quot;:&quot;string&quot;,&quot;title&quot;:&quot;创建时间&quot;,&quot;name&quot;:&quot;_create&quot;},{&quot;type&quot;:&quot;string&quot;,&quot;title&quot;:&quot;更新时间&quot;,&quot;name&quot;:&quot;_update&quot;}]" mark="new" :structureName="{&quot;dbName&quot;:&quot;留言库&quot;,&quot;subName&quot;:&quot;all&quot;,&quot;bid&quot;:&quot;cejn4z3a3j500007f3s0&quot;}" name="留言列表"/>
    </ivx-page>
  </ivx-stage>
</template>

<script>
var cpqpt8sa3j50000px7t0_value = []

function cejn4qja3j500007f3rg_tap() {
$func.cejn4z3a3j500007f3s0.dbInsert_stage(['留言'],[($var.cejn4mja3j500007f3r0.value)],undefined);
}

function cpqpsf5a3j50000px7sg_tap() {
$func.cejn4f1a3j500007f3ng.gotoPage('cpqpq7ca3j50000px7pg',undefined);
}

function cpqpq7ca3j50000px7pg_show() {
$func.cejn4z3a3j500007f3s0.dbSelect_stage(undefined,undefined,undefined,undefined,function(cbStatus, cbParams) {$asyncStart; if(true){$func.cpqpt8sa3j50000px7t0.setValue(($util.getSelf($util.db_getDataObjLocArr(cbParams))));} ;$asyncEnd}.bind(this));
}

function cpqpqy7a3j50000px7qg_tap() {
$func.cejn4f1a3j500007f3ng.gotoPage('cejn4gaa3j500007f3qg',undefined);
}
</script>
