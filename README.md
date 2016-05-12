# android-gogs-ui
UI for login and profile creation for Door43 gogs 

 How to Use:
 Start ProfileActivity for result
 Pass in a profile as a string extra with Profile.PROFILE_KEY. If no extra is provided, or the provided
 string throws a JSON exception, the profile is set to null.
 
 Providing a profile will check if the terms of use have been accepted. If yes, the activity will return
 with RESULT_OK and the serialized profile as an extra via Profile.PROFILE_KEY. If no, the terms of use
 activity will be called.
 
 Terms of Use can be checked using the static method: TermsOfUseActivity.termsAccepted(String)
 
 Returns:

 RESULT_OK: profile has accepted terms of use, profile included as extra via Profile.PROFILE_KEY
 RESULT_CANCELED: user backed out of the profile page
 
 TermsOfUseActivity.RESULT_BACKED_OUT_TOU: user backed out of Terms of Use activity. Profile included as extra, profile terms of use not accepted.
 
 TermsOfUseActivity.RESULT_DECLINED_TOU: user declined Terms of Use
