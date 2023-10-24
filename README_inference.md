Use this blueprint to immediately detect logo elements and their position in images. To use this pretrained logo detection model, create a ready-to-use API-endpoint that can be quickly integrated with your data and application.

This inference blueprint's model was trained using three logos: 76, Steeden, and Cafe Coffee Day. To use custom logo data according to your specific business, run this counterpart's [training blueprint](../logo-detection-blueprint/README.md), which trains the model and establishes an endpoint based on the newly trained model. If no logo training data is available and if text detection is needed, then the cnvrg team suggests the [Text Detection Inference] (https://metacloud.cloud.cnvrg.io/marketplace/blueprints/text-detection-inference) blueprint as an alternative.

Complete the following steps to deploy this logo-detector API endpoint:
1. Click the **Use Blueprint** button. The cnvrg Blueprint Flow page displays.
2.	In the dialog, select the relevant compute to deploy API endpoint and click the **Start** button.
3. The cnvrg software redirects to your endpoint. Complete one or both of the following options:
   * Use the Try it Live section with any logo image to check the model.
   * Use the bottom integration panel to integrate your API with your code by copying in your code snippet.
   
An API endpoint that detects logos in images has now been deployed.
