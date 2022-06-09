<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width,height=device-height,inital-scale=1.0,maximum-scale=1.0,user-scalable=no;">
	<meta name="apple-mobile-web-app-capable" content="yes">
	<meta name="apple-mobile-web-app-status-bar-style" content="black">
	<meta name="format-detection" content="telephone=no">
	<title>网络</title>
</head>
<h2>账号注册</h2>
<div>
<form action="" method="post">
<input  type="text" id="username" name="username"  value="" placeholder="请输入登陆账号" maxlength="30"><br><br>
<button type="submit" name="register" id="register" >点击注册
</button></font><br></a></form>
<?php
if(isset($_POST["register"])){
    $user=$_POST["username"];
    
    $manager = new MongoDB\Driver\Manager('mongodb://localhost:27017');
    $where = ['username'=>$user];
    $options = ['username'=>''];
    $query = new MongoDB\Driver\Query($where, $options);
    $cursor = $manager->executeQuery('grasscutter.accounts', $query);
    foreach($cursor as $doc){
        $UID=$doc->_id;
    }
    $where = ['_id'=>'Account'];
    $options = ['count'=>''];
    $query = new MongoDB\Driver\Query($where, $options);
    $cursor = $manager->executeQuery('grasscutter.counters', $query);
    foreach($cursor as $doc) {
        $Account=$doc->count;
    }
	if($user == ""){
		echo "<font size='4' color= '#00BFFF'><br>用户名和UID不能为空!<br>";
	}elseif($UID==""){
		$bulk = new MongoDB\Driver\BulkWrite;
	        $bulk->update(['_id'=>'Account'],['count'=>intval($Account)+1]);
	        $manager->executeBulkWrite('grasscutter.counters', $bulk); 
		$bulk = new MongoDB\Driver\BulkWrite;
		$bulk->insert(['_id'=>(string)(intval($Account)+1),'username'=>$user,'reservedPlayerId'=>intval('0'),'permissions'=>['0'=>''],'locale'=>'zh_CN']);
		$manager->executeBulkWrite('grasscutter.accounts', $bulk); 
		echo "<font size='4' color= '#00BFFF'><br>账号注册成功!<br>";
		echo "<font size='4' color= '#00BFFF'><br>注册的账号名为:".$user."<br>";
		echo "<font size='4' color= '#00BFFF'><br>注册的UID为:".(string)(intval($Account)+1)."<br>";
	    }else{
	        echo("<font size='4' color= '#00BFFF'><br>用户已经存在!");
        }
    }
?>

</div>
</body>

</html>
