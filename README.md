# Khmer Text Detection Dataset

## Overview
This dataset contains **10,050 synthetic images** with Khmer text, specifically designed for text detection tasks. Each image includes **75-300 words** and is annotated in two formats: **XML** and **YOLOv8**. The dataset introduces diversity by randomly applying **10 Khmer fonts** with a fixed font size of **20**, ensuring variability in the text appearance.

## Dataset Structure
- **Images Folder:** Contains 10,050 images, each with Khmer text.
- **XML Annotations:** Each image has an associated XML file with the following elements:
  - `<image>`: Image file name.
  - `<width>`: Width of the image.
  - `<height>`: Height of the image.
  - `<paragraph>`: Annotates the entire paragraph.
  - `<line>`: Represents individual lines of text.
  - `<word>`: Specifies each word's bounding box coordinates within the image.
  
  The XML files provide detailed annotations for the location and structure of the text within the images.

- **YOLOv8 Annotations:** Each image has an associated text file in YOLOv8's **normalized bounding box format**, making it compatible for use with YOLOv8 for text detection. The format consists of class label and normalized coordinates (x_center, y_center, width, height) for each detected word.

### Example Image
Below is an example image from the dataset, along with its label structure:
![image](https://github.com/user-attachments/assets/65368e22-096f-4c4c-9c2f-d65b02912b9d)


### XML File Example:
Here is an example of how the XML annotations are structured:
```
<metadata>
  <image>kh_data_323.png</image>
  <width>803</width>
  <height>784</height>
  <paragraph/>
  <paragraph id="1">
    <line id="1">
      <word>
        <text>ក្រសួង</text>
        <bbox> x1="65" y1="10" x2="127" y2="42" </bbox>
      </word>
      ...
    </line>
  </paragraph>
</image>
```
### YOLO File Example:
Each YOLOv8 annotation file contains one line per word:
```
<class_id> <x_center> <y_center> <width> <height>
0  0.028402  0.039613  0.030383  0.044014
```
Where:
- <class_id>: Typically set to 0 (for single class detection of Khmer text).
- <x_center>, <y_center>, <width>, and <height> are normalized to the range [0, 1].

## Getting Started
1. **Download the Dataset:** You can download the dataset files from Kaggle Link: (https://www.kaggle.com/datasets/emhengly/khmer-text-detection-dataset).
2. **Unzip the Files:** Make sure to unzip the downloaded files if they come in compressed format.
3. **Explore the Label File:** The label file maps each image to its Khmer word label, allowing you to easily load and preprocess data for model training.

## Citation
If you use this dataset in your research, please cite:
Em, H., Valy, D., Gosselin, B. & Kong, P. (2024). Word Spotting on Khmer Printed Documents. *Techno Science Research Journal (TSRJ)*.

# Contact Information
For more information, please reach out:

- **Author:** Hengly Em  
  - **Email:** emhengly@gmail.com
  - **Facebook:** [Em Hengly](https://www.facebook.com/people/Em-Hengly/pfbid024e1fPwCY6jZTDE4eXvnt5RHB5zeouHJztGjRPtHDRtbeVX2AxiyXvV7QPvqF2kzjl/)
- **Research Group:** ViLa Lab  
  - **Facebook Page:** [ViLa Lab](https://www.facebook.com/vilalabitc/?_rdr)

## License
Specify the license you’re using here.

## Acknowledgments
This research is supported by ViLa Lab and funded by the ARES (Academy of Research and Higher Education) program. We are grateful for their support in advancing text recognition for complex scripts like Khmer.




