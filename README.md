# Mollie-C#-example
Creating a C# payment transaction with Mollie.com

 You can use plain JSON to talk to Mollie, please find the manual at: https://docs.mollie.com/reference/v2/payments-api/create-payment
 

 This ASP.Net C# WEB example form shows how to send a transaction to Mollie with plain JSON
 Copy these files to your Visual studio development environment and use the debugger to see what is happening by starting this one form.
 
 To Generate JSON you need to load the libraries from Newonsoft.Json in your Visual studio project. Find it in "Manage NuGet Packages" 
  (in Visual Studio 2015 right click on your solution name)

 Very importand is to TURN ON PAYMENT METHODS after you have created a Mollie account under Settings ==> Website Profiles:
 https://www.mollie.com/dashboard/settings/profiles   (Select payment methods) They do not need to be completed to test your interface.
 In Mollie you do not need to activate your account "Complete account" to run program tests


 Common error:
 The remote server returned an error: (401) Unauthorized.: Explanation: This means that you do not have valid credentials, e.g.  test_Mut7BGvad8dQu6mrGvgtpxk2UuGVtE is  not correct.

 Return message in JSON: Status: 422, title: Unprocessed entity. Detail:"Non-Existent body parameter \"first parameter name\" for 
 this API call. Explanation:
 This eror will happen if you did not specify a payment option in the mollie account settings.
 
 Error message: The remote server returned an error: (422) Unprocessable Entity.
 This happens if you use localhost in the webhookurl (PayRequest.webhookUrl = "https://localhost/)
