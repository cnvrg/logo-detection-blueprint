Use this batch blueprint to run in batch mode a pretrained tailored model with your custom data which detects logo elements in images and videos stored in a directory. To run this blueprint, provide the S3 Connector path to a directory folder containing videos and images.

This blueprint supports by default detection of the following logo classes: CCD, Steeden, and 76. To detect custom logos, the path to the weights file is required. Run this counterpart’s [training blueprint](https://metacloud.cloud.cnvrg.io/marketplace/blueprints/logo-detection-training), and then upload the trained model weights to the S3 Connector.

Click [here]() to view this blueprint's supported video and image formats.

Complete the following steps to run this logo-detector blueprint in batch mode:
1. Click **Use Blueprint** button. The cnvrg Blueprint Flow page displays.
2. Click the **S3 Connector** task to display its dialog.
   - Within the **Parameters** tab, provide the following Key-Value pair information:
     - Key: `bucketname` − Value: provide the data bucket name
     - Key: `prefix` – Value: provide the main to the data folder
   - Click the **Advanced** tab to change resources to run the blueprint, as required.
3. Click the **Batch** task to display its dialog.
   - Within the **Parameters** tab, provide the following Key-Value pair information:
     - Key: `source` – Value: provide the S3 location containing all the images and videos
     - `/input/s3_connector/logo_detection_batch` − ensure the path adheres to this format
     NOTE: You can use prebuilt example data paths provided.
   - Click the **Advanced** tab to change resources to run the blueprint, as required.
4. Click the **Run** button. The cnvrg software deploys a logo-detector model that detects logos and their locations in a batch of images.
5. Track the blueprint’s real-time progress in its Experiments page, which displays artifacts such as logs, metrics, hyperparameters, and algorithms.
6. Select **Batch > Experiments > Artifacts** and locate the output files.
7. Select a File Name, click the Menu icon, and select **Open File** to view an output image or video file.

A tailored model that detects logos, draws their boundaries, and labels them in images and videos has now been deployed in batch mode.

For detailed instructions on this blueprint's run, click [here](). To learn how this blueprint was created, click [here](https://github.com/cnvrg/logo-detection-blueprint).
