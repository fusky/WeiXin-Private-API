WeiXin-Private-API
==================

微信公用平台私有接口, 发送信息, 得到用户信息, 解析用户fakeId

用法参考test.php:

<pre>
<?php
require "config.php";
require "include/WeiXin.php";

$weiXin = new WeiXin($G_CONFIG['weiXin']);

// 发送消息
$testFakeId = "1477341522";
print_r($weiXin->send($testFakeId, "test"));

// 得到用户信息
print_r($weiXin->getUserInfo($testFakeId));

// 得到最新消息
print_r($weiXin->getLatestMsgs());	
</pre>