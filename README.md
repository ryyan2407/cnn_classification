# Selection Task for Project 5: ML for Sustainability: Satellite Data Processing for Detecting Pollution Sources
Submission for Professor Nipun Batra's internship opportunity


# Dataset Preparation

The initial phase involved organizing the dataset for one-vs-rest classification. Given the diversity, this meant creating 90 different binary classifiers. Each classifier had the task of identifying its target animal (in this case, 'cat') against all others ('not cat'), turning the multi-class challenge into multiple binary classification problems. This step was crucial for laying the groundwork for the subsequent classifications.

Transitioning to binary classification, I selected pairs of animals to simplify the complexity, focusing on direct comparisons (e.g., 'cat' vs. 'dog'). This step was instrumental in fine-tuning the approach for distinguishing features between two classes.

The final preparatory step transitioned the task to 5-class classification. Rather than meticulously grouping the animals based on characteristics or representativeness, I selected 5 random animals from the dataset. This approach, while simpler, still required careful consideration to ensure that the random selection did not inadvertently introduce bias. The aim was to maintain a level of unpredictability in the classification task, testing the model's ability to generalize across a less curated set of categories.

# Cross-Validation

Employing 3-fold cross-validation across these stages was vital for assessing the model's generalizability. This methodological approach allowed me to rigorously evaluate the model's performance, ensuring that it wasn't just tailored to a subset of the data but capable of adapting to new, unseen images.

# Model Development

The cornerstone of this project was the development of a custom Convolutional Neural Network (CNN) model. Tasked with avoiding the use of popular pre-built architectures like ResNet or DenseNet, I ventured to create a model from the ground up. This involved intricately designing the number of layers, and filters, and selecting hyperparameters that would best capture the distinct features of animal images within the dataset.

# Training and Evaluation

The training process was a meticulous endeavor where the custom CNN was put to the test against both the one-vs-rest and 5-class classification challenges. Adjusting weights through backpropagation and iterating over the datasets, the model was fine-tuned to reduce classification errors.

Evaluation was conducted through the generation of classification matrices for each classification task. These matrices not only quantified the model's accuracy but offered a granular view of its predictive capabilities, identifying areas of strength and weakness in distinguishing between the classes.

# Convolutional Layer Visualization

Perhaps one of the most enlightening aspects of the project was the visualization of the convolutional layers. This exercise allowed me to peel back the layers of the CNN, quite literally, and observe the features it deemed significant at various levels of abstraction. From simple edges and colors in the initial layers to complex patterns in the deeper layers, these visualizations provided a window into the model's 'thought' process.

During the initial layers, we can see that the model attempts to grasp the basic shapes and edges. As we progress through the network's layers the model begins to identify more intricate features, like textures. In the concluding layers, the network can recognize the specific entities in the image, in this case, the particular animal. As my network was in the beginning of training phases, yet to discern nuanced features comprehensively.
