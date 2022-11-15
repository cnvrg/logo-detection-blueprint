Use this blueprint with your custom data to train a tailored model and deploy an endpoint that detects logos in images. Training a logo-detection algorithm requires data provided in the form of logo-containing images, the logo locations, and their labels.
To train this model with your data, provide the following two folders in the S3 Connector:
- Images − A folder with the images to train the model
- Labels − A folder with labels that correlate to the logos in the images folder

Complete the following steps to train this logo-detector model:
1. Click the **Use Blueprint** button. The cnvrg Blueprint Flow page displays.
2. In the flow, click the **S3 Connector** task to display its dialog.
   * Within the **Parameters** tab, provide the following Key-Value pair information:
     - **Key**: `bucketname` - **Value**: enter the data bucket name
     - **Key**: `prefix` - **Value**: provide the main path where the data folder is located
   * Click the **Advanced** tab to change resources to run the blueprints, as required.
3. Return to the flow and click the **Recreate** task to display its dialog.
   * Within the **Parameters** tab, provide the following Key-Value pair information:
     - **Key**: `images` – **Value**: provide the path to the images including the S3 prefix, with the following format: `/input/s3_connector/<prefix>/images`
     - **Key**: `labels` – **Value**: provide the path to the labels including the S3 prefix, with the following format: `/input/s3_connector/<prefix>/labels`
   NOTE: You can use prebuilt example data paths already provided.
   * Click the **Advanced** tab to change resources to run the blueprints, as required.
4. Click the **Retrain** task to display its dialog.
   * Within the **Parameters** tab, provide the following Key-Value pair information:
     - **Key**: `batch` – **Value**:  set the batch size the neural network ingests before calculating loss and readjusting weights
     - **Key**: `epochs` – **Value**: set the number of times the neural network trains the dataset
     - **Key**: `class_names` – **Value**: provide the names of the classes for the model to learn
   * Click the **Advanced** tab to change resources to run the blueprint, as required.
5.	Click the **Run** button. The cnvrg software launches the training blueprint as set of experiments, generating a trained logo detector model and deploying it as a new API endpoint.
6. Track the blueprint's real-time progress in its experiments page, which displays artifacts such as logs, metrics, hyperparameters, and algorithms.
7. Click the **Serving** tab in the project and locate your endpoint. Complete one or both of the following options:
   * Use the Try it Live section with any logo image to check the model.
   * Use the bottom Integration panel to integrate your API with your code by copying in your code snippet.
   
A custom model that can detect logos in images has now been trained and deployed. To learn how this blueprint was created, click [here](https://github.com/cnvrg/logo-detection-blueprint/).
