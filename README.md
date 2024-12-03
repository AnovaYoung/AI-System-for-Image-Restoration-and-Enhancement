**Data Cleaning and Preparation for Modeling**

Overview of Data Cleaning and Preparation
High-level plan for cleaning and preparation:

**Understand Dataset Content:**

Analyze the structure of the dataset.
Identify tasks (denoising, super-resolution, inpainting, colorization) and the corresponding image pairs.

**Validate and Filter Data**:

Remove non-image files (already done in earlier phases).
Ensure all image files can be opened and are in the correct format.
Check for duplicate or corrupted files.

**Organize Data by Tasks:**

Group images into directories by task (e.g., denoising, super_resolution).
Separate inputs (e.g., noisy/low-res) and targets (e.g., clean/high-res).

**Preprocess Images:**

Standardize dimensions: Resize images to a common resolution (e.g., 256x256 or 512x512) based on model requirements.
Normalize pixel values: Scale pixel values to the range [0, 1] or standardize using ImageNet means/standard deviations if necessary.
Convert grayscale images for colorization tasks.

**Split Data:**

Split the dataset into training, validation, and test sets (e.g., 80% train, 10% validation, 10% test).
Ensure each split has balanced representation across tasks and sources.
Data Augmentation:

Apply augmentations such as random cropping, flipping, rotation, or noise addition to diversify the training data.
Save Cleaned Data:

Save the preprocessed dataset into organized directories or a new zip file for easy retrieval during training.
