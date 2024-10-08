# Amazon-Machine-Learning-Challenge-2024

Amazon Machine Learning Competition Report
 Team Name: TAMS
 
 Approach
 1. Text Extraction with EasyOCR
 Our initial step involved extracting text from product images using the EasyOCR model.
 Since product labels and specifications might appear in different orientations, we rotated the
 images at angles of 90°, 180°, and 270° to ensure no text was missed due to orientation.
 EasyOCR was slow efficiently provided the text that served as input for the next phase.
 2. Entity Extraction Using Llava Model
 After gathering the text from images, we employed the Llava model, a deep learning model
 that specializes in extracting entities from image-text pairs. We passed the product image
 and the extracted text into the LLaVa model, embedding the text through a custom prompt.
 The model then generated the corresponding product entity values, such as weight, volume,
 voltage, wattage, and dimensions, along with their associated units.
 3. Post-Processing
 The output from the Llava model required post-processing to ensure that the extracted
 values were formatted correctly and aligned with the competition's specifications. This step
 involved refining the unit detection and ensuring consistent output formats across the
 dataset, ensuring that each entity was correctly paired with its respective unit.
 Conclusion
 Our approach of combining OCR-based text extraction with the Llava model for entity
 extraction, followed by careful post-processing, allowed us to accurately retrieve product
 specifications from images. This method proved effective in handling various image
 orientations and ensuring that both the entity values and their units were properly identified.
