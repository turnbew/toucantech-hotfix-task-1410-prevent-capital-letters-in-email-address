FOR PRIVACY AND CODE PROTECTING REASONS THIS IS A SIMPLIFIED VERSION OF CHANGES AND NEW FEATURES

TASK DATE: 16.03.2018 - FINISHED: 16.03.2018

TASK'S LEVEL: (EASY)

TASK SHORT DESCRIPTION: [ Prevent/filter out/remove capital letters from being input into the email address field in the registration form]
				
GITHUB REPOSITORY CODE:hotfix/task-1410-prevent-capital-letters-in-email-address

CHANGES
 
	IN FILES: 
		
		register.js

			CHANGED CODE:
			
			
				FROM: if (confirm_email.val() !== register_email.val())) 
					
				TO: if (confirm_email.val().toLowerCase() !== register_email.val().toLowerCase()) 
					
					
					
		jquery.validate.min.js
		
			CHANGED CODE:
				
				Inside equalTo: function
			
					FROM: return a.==d.val()

					TO: return a.toLowerCase()==d.val().toLowerCase()
