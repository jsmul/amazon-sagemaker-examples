![SageMaker](https://github.com/aws/amazon-sagemaker-examples/raw/main/_static/sagemaker-banner.png)

# Amazon SageMaker Examples

Example Jupyter notebooks that demonstrate how to build, train, and deploy machine learning models using Amazon SageMaker.

## :books: Read this before you proceed further

Amazon SageMaker examples are divided in two repositories:

- [SageMaker example notebooks](https://github.com/aws/amazon-sagemaker-examples) is the official repository, containing examples that demonstrate the usage of Amazon SageMaker. This repository is entirely focussed on covering the breadth of features provided by SageMaker, and is maintained directly by Amazon SageMaker team.

- [Sagemaker Example Community repository](https://github.com/aws/amazon-sagemaker-examples-community) is another SageMaker repository which contains additional examples and reference solutions, beyond the examples showcased in the [official repository](https://github.com/aws/amazon-sagemaker-examples). This repository is maintained by community of engineers and solution architects at AWS.

## Planning to submit a PR to this repository? Read this first:

- This repository will only accept notebooks/examples which demonstrate a feature of SageMaker, not yet covered anywhere in this repository. PR submitters are requested to check this before submitting the PR to avoid getting it rejected.

- If you still would like to contribute your example, please submit a PR to [Sagemaker Example Community repository](https://github.com/aws/amazon-sagemaker-examples-community) instead.

## :hammer_and_wrench: Setup

The quickest setup to run example notebooks includes:

- An [AWS Account](http://docs.aws.amazon.com/sagemaker/latest/dg/gs-account.html)
- Proper [IAM User and Role](http://docs.aws.amazon.com/sagemaker/latest/dg/authentication-and-access-control.html) setup
- An [Amazon SageMaker Notebook Instance](http://docs.aws.amazon.com/sagemaker/latest/dg/gs-setup-working-env.html)
- An [S3 bucket](http://docs.aws.amazon.com/sagemaker/latest/dg/gs-config-permissions.html)

## :computer: Usage

These example notebooks are automatically loaded into SageMaker Notebook Instances.
They can be accessed by clicking on the `SageMaker Examples` tab in Jupyter or the SageMaker logo in JupyterLab.

Although most examples utilize key Amazon SageMaker functionality like distributed, managed training or real-time hosted endpoints, these notebooks can be run outside of Amazon SageMaker Notebook Instances with minimal modification (updating IAM role definition and installing the necessary libraries).

As of February 7, 2022, the default branch is named "main". See our [announcement](https://github.com/aws/amazon-sagemaker-examples/discussions/3131) for details and how to update your existing clone.

## :notebook: Examples

### Introduction to geospatial capabilities

These examples introduce SageMaker geospatial capabilities which makes it easy to build, train, and deploy ML models using geospatial data.

- [How to use SageMaker Processing with geospatial image](sagemaker-geospatial/processing-geospatial-ndvi/geospatial-processing-ndvi-intro.ipynb) shows how to compute the normalized difference vegetation index (NDVI) which indicates health and density of vegetation using SageMaker Processing and satellite imagery
- [Monitoring Lake Drought with SageMaker Geospatial Capabilities](sagemaker-geospatial/lake-mead-drought-monitoring) shows how to monitor Lake Mead drought using SageMaker geospatial capabilities.
- [Digital Farming with Amazon SageMaker Geospatial Capabilities](sagemaker-geospatial/digital-farming-pipelines) shows how geospatial capabilities can help accelerating, optimizing, and easing the processing of the geospatial data for the Digital Farming use cases.
- [Assess wildfire damage with Amazon SageMaker Geospatial Capabilities](sagemaker-geospatial/dixie-wildfire-damage-assessment/dixie-wildfire-damage-assessment.ipynb) demonstrates how Amazon SageMaker geospatial capabilities can be used to identify and assess vegetation loss caused by the Dixie wildfire in Northern California.
- [Monitoring Glacier Melting with SageMaker Geospatial Capabilities](sagemaker-geospatial/mount-shasta-glacier-melting-monitoring) shows how to monitor glacier melting at Mount Shasta using SageMaker geospatial capabilities.
- [Monitoring of methane (CH4) emission point sources using Amazon SageMaker Geospatial Capabilities](sagemaker-geospatial/methane-emission-monitoring/monitor_methane_ch4_emission_point_sources.ipynb) demonstrates how methane emissions can be detected by using open data Satellite imagery (Sentinel-2).
- [How to use Vector Enrichment Jobs for Map Matching](sagemaker-geospatial/vector-enrichment-map-matching/vector-enrichment-map-matching.ipynb) shows how to use vector enrichtment operations with Amazon SageMaker Geospatial capabilities to snap GPS coordinates to road segments.
- [How to use Vector Enrichment Jobs for Reverse Geocoding](sagemaker-geospatial/vector-enrichment-reverse-geocoding/vector-enrichment-reverse-geocoding.ipynb) shows how to use Amazon SageMaker Geospatial capabilities for reverse geocoding to obtain human readable addresses from data with latitude/longitude information.

### Introduction to Ground Truth Labeling Jobs

These examples provide quick walkthroughs to get you up and running with the labeling job workflow for Amazon SageMaker Ground Truth.

- [Bring your own model for SageMaker labeling workflows with active learning](ground_truth_labeling_jobs/bring_your_own_model_for_sagemaker_labeling_workflows_with_active_learning) is an end-to-end example that shows how to bring your custom training, inference logic and active learning to the Amazon SageMaker ecosystem.
- [From Unlabeled Data to a Deployed Machine Learning Model: A SageMaker Ground Truth Demonstration for Image Classification](ground_truth_labeling_jobs/from_unlabeled_data_to_deployed_machine_learning_model_ground_truth_demo_image_classification) is an end-to-end example that starts with an unlabeled dataset, labels it using the Ground Truth API, analyzes the results, trains an image classification neural net using the annotated dataset, and finally uses the trained model to perform batch and online inference.
- [Ground Truth Object Detection Tutorial](ground_truth_labeling_jobs/ground_truth_object_detection_tutorial) is a similar end-to-end example but for an object detection task.
- [Basic Data Analysis of an Image Classification Output Manifest](ground_truth_labeling_jobs/data_analysis_of_ground_truth_image_classification_output) presents charts to visualize the number of annotations for each class, differentiating between human annotations and automatic labels (if your job used auto-labeling). It also displays sample images in each class, and creates a pdf which concisely displays the full results.
- [Training a Machine Learning Model Using an Output Manifest](ground_truth_labeling_jobs/object_detection_augmented_manifest_training) introduces the concept of an "augmented manifest" and demonstrates that the output file of a labeling job can be immediately used as the input file to train a SageMaker machine learning model.
- [Annotation Consolidation](ground_truth_labeling_jobs/annotation_consolidation) demonstrates Amazon SageMaker Ground Truth annotation consolidation techniques for image classification for a completed labeling job.

### Introduction to Applying Machine Learning

These examples provide a gentle introduction to machine learning concepts as they are applied in practical use cases across a variety of sectors.

- [Predicting Customer Churn](introduction_to_applying_machine_learning/xgboost_customer_churn) uses customer interaction and service usage data to find those most likely to churn, and then walks through the cost/benefit trade-offs of providing retention incentives. This uses Amazon SageMaker's implementation of [XGBoost](https://github.com/dmlc/xgboost) to create a highly predictive model.
- [Ensembling](introduction_to_applying_machine_learning/ensemble_modeling) predicts income using two Amazon SageMaker models to show the advantages in ensembling.
- [MXNet Gluon Recommender System](introduction_to_applying_machine_learning/gluon_recommender_system) uses neural network embeddings for non-linear matrix factorization to predict user movie ratings on Amazon digital reviews.
- [Population Segmentation of US Census Data using PCA and Kmeans](introduction_to_applying_machine_learning/US-census_population_segmentation_PCA_Kmeans) analyzes US census data and reduces dimensionality using PCA then clusters US counties using KMeans to identify segments of similar counties.
- [Traffic violations forecasting using DeepAR](introduction_to_applying_machine_learning/deepar_chicago_traffic_violations) is an example to use daily traffic violation data to predict pattern and seasonality to use Amazon DeepAR alogorithm.
- [Visual Inspection Automation with Pre-trained Amazon SageMaker Models](introduction_to_applying_machine_learning/visual_object_detection) is an example for fine-tuning pre-trained Amazon Sagemaker models on a target dataset.
- [Create SageMaker Models Using the PyTorch Model Zoo](introduction_to_applying_machine_learning/sagemaker_pytorch_model_zoo) contains an example notebook to create a SageMaker model leveraging the PyTorch Model Zoo and visualize the results.
- [Deep Demand Forecasting](introduction_to_applying_machine_learning/deep_demand_forecasting) provides an end-to-end solution for Demand Forecasting task using three state-of-the-art time series algorithms LSTNet, Prophet, and SageMaker DeepAR, which are available in GluonTS and Amazon SageMaker.
- [Fraud Detection Using Graph Neural Networks](introduction_to_applying_machine_learning/fraud_detection_using_graph_neural_networks) is an example to identify fraudulent transactions from transaction and user identity datasets.
- [Identify key insights from textual document](introduction_to_applying_machine_learning/identify_key_insights_from_textual_document) contains comphrensive notebooks for five natural language processing tasks Document Summarization, Text Classification, Question and Answering, Name Entity Recognition, and Semantic Relation Extracion.
- [Credit Card Fraud Detector](introduction_to_applying_machine_learning/credit_card_fraud_detector) is an example of the core of a credit card fraud detection system using SageMaker with Random Cut Forest and XGBoost.
- [Churn Prediction Multimodality of Text and Tabular](introduction_to_applying_machine_learning/churn_prediction_multimodality_of_text_and_tabular) is an example notebook to train and deploy a churn prediction model that uses state-of-the-art natural language processing model to find useful signals in text. In addition to textual inputs, this model uses traditional structured data inputs such as numerical and categorical fields.

### SageMaker Automatic Model Tuning

These examples introduce SageMaker's hyperparameter tuning functionality which helps deliver the best possible predictions by running a large number of training jobs to determine which hyperparameter values are the most impactful.

- [TensorFlow Tuning](hyperparameter_tuning/tensorflow2_mnist) shows how to use SageMaker hyperparameter tuning with the pre-built TensorFlow container and MNIST dataset.
- [HuggingFace Tuning](hyperparameter_tuning/huggingface_multiclass_text_classification_20_newsgroups) shows how to use SageMaker hyperparameter tuning with the pre-built HuggingFace container and 20_newsgroups dataset.
- [Keras BYO Tuning](hyperparameter_tuning/keras_bring_your_own) shows how to use SageMaker hyperparameter tuning with a custom container running a Keras convolutional network on CIFAR-10 data.
- [Analyzing Results](hyperparameter_tuning/analyze_results) is a shared notebook that can be used after each of the above notebooks to provide analysis on how training jobs with different hyperparameters performed.
- [Model tuning for distributed training](hyperparameter_tuning/model_tuning_for_distributed_training) shows how to use SageMaker hyperparameter tuning with Hyperband strategy for optimizing model in distributed training.
- [Neural Architecture Search for Large Language Models](hyperparameter_tuning/neural_architecture_search_llm) shows how to prune fine-tuned large language models via neural architecture search.

### SageMaker Autopilot

These examples introduce SageMaker Autopilot. Autopilot automatically performs feature engineering, model selection, model tuning (hyperparameter optimization) and allows you to directly deploy the best model to an endpoint to serve inference requests.

- [Customer Churn AutoML](autopilot/) shows how to use SageMaker Autopilot to automatically train a model for the [Predicting Customer Churn](introduction_to_applying_machine_learning/xgboost_customer_churn) task.
- [Targeted Direct Marketing AutoML](autopilot/) shows how to use SageMaker Autopilot to automatically train a model.
- [Housing Prices AutoML](autopilot/autopilot_california_housing) shows how to use SageMaker Autopilot for a linear regression problem (predict housing prices).
- [Portfolio Churn Prediction with Amazon SageMaker Autopilot and Neo4j](autopilot/sagemaker_autopilot_neo4j_portfolio_churn.ipynb) shows how to use SageMaker Autopilot with graph embeddings to predict investment portfolio churn.
- [Move Amazon SageMaker Autopilot ML models from experimentation to production using Amazon SageMaker Pipelines](autopilot/sagemaker-autopilot-pipelines) shows how to use SageMaker Autopilot in combination with SageMaker Pipelines for end-to-end AutoML training automation.
- [Amazon SageMaker Autopilot models to serverless endpoints](autopilot/autopilot-serverless-inference) shows how to deploy Autopilot generated models to serverless endpoints.

### Introduction to Amazon Algorithms

These examples provide quick walkthroughs to get you up and running with Amazon SageMaker's custom developed algorithms. Most of these algorithms can train on distributed hardware, scale incredibly well, and are faster and cheaper than popular alternatives.

- [k-means](sagemaker-python-sdk/1P_kmeans_highlevel) is our introductory example for Amazon SageMaker. It walks through the process of clustering MNIST images of handwritten digits using Amazon SageMaker k-means.
- [Factorization Machines](introduction_to_amazon_algorithms/factorization_machines_mnist) showcases Amazon SageMaker's implementation of the algorithm to predict whether a handwritten digit from the MNIST dataset is a 0 or not using a binary classifier.
- [Latent Dirichlet Allocation (LDA)](introduction_to_amazon_algorithms/lda_topic_modeling) introduces topic modeling using Amazon SageMaker Latent Dirichlet Allocation (LDA) on a synthetic dataset.
- [Linear Learner](introduction_to_amazon_algorithms/linear_learner_mnist) predicts whether a handwritten digit from the MNIST dataset is a 0 or not using a binary classifier from Amazon SageMaker Linear Learner.
- [Neural Topic Model (NTM)](introduction_to_amazon_algorithms/ntm_synthetic) uses Amazon SageMaker Neural Topic Model (NTM) to uncover topics in documents from a synthetic data source, where topic distributions are known.
- [Principal Components Analysis (PCA)](introduction_to_amazon_algorithms/pca_mnist) uses Amazon SageMaker PCA to calculate eigendigits from MNIST.
- [Seq2Seq](introduction_to_amazon_algorithms/seq2seq_translation_en-de) uses the Amazon SageMaker Seq2Seq algorithm that's built on top of [Sockeye](https://github.com/awslabs/sockeye), which is a sequence-to-sequence framework for Neural Machine Translation based on MXNet. Seq2Seq implements state-of-the-art encoder-decoder architectures which can also be used for tasks like Abstractive Summarization in addition to Machine Translation. This notebook shows translation from English to German text.
- [XGBoost for regression](introduction_to_amazon_algorithms/xgboost_abalone) predicts the age of abalone ([Abalone dataset](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/regression.html)) using regression from Amazon SageMaker's implementation of [XGBoost](https://github.com/dmlc/xgboost).
- [XGBoost for multi-class classification](introduction_to_amazon_algorithms/xgboost_mnist) uses Amazon SageMaker's implementation of [XGBoost](https://github.com/dmlc/xgboost) to classify handwritten digits from the MNIST dataset as one of the ten digits using a multi-class classifier. Both single machine and distributed use-cases are presented.
- [BlazingText Word2Vec](introduction_to_amazon_algorithms/blazingtext_word2vec_text8) generates Word2Vec embeddings from a cleaned text dump of Wikipedia articles using SageMaker's fast and scalable BlazingText implementation.
- [Object detection for bird images](introduction_to_amazon_algorithms/object_detection_birds) demonstrates how to use the Amazon SageMaker Object Detection algorithm with a public dataset of Bird images.
- [Object2Vec for sentence similarity](introduction_to_amazon_algorithms/object2vec_sentence_similarity) explains how to train Object2Vec using sequence pairs as input using sentence similarity analysis as the application.
- [IP Insights for suspicious logins](introduction_to_amazon_algorithms/ipinsights_login) shows how to train IP Insights on a login events for a web server to identify suspicious login attempts.
- [Semantic Segmentation](introduction_to_amazon_algorithms/semantic_segmentation_pascalvoc) shows how to train a semantic segmentation algorithm using the Amazon SageMaker Semantic Segmentation algorithm. It also demonstrates how to host the model and produce segmentation masks and probability of segmentation.
- [JumpStart Instance Segmentation](introduction_to_amazon_algorithms/jumpstart_instance_segmentation) demonstrates how to use a pre-trained Instance Segmentation model available in JumpStart for inference.
- [JumpStart Semantic Segmentation](introduction_to_amazon_algorithms/jumpstart_semantic_segmentation) demonstrates how to use a pre-trained Semantic Segmentation model available in JumpStart for inference, how to finetune the pre-trained model on a custom dataset using JumpStart transfer learning algorithm, and how to use fine-tuned model for inference.
- [JumpStart Text Generation](introduction_to_amazon_algorithms/jumpstart_text_generation) shows how to use JumpStart to generate text that appears indistinguishable from the hand-written text.
- [JumpStart Text Summarization](introduction_to_amazon_algorithms/jumpstart_text_summarization) shows how to use JumpStart to summarize the text to contain only the important information.
- [JumpStart Image Embedding](introduction_to_amazon_algorithms/jumpstart_image_embedding) demonstrates how to use a pre-trained model available in JumpStart for image embedding.
- [JumpStart Text Embedding](introduction_to_amazon_algorithms/jumpstart_text_embedding) demonstrates how to use a pre-trained model available in JumpStart for text embedding.
- [JumpStart Object Detection](introduction_to_amazon_algorithms/jumpstart_object_detection) demonstrates how to use a pre-trained Object Detection model available in JumpStart for inference, how to finetune the pre-trained model on a custom dataset using JumpStart transfer learning algorithm, and how to use fine-tuned model for inference.
- [JumpStart Machine Translation](introduction_to_amazon_algorithms/jumpstart_machine_translation) demonstrates how to translate text from one language to another language in JumpStart.
- [JumpStart Named Entity Recognition](introduction_to_amazon_algorithms/jumpstart_named_entity_recognition) demonstrates how to identify named entities such as names, locations etc. in the text in JumpStart.
- [JumpStart Text to Image](introduction_to_amazon_algorithms/jumpstart_text_to_image) demonstrates how to generate image conditioned on text in JumpStart.
- [JumpStart Upscaling](introduction_to_amazon_algorithms/jumpstart_upscaling) demonstrates how to enhance image quality with Stable Diffusion models in JumpStart.
- [JumpStart Inpainting](introduction_to_amazon_algorithms/jumpstart_inpainting) demonstrates how to inpaint an image with Stable Diffusion models in JumpStart.
- [In-context learning with AlexaTM 20B](introduction_to_amazon_algorithms/jumpstart_alexatm20b) demonstrates how to use AlexaTM 20B for in-context-learning in JumpStart.

### Amazon SageMaker RL

The following provide examples demonstrating different capabilities of Amazon SageMaker RL.

- [HVAC using EnergyPlus](reinforcement_learning/rl_hvac_coach_energyplus) demonstrates the training of HVAC systems using the EnergyPlus environment.
- [Mountain Car](reinforcement_learning/rl_mountain_car_coach_gymEnv) Mountain car is a classic RL problem. This notebook explains how to solve this using the OpenAI Gym environment.
- [Travelling Salesman](reinforcement_learning/rl_traveling_salesman_vehicle_routing_coach) is a classic NP hard problem, which this notebook solves with AWS SageMaker RL.
- [Unity Game Agent](reinforcement_learning/rl_unity_ray) shows how to use RL algorithms to train an agent to play Unity3D game.

### Scientific Details of Algorithms

These examples provide more thorough mathematical treatment on a select group of algorithms.

- [Latent Dirichlet Allocation (LDA)](scientific_details_of_algorithms/lda_topic_modeling) dives into Amazon SageMaker's spectral decomposition approach to LDA.

### Amazon SageMaker Debugger

These examples provide and introduction to SageMaker Debugger which allows debugging and monitoring capabilities for training of machine learning and deep learning algorithms. Note that although these notebooks focus on a specific framework, the same approach works with all the frameworks that Amazon SageMaker Debugger supports. The notebooks below are listed in the order in which we recommend you review them.

- [Using a built-in rule with TensorFlow](sagemaker-debugger/tensorflow_builtin_rule/)
- [Using a custom rule with TensorFlow Keras](sagemaker-debugger/tensorflow_keras_custom_rule/)
- [Reacting to CloudWatch Events from Rules to take an action based on status with TensorFlow](sagemaker-debugger/tensorflow_action_on_rule/)

### Amazon SageMaker Distributed Training

These examples provide an introduction to SageMaker Distributed Training Libraries for data parallelism and model parallelism. The libraries are optimized for the SageMaker training environment, help adapt your distributed training jobs to SageMaker, and improve training speed and throughput.
More examples for models such as BERT and YOLOv5 can be found in [distributed_training/](https://github.com/aws/amazon-sagemaker-examples/tree/main/training/distributed_training).

### Amazon SageMaker Smart Sifting

These examples provide an Introduction to Smart Sifting library. Smart Sifting is a framework to speed up training of PyTorch models. The framework implements a set of algorithms that filter out inconsequential training examples during training, reducing the computational cost and accelerating the training process. It is configuration-driven and extensible, allowing users to add custom logic to transform their training examples into a filterable format. Smart sifting provides a generic utility for any DNN model, and can reduce the training cost by up to 35% in infrastructure cost.
  
- [Train Image Classification using Vision Transformer with Smart Sifting](https://github.com/aws/amazon-sagemaker-examples/tree/main/training/smart_sifting/Image_Classification_VIT/Train_Image_classification.ipynb): This Example shows how to use Smart sifting to fine tune Vision Transformers for Image Classification.
- [Train Text Classification using BERT with Smart Sifting](https://github.com/aws/amazon-sagemaker-examples/tree/main/training/smart_sifting/Text_Classification_BERT/Train_text_classification.ipynb): This Example shows how to use Smart Sifting to fine tune BERT for Text Classification.

### Amazon SageMaker Clarify

These examples provide an introduction to SageMaker Clarify which provides machine learning developers with greater visibility into their training data and models so they can identify and limit bias and explain predictions.

- [Fairness and Explainability with SageMaker Clarify](sagemaker-clarify/fairness_and_explainability) shows how to use SageMaker Clarify Processor API to measure the pre-training bias of a dataset and post-training bias of a model, and explain the importance of the input features on the model's decision.
- [TimeSeries Explainability with SageMaker Clarify](sagemaker-clarify/time_series_deepar) shows how to use SageMaker Clarify Processor API to explain the importance of the input features on the time-series model's decision.
- [Amazon SageMaker Clarify Model Monitors](sagemaker_model_monitor/fairness_and_explainability) shows how to use SageMaker Clarify Model Monitor API to schedule bias monitor to monitor predictions for bias drift on a regular basis, and schedule explainability monitor to monitor predictions for feature attribution drift on a regular basis.

### Publishing content from RStudio on Amazon SageMaker to RStudio Connect

These examples show you how to run R examples, and publish applications in RStudio on Amazon SageMaker to RStudio Connect.

- [Publishing R Markdown](r_examples/rsconnect_rmarkdown/) shows how you can author an R Markdown document (.Rmd, .Rpres) within RStudio on Amazon SageMaker and publish to RStudio Connect for wide consumption.
- [Publishing R Shiny Apps](r_examples/rsconnect_shiny/) shows how you can author an R Shiny application within RStudio on Amazon SageMaker and publish to RStudio Connect for wide consumption.
- [Publishing Streamlit Apps](r_examples/rsconnect_streamlit/) shows how you can author a streamlit application withing Amazon SageMaker Studio and publish to RStudio Connect for wide consumption.

### Advanced Amazon SageMaker Functionality

These examples showcase unique functionality available in Amazon SageMaker. They cover a broad range of topics and utilize a variety of methods, but aim to provide the user with sufficient insight or inspiration to develop within Amazon SageMaker.

- [Distributed Training and Batch Transform with Sentiment Classification](advanced_functionality/sentiment_parallel_batch) shows how to use SageMaker Distributed Data Parallelism, SageMaker Debugger, and distrubted SageMaker Batch Transform on a HuggingFace Estimator, in a sentiment classification use case.
- [Connecting to Redshift](advanced_functionality/working_with_redshift_data) demonstrates how to copy data from Redshift to S3 and vice-versa without leaving Amazon SageMaker Notebooks.
- [Bring Your Own XGBoost Model](advanced_functionality/xgboost_bring_your_own_model) shows how to use Amazon SageMaker Algorithms containers to bring a pre-trained model to a realtime hosted endpoint without ever needing to think about REST APIs.
- [Bring Your Own k-means Model](advanced_functionality/kmeans_bring_your_own_model) shows how to take a model that's been fit elsewhere and use Amazon SageMaker Algorithms containers to host it.
- [Bring Your Own scikit Algorithm](advanced_functionality/scikit_bring_your_own) provides a detailed walkthrough on how to package a scikit learn algorithm for training and production-ready hosting.
- [Bring Your Own TensorFlow Model](advanced_functionality/tensorflow_iris_byom) shows how to bring a model trained anywhere using TensorFlow into Amazon SageMaker.
- [Bring Your Own Model train and deploy BERTopic](advanced_functionality/pytorch_extend_container_train_deploy_bertopic) shows how to bring a model through an external library, how to train it and deploy it into Amazon SageMaker by extending the pytorch base containers.
- [Host Multiple Models with Your Own Algorithm](advanced_functionality/multi_model_bring_your_own) shows how to deploy multiple models to a realtime hosted endpoint with your own custom algorithm.
- [Host Multiple Models with XGBoost](advanced_functionality/multi_model_xgboost_home_value) shows how to deploy multiple models to a realtime hosted endpoint using a multi-model enabled XGBoost container.
- [Host Multiple Models with SKLearn](advanced_functionality/multi_model_sklearn_home_value) shows how to deploy multiple models to a realtime hosted endpoint using a multi-model enabled SKLearn container.
- [Host Multimodal HuggingFace Model](advanced_functionality/huggingface_deploy_instructpix2pix) shows how to host an instruction based image editing model from HuggingFace as a SageMaker endpoint using single core or multi-core GPU based instances. Inference Recommender is used to run load tests and compare the performance of instances.
- [SageMaker Training and Inference with Script Mode](sagemaker-script-mode) shows how to use custom training and inference scripts, similar to those you would use outside of SageMaker, with SageMaker's prebuilt containers for various frameworks like Scikit-learn, PyTorch, and XGBoost.
- [Host Models with NVidia Triton Server](sagemaker-triton) shows how to deploy models to a realtime hosted endpoint using [Triton](https://developer.nvidia.com/nvidia-triton-inference-server) as the model inference server.
- [Heterogenous Clusters Training in TensorFlow or PyTorch](training/heterogeneous-clusters/README.md) shows how to train using TensorFlow tf.data.service (distributed data pipeline) or Pytorch (with gRPC) on top of Amazon SageMaker Heterogenous clusters to overcome CPU bottlenecks by including different instance types (GPU/CPU) in the same training job.

### Amazon SageMaker Neo Compilation Jobs

These examples provide an introduction to how to use Neo to compile and optimize deep learning models.

- [Deploying pre-trained PyTorch vision models](sagemaker_neo_compilation_jobs/pytorch_torchvision) shows how to use Amazon SageMaker Neo to compile and optimize pre-trained PyTorch models from TorchVision.

### Amazon SageMaker Processing

These examples show you how to use SageMaker Processing jobs to run data processing workloads.

- [Scikit-Learn Data Processing and Model Evaluation](sagemaker_processing/scikit_learn_data_processing_and_model_evaluation) shows how to use SageMaker Processing and the Scikit-Learn container to run data preprocessing and model evaluation workloads.
- [Feature transformation with Amazon SageMaker Processing and Dask](sagemaker_processing/feature_transformation_with_sagemaker_processing_dask) shows how to use SageMaker Processing to transform data using Dask distributed clusters
- [Distributed Data Processing using Apache Spark and SageMaker Processing](sagemaker_processing/spark_distributed_data_processing) shows how to use the built-in Spark container on SageMaker Processing using the SageMaker Python SDK.

### Amazon SageMaker Pipelines

These examples show you how to use [SageMaker Pipelines](https://aws.amazon.com/sagemaker/pipelines) to create, automate and manage end-to-end Machine Learning workflows.

- [Amazon Comprehend with SageMaker Pipelines](sagemaker-pipelines/nlp/amazon_comprehend_sagemaker_pipeline) shows how to deploy a custom text classification using Amazon Comprehend and SageMaker Pipelines.
- [Amazon Forecast with SageMaker Pipelines](sagemaker-pipelines/time_series_forecasting/amazon_forecast_pipeline) shows how you can create a dataset, dataset group and predictor with Amazon Forecast and SageMaker Pipelines.
- [Multi-model SageMaker Pipeline with Hyperparamater Tuning and Experiments](sagemaker-pipeline-multi-model) shows how you can generate a regression model by training real estate data from Athena using Data Wrangler, and uses multiple algorithms both from a custom container and a SageMaker container in a single pipeline.
- [SageMaker Pipeline Local Mode with FrameworkProcessor and BYOC for PyTorch with sagemaker-training-toolkig](sagemaker-pipelines/tabular/local-mode/framework-processor-byoc)
- [SageMaker Pipeline Step Caching](sagemaker-pipelines/tabular/caching) shows how you can leverage pipeline step caching while building pipelines and shows expected cache hit / cache miss behavior.
- [Native AutoML step in SageMaker Pipelines](sagemaker-pipelines/tabular/automl-step/sagemaker_autopilot_pipelines_native_auto_ml_step.ipynb) shows how you can use SageMaker Autopilot with a native AutoML step in SageMaker Pipelines for end-to-end AutoML training automation.
- [Computer Vision Pipeline using step decorator](sagemaker-pipelines/step-decorator/computer-vision-examples/computer-vision-pipeline.ipynb) shows how you can augment a dataset, train a computer vision model, and evaluate the model using a combination of built-in steps and the step decorator.

### Amazon SageMaker Pre-Built Framework Containers and the Python SDK

#### Pre-Built Deep Learning Framework Containers

These examples show you how to train and host in pre-built deep learning framework containers using the SageMaker Python SDK.

- [IRIS with Scikit-learn](sagemaker-python-sdk/scikit_learn_iris) trains a Scikit-learn classifier on IRIS data
- [Model Registry and Batch Transform with Scikit-learn](sagemaker-python-sdk/scikit_learn_model_registry_batch_transform) trains a Scikit-learn Random Forest model, registers it in Model Registry, and runs a Batch Transform Job.
- [TensorFlow training and serving](sagemaker-python-sdk/tensorflow_script_mode_training_and_serving) trains a basic neural network on MNIST
- [TensorFlow with Horovod](sagemaker-python-sdk/tensorflow_script_mode_horovod) trains on MNIST using Horovod for distributed training

#### Pre-Built Machine Learning Framework Containers

These examples show you how to build Machine Learning models with frameworks like Apache Spark or Scikit-learn using SageMaker Python SDK.

- [Inference with SparkML Serving](sagemaker-python-sdk/sparkml_serving_emr_mleap_abalone) shows how to build an ML model with Apache Spark using Amazon EMR on Abalone dataset and deploy in SageMaker with SageMaker SparkML Serving.
- [Pipeline Inference with Scikit-learn and LinearLearner](sagemaker-python-sdk/scikit_learn_inference_pipeline) builds a ML pipeline using Scikit-learn preprocessing and LinearLearner algorithm in single endpoint

### Using Amazon SageMaker with Apache Spark

These examples show how to use Amazon SageMaker for model training, hosting, and inference through Apache Spark using [SageMaker Spark](https://github.com/aws/sagemaker-spark). SageMaker Spark allows you to interleave Spark Pipeline stages with Pipeline stages that interact with Amazon SageMaker.

- [MNIST with SageMaker PySpark](sagemaker-spark/pyspark_mnist)
- [Parameterize spark configuration in pipeline PySparkProcessor execution](sagemaker-spark/parameterize-spark-config-pysparkprocessor-pipeline) shows how you can define spark-configuration in different pipeline PysparkProcessor executions

### Using Amazon SageMaker with Amazon Keyspaces (for Apache Cassandra)

These examples show how to use Amazon SageMaker to read data from [Amazon Keyspaces](https://docs.aws.amazon.com/keyspaces/).

- [Train Machine Learning Models using Amazon Keyspaces as a Data Source](ingest_data/sagemaker-keyspaces)

### AWS Marketplace

#### Create algorithms/model packages for listing in AWS Marketplace for machine learning.

These example notebooks show you how to package a model or algorithm for listing in AWS Marketplace for machine learning.

- [Creating Marketplace Products](aws_marketplace/creating_marketplace_products)
  - [Creating a Model Package - Listing on AWS Marketplace](aws_marketplace/creating_marketplace_products/models) provides a detailed walkthrough on how to package a pre-trained model as a SageMaker Model Package that can be listed on AWS Marketplace.
  - [Creating Algorithm and Model Package - Listing on AWS Marketplace](aws_marketplace/creating_marketplace_products/algorithms) provides a detailed walkthrough on how to package a scikit learn algorithm to create SageMaker Algorithm and SageMaker Model Package entities that can be used with the enhanced SageMaker Train/Transform/Hosting/Tuning APIs and listed on AWS Marketplace.

Once you have created an algorithm or a model package to be listed in the AWS Marketplace, the next step is to list it in AWS Marketplace, and provide a sample notebook that customers can use to try your algorithm or model package.

- [Curate your AWS Marketplace model package listing and sample notebook](aws_marketplace/curating_aws_marketplace_listing_and_sample_notebook/ModelPackage) provides instructions on how to craft a sample notebook to be associated with your listing and how to curate a good AWS Marketplace listing that makes it easy for AWS customers to consume your model package.
- [Curate your AWS Marketplace algorithm listing and sample notebook](aws_marketplace/curating_aws_marketplace_listing_and_sample_notebook/Algorithm) provides instructions on how to craft a sample notebook to be associated with your listing and how to curate a good AWS Marketplace listing that makes it easy for your customers to consume your algorithm.

#### Use algorithms, data, and model packages from AWS Marketplace

These examples show you how to use model-packages and algorithms from AWS Marketplace and dataset products from AWS Data Exchange, for machine learning.

- [Using Algorithms](aws_marketplace/using_algorithms)
  - [Using Algorithm From AWS Marketplace](aws_marketplace/using_algorithms/amazon_demo_product) provides a detailed walkthrough on how to use Algorithm with the enhanced SageMaker Train/Transform/Hosting/Tuning APIs by choosing a canonical product listed on AWS Marketplace.
  - [Using AutoML algorithm](aws_marketplace/using_algorithms/automl) provides a detailed walkthrough on how to use AutoML algorithm from AWS Marketplace.
- [Using Model Packages](aws_marketplace/using_model_packages)
  - [Using Amazon Demo product From AWS Marketplace](aws_marketplace/using_model_packages/amazon_demo_product) provides a detailed walkthrough on how to use Model Package entities with the enhanced SageMaker Transform/Hosting APIs by choosing a canonical product listed on AWS Marketplace.
  - [Using models for extracting vehicle metadata](aws_marketplace/using_model_packages/auto_insurance) provides a detailed walkthrough on how to use pre-trained models from AWS Marketplace for extracting metadata for a sample use-case of auto-insurance claim processing.
  - [Using models for identifying non-compliance at a workplace](aws_marketplace/using_model_packages/improving_industrial_workplace_safety) provides a detailed walkthrough on how to use pre-trained models from AWS Marketplace for extracting metadata for a sample use-case of generating summary reports for identifying non-compliance at a construction/industrial workplace.
  - [Creative writing using GPT-2 Text Generation](aws_marketplace/using_model_packages/creative-writing-using-gpt-2-text-generation) will show you how to use AWS Marketplace GPT-2-XL pre-trained model on Amazon SageMaker to generate text based on your prompt to help you author prose and poetry.
  - [Amazon Augmented AI with AWS Marketplace ML models](aws_marketplace/using_model_packages/amazon_augmented_ai_with_aws_marketplace_ml_models) will show you how to use AWS Marketplace pre-trained ML models with Amazon Augmented AI to implement human-in-loop workflow reviews with your ML model predictions.
  - [Monitoring data quality in third-party models from AWS Marketplace](aws_marketplace/using_model_packages/data_quality_monitoring) will show you how to perform Data Quality monitoring on a pre-trained third-party model from AWS Marketplace.
  - [Evaluating ML models from AWS Marketplace for person counting use case](aws_marketplace/using_model_packages/evaluating_aws_marketplace_models_for_person_counting_use_case) will show you how to use two AWS Marketplace GluonCV pre-trained ML models for person counting use case and evaluate each model for performance in different types of crowd images.
  - [Preprocessing audio data using a pre-trained machine learning model](aws_marketplace/using_model_packages/preprocessing-audio-data-using-a-machine-learning-model) demonstrates the usage of a pre-trained audio track separation model to create synthetic features and improve an acoustic classification model.
- [Using Dataset Products](aws_marketplace/using_data)
  - [Using Dataset Product from AWS Data Exchange with ML model from AWS Marketplace](aws_marketplace/using_data/using_data_with_ml_model) is a sample notebook which shows how a dataset from AWS Data Exchange can be used with an ML Model Package from AWS Marketplace.
  - [Using Shutterstock Image Datasets to train Image Classification Models](aws_marketplace/using_data/image_classification_with_shutterstock_image_datasets) provides a detailed walkthrough on how to use the [Free Sample: Images & Metadata of “Whole Foods” Shoppers](https://aws.amazon.com/marketplace/pp/prodview-y6xuddt42fmbu?qid=1623195111604&sr=0-1&ref_=srh_res_product_title#offers) from Shutterstock's Image Datasets to train a multi-label image classification model using Shutterstock's pre-labeled image assets. You can learn more about this implementation [from this blog post](https://aws.amazon.com/blogs/awsmarketplace/using-shutterstocks-image-datasets-to-train-your-computer-vision-models/).

### Using Amazon SageMaker for Generative AI use cases

These examples show you how to use AWS services for Generative AI use cases.

- Text-to-image
  - [Fine-tune Stable Diffusion XL model with Kohya](use-cases/text-to-image-fine-tuning) Provides an automated solution to create the necessary components to fine-tune a custom Stable Diffusion XL model.

### Archived

This folder houses legacy, low-viewed, and duplicate notebooks, with a 6-month grace period before deletion. If you believe a notebook has been moved into this folder in error, please submit a PR with justification.
  
## :balance_scale: License

This library is licensed under the [Apache 2.0 License](http://aws.amazon.com/apache2.0/).
For more details, please take a look at the [LICENSE](https://github.com/aws/amazon-sagemaker-examples/blob/master/LICENSE.txt) file.

## :handshake: Contributing

Although we're extremely excited to receive contributions from the community, we're still working on the best mechanism to take in examples from external sources. Please bear with us in the short-term if pull requests take longer than expected or are closed.
Please read our [contributing guidelines](https://github.com/aws/amazon-sagemaker-examples/blob/master/CONTRIBUTING.md)
if you'd like to open an issue or submit a pull request.

