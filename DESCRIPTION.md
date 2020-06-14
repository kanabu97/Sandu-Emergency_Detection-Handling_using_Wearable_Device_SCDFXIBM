# Emergency Detection and Handling using Wearable Device 

## Idea specification
* 1. Wearable device constantly checking user's heart rate.
* 2. Healthy heart rate of the user are stored beforehands to be used for heart rate abnormality detection. 
* 3. In the event where abnormal heart rate lasts for more than 3 minutes or fall is detected, user will be prompted a message to ask if they need help. Only one 'click' is needed to get help. 
* 4. If help is needed or no reponse from the user, a message is sent to SCDF immediately.
* 5. In the event where abnormal heart rate is too far away from range, SCDF will be informed directly.
* 6. Nobody except the user can access the user details unless emergency happens.
* 7. It should not overload the emergency hotline unnecessarily.

## Built Node Red Application Explaination
1. Since there is no hardware provided, simulation inputs is used in the application. The inputs are in the following format:
   {Activity:"", HRValue:""}
2. Dashboard is can be used as the demo of the screen that will be show on wearable device.
3. Node red is built on local phone drive to ensure all the user datas are saved in user's local drive unless when emergency happens. Hence, users' privacy is protected.
4. Healthy heart rate sample is computed based on data. Thus it is more accurate as different people might have different heart rate range.
5. Actual SMS can be sent using node-red, however it is not implemented because top-up is needed for an Nexmo number.

## Further Developments
1. This function can be pushed out to everyone, not just the aging population.
2. More activity modes such as sleeping can be computed for more accurate emergency detection.
3. Can include more descriptions in the SMS so that more precise aid can be given.
4. Machine learning can be deployed for heart rate data analysis when chip technology advances, i.e. when mobile phone chip become more powerful.

## Conclusion
The most important feature of emergency response is simple and direct. That's the reason why our idea focuses on the simplicity of the user interface with one 'click' to save your life feature. Although solution proposed is not complete, we do believe that if this feature is successfully implemented, a more efficiet emergency response system can be built, and more lives can be saved.
