<h1 align="center">Handwritten Layout Recognition</h1>

<p align="justify">Many students struggle with effectively understanding and retaining the content from their lecture notes. Often, the process of quickly writing down notes during a lecture leaves little time for true comprehension. This problem can result in a significant time waste as students try to revisit and make sense of their hastily written notes after the fact.

To address this challenge, a mobile application called DigiNote has been developed using deep learning technology. The application aims to provide students with a streamlined solution for document extraction and digitization, enabling more efficient review and understanding of lecture materials.
The DigiNote workflow involves the user uploading an image of their handwritten lecture notes. The application then undergoes a series of preprocessing steps, including filtering, grayscaling, binarization, morphological operations, normalization, and augmentation. This preparatory phase ensures the image is optimized for the subsequent deep learning models.
Next, a YOLO (You Only Look Once) model is employed to identify and label the relevant regions within the document. The labeled regions are then processed using OCR (Optical Character Recognition) models, converting the handwritten text into a digital format.
Finally, the processed output is presented to the user in an organized HTML format, allowing for easy review and comprehension of the lecture notes. This integration of deep learning algorithms and postprocessing techniques creates a valuable tool for students, helping to minimize the time waste associated with understanding hastily written lecture notes.</p>


##### Mobile App: 
You can check the mobile app implementaion
<a href="https://github.com/omar546/diginote">HERE!</a>



