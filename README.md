# 1_yunosPay


產生訂單

<script type="text/javascript">

pay("20160322","01","title","1","http://xxx.xxx.xxx/xxx.php");
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
  		function(mag){alert(mag);},
  		function(err){}
  	);
  }
  
</script>

  
  
```取得裝置ID
	YunosPay.iandroid(
	  true, 
	  function(mag){ 
	  	console.log("device ID: " + mag);
	  },
	  function(err){}
	);		
			
```			

```
	YunosPay.change(true);
```
