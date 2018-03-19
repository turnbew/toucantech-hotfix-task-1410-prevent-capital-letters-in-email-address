TASK DATE (EASY): 16.03.2018 - FINISHED: 16.03.2018


TASK SHORT DESCRIPTION: 1412 [
								Prevent/filter out/remove capital letters from being input into the email address 
								field in the registration form
							]

GITHUB REPOSITORY CODE: hotfix/task-1410-prevent-capital-letters-in-email-address


ORIGINAL WORK: https://github.com/BusinessBecause/network-site/tree/hotfix/task-1410-prevent-capital-letters-in-email-address


CHANGES
 
	IN FILES: 
		
		\network-site\addons\default\modules\bbusers\js\register.js

			CHANGED CODE:
			
			
				FROM: if (confirm_email.val() !== register_email.val())) 
					
				TO: if (confirm_email.val().toLowerCase() !== register_email.val().toLowerCase()) 
					
					
					
		\network-site\assets\jquery-validate\jquery.validate.min.js
		
			CHANGED CODE:
				
				Inside equalTo: function
			
					FROM: return a.==d.val()

					TO: return a.toLowerCase()==d.val().toLowerCase()
