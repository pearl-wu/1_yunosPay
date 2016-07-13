# yunosPay

##產生訂單
```javascript
<script type="text/javascript">
	pay("20160322","01","title name","1","http://xxx.xxx.xxx/xxx.php");  
	  //訂單編號//商品ID//商品名稱//商品價格(單位:分錢)//應用開發者回傳通知url
	   
	    
	  function pay(P_no,S_id,S_name,pri,P_url){
	  	YunosPay.pay(
	  		{
	  		      //訂單編號//商品ID//商品名稱//商品價格(單位:分錢)//應用開發者回傳通知url
	  			partner_order_no:P_no,
	  			subject_id:S_id,				
	  			subject:S_name,					
	  			price:pri,     						
	  			partner_notify_url:P_url		
	  		},
	  		//回傳訊息
	  		function(mag){alert(mag);}
	  	);
	  }
</script>
```

##取得裝置ID
```javascript
<script type="text/javascript">
	YunosPay.iandroid(
	  true, 
	  function(mag){ 
	  	console.log("device ID: " + mag);
	  }
	);		
</script>			
```
## APP package ID & version
```javascript
	<script type="text/javascript">
		YunosPay.packageinfo(
		1,	// 1:package ID ; 2:package version
		function(mag){
			console.log("device ID: " + mag);	
		}
		);
	</script>
```
## Sign
```javascript
	<script type="text/javascript">
	YunosPay.sign(
		"MAG",
		function(mag){
			alert(mag);
		}			
	);
	</script>
```

## Echo
```javascript
	<script type="text/javascript">
	YunosPay.echo("context",0);  // 0:約5秒 1:約9秒
	</script> 
```
