 var loadFunction = function(data) {
>>             if (data['error'] == true) {
>>                 PWM_MAIN.getObject('password').value = '';
>>                 PWM_MAIN.showErrorDialog(data,{
>>                     okAction:function(){
>>                         setTimeout(function(){
>>                             PWM_MAIN.getObject('password').focus();
>>                         },50);
>>                     }
>>                 });
>>                 return;
>>             }
>>             console.log('authentication success');
>>             var nextURL = data['data']['nextURL'];
>>             if (nextURL) {
>>                 PWM_MAIN.goto(nextURL, {noContext: true});
>>             }
>>         };
