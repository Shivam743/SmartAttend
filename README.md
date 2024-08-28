# SmartAttend

## Data Requirements

### 1. Student Facial Images
- **Individual Student Photos**:
  - **Resolution**: High-resolution images, standardized to 160x160 pixels.
  - **Number of Images per Student**: 10-20 images per student, capturing variations in facial expressions, angles, and lighting conditions.
  - **Angles**: Images from different angles (front, left, right, slightly above, slightly below).
  - **Appearance Variations**: Include images with different hairstyles, glasses, hats, and without makeup to handle changes in appearance.

- **Classroom Group Photos**:
  - **Resolution**: High-resolution group photos capturing all students clearly.
  - **Angles**: Photos from multiple angles and distances within the classroom.
  - **Lighting Variations**: Photos taken under different lighting conditions (e.g., morning, afternoon, artificial light).
  - **Occlusions**: Include images where faces are partially occluded (e.g., students looking down, partially hidden by objects) to improve robustness.

### 2. Annotation Data
- **Bounding Boxes**: Each face in the training images must be annotated with bounding boxes.
- **Labels**: Each detected face should be labeled with the corresponding student ID or name.

### 3. Triplet Loss Data (For Training, If Applicable)
- **Anchor, Positive, Negative Samples**:
  - **Anchor Image**: A clear, standard image of the student.
  - **Positive Image**: Another image of the same student with a different pose, expression, or under different lighting.
  - **Negative Image**: An image of a different student or a random person.

<!-- ### 4. Validation and Testing Data
- **Separate Dataset**: A distinct set of images not used in training, including a mix of individual and group photos.
- **Cross-Validation**: Use cross-validation with unseen images and classroom scenarios.-->

### 5. Classroom Environment Data
- **Group Photos**: High-quality group photos from various classroom sessions.
- **Lighting Variations**: Images with natural and artificial light, taken at different times of day.
- **Positional Variations**: Photos with students sitting in different positions and postures.

### 6. Attendance Records (Ground Truth)
- **Manual Logs**: Accurate records of student attendance for comparison with the model's predictions.

### 7. Demographic Data (Optional)
- **Age, Gender, Ethnicity**: Include diverse samples to ensure fairness across different demographics.
- **Appearance Changes**: Data covering students with and without accessories like glasses, hats, and masks.

### Data Collection Tips for FaceNet
- **Consistency**: Ensure all images are resized to 160x160 pixels.
- **Quality Over Quantity**: Focus on high-quality, well-labeled images for better performance.
- **Data Augmentation**: Use techniques like rotation, zoom, and color shifts to increase dataset size and variety.
