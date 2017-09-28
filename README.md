# technology
Some common technical points encountered，Including app or web
正则：
1.正则匹配某一段文字
var str = '<div><head><span>i love you</span></head></div>',
        reg = /head(.+)head/g;
    console.log(str.replace(reg,'http://~www~bbb~com'));
2.输入框只能输入数字或者小数。
var value=input.replace(/[^\.\d]/g,'');
if(input.split('.').length>2){
    value=input.split('.')[0]+'.'+input.split('.')[1]
}
//判断手机号以及电话
if (user_phone!="" && !/^((\d{1,10}-\d{2,15})|(\d{1,20}))$/.test(user_phone)) {
			ui.toast('请填写收货人联系电话，20字内');
			return false;
		}
//判断手机号
 if (user_phone!="" && !/^(1[0-9][0-9]|14[0-9]|15[0-9]|17[0-9]|18[0-9])\d{8}$/i.test(user_phone) ) {
            ui.toast("您填写的手机号格式异常");
            return false;
        }	
 //车牌号首个字
  var platPro="京：津：沪：渝：冀：豫：云：辽：黑：湘：皖：闽：鲁：新：苏：浙：赣：鄂：桂：甘：晋：蒙：；陕：吉：贵：粤：青：藏：川：宁：琼；台；港；澳";
   "pattern":/^[A-Z0-9]{5}[A-Z0-9挂]{1}$/,//车牌号验证
     "pattern":/^[A-Za-z0-9]{5}[A-Za-z0-9挂]{1}$/,
  //整数或者保留两位小数
  if (debt!="" && !/^[0-9]+(\.[0-9]{2})?$/.test(debt) ) {
				$.ligerDialog.alert("请输入负债总额为整数或者保留两位小数","提示","warn");
				return false;
			}
	//整数或者保留两位小数		
if(this_val && !/^\d+(\.\d{1,2})?$/.test(this_val)){
            layer.msg("请输入的金额为整数或者保留两位小数！",{time:1500});
            _status_=false;
        };			 
//判断只输入中文。			   
if (user_name!="" && !/^[\u4e00-\u9fa5]{2,5}$/.test(user_name)) {
					$.ligerDialog.alert("输入的用户名应为2-5个中文字符","提示","warn");
					return false;
				}			   	
//身份证验证
if (idNum!="" && !/^(\d{15}$|^\d{18}$|^\d{17}(\d|X|x))$/.test(idNum) ) {
				$.ligerDialog.alert("证件号码不能为汉字和特殊符号","提示","warn");
				return false;
			}		
			
//输入正整数
if (cardNo!="" && !/0|(^[1-9]+\d*$)/.test(cardNo) ) {
				$.ligerDialog.alert("请输入代扣银行为非汉字或者非负数的值","提示","warn");
				return false;
			}	
			
//银行卡号输入限制
if (bankval!="" && !/^(\d{16}|\d{19})$/.test(bankval)) {
				ui.toast('请填写正确的银行卡号');
				return false;
			}	
			
//输入大于0的正整数！！！	
/^\+?[1-9]\d*$/		
//输入大于0的且可以为输入小数点
  if(thisVlue.length>3){
            if (thisVlue!="" && !/^([0-9]\d*(\.\d+))|([1-9]\d*)$/.test(thisVlue) ) {
                layer.msg("请输入大于0的数字",{
                    time: 1000 //20s后自动关闭
                });
                $(this).val("");
                return false;
            }
        }	
  //9或者18位字符      
         inputBlur("organizationCode",{
        "pattern":/^([0-9a-zA-Z]{9}$|^[0-9a-zA-Z]{18}$)/,
        "errormsg":"请输入组织机构代码9或者18位字符"
    })
 //姓名2~10个汉字
 
   "pattern":/^[\u4e00-\u9fa5]{2,10}$/,
   
 //身份证号18位数字或者17位数字+X
   "pattern":/^(^\d{18}$|^\d{17}(\d|X|x))$/,     
        					
 //输入特殊符号
  "pattern":/^[0-9a-zA-Z\u4e00-\u9fa5`~!@#\$%\^\&\*\(\)_\+<>\?:"\{\},\.\\\/;'\[\]]{1,50}$/,    
  //输入15位或者18位
  inputBlur("taxRegisterCode",{
        "pattern":/^([0-9a-zA-Z]{15}$|^[0-9a-zA-Z]{18}$)/,
        "errormsg":"请输入税务登记号15或者18位字符"
    })   					
