# Icon Recommendation System

## Overview
This project is an **Icon Recommendation System** designed to help designers find icons that are visually and contextually similar. The system combines **visual features** from the icons with **semantic information** extracted from their names to provide more relevant recommendations. It aims to solve the problem where designers need icons that not only look similar but also fit the intended meaning or context.

## Dataset
The dataset consists of **2,259 icons** from three popular icon sets:
- **Feather Icons**
- **Font Awesome**
- **Heroicons**

The icons have been standardized to **128x128 pixels** in PNG format for consistency.

## Project Goal
The goal of this project is to build a tool that helps designers quickly find icons that are both **visually similar** and **semantically meaningful**. The system uses deep learning techniques to extract **visual features** and word embeddings for **textual features**, combining them to enhance the relevance of icon recommendations.

## Methods and Technologies Used
1. **Data Preprocessing**: All icons were resized to 128x128 pixels and converted to PNG to ensure consistency. Transparency issues were handled by adding a white background to SVG icons.
2. **Visual Feature Extraction**: We used the **MobileNet** model, pre-trained on ImageNet, to extract visual features (or embeddings) from each icon.
3. **Textual Feature Extraction**: Icon names were converted into **textual embeddings** using **GloVe word embeddings**, capturing semantic information.
4. **Combining Features**: Both visual and textual embeddings were concatenated to create a comprehensive feature vector for each icon.
5. **Similarity Calculation**: The **cosine similarity** measure was used to determine how similar each icon is to a given input icon.

## Results
- Using **visual features alone**, the system provided recommendations based solely on the visual appearance, such as shape and style. While effective, it lacked consideration of the meaning behind the icons.
- By **combining visual and textual features**, the system was able to recommend icons that were not only visually similar but also matched the intended context, making the recommendations more useful for designers.

## Demo
The system allows a user to select an icon, either randomly or by specifying the name. The results show visually similar icons when using visual features only, and contextually better matches when using combined features.

## Future Work
Future improvements to this project could include:
- **Fine-tuning MobileNet** on icon data specifically, which could improve the visual similarity search.
- Adding a **user feedback loop** that allows users to rate the quality of the recommendations, which could be used to refine the model.
- Developing a **web interface** to make the system more accessible for users.
