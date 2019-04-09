# mpesa-library
Mpesa Api library 

#usage
     $mpesa  = new Mpesa();
     
 # access_token
 
     echo " Token : " .$mpesa->oauth_token();  
     Token : zlfUeamewm24r2NjnsgjBlQQANNP
    
 # STKPushQuery
     
     print_r($mpesa->STKPushQuery('ws_CO_DMZ_297481201_09042019174418021'));        
     //result
     { "ResponseCode": "0", 
       "ResponseDescription":"The service request has been accepted successsfully", 
      "MerchantRequestID":"28415-165347-1",
      "CheckoutRequestID":"ws_CO_DMZ_297481201_09042019174418021",
      "ResultCode": "1032", 
      "ResultDesc":"[STK_CB - ]Request cancelled by user" 
      }
  # STKPushSimulation
  
      print_r($mpesa->STKPushSimulation('20','254708374149','pay now','test'));
      //result
      { 
     "MerchantRequestID":"16658-1455367-1", 
     "CheckoutRequestID":"ws_CO_DMZ_435322918_09042019180550656", 
     "ResponseCode": "0",        
     "ResponseDescription":"Success. Request accepted for processing", 
     "CustomerMessage":"Success. Request accepted for processing"
     }
     
  # register url
     print_r( $mpesa->register_url());   
     
  # c2b
     print_r($mpesa->c2b('120','254708374149','account'));
     
  # b2c
     print_r($mpesa->b2c('20','BusinessPayment','254708374149','payment'));
     
  #  b2b
     print_r($mpesa->b2b('10000','BusinessPayBill','60000','4','4','paytest','cool'));
     
  # accountbalance
     print_r($mpesa->accountbalance('600443','4','remarks'));
     
  # reversal
     print_r( $mpesa->reversal('2','254708374149','1','NCR7S1UXBT','PAY NOW VIA WASKSOFT'));
     
  # transaction status
     print_r($mpesa->transaction_status('NCR7S1UXBT','254708374149','4','apitest'));
  
# installation  

