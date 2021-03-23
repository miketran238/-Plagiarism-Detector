<h1>Plagiarism-Detector </h1>
This project detects plagiarized works from students. Their works are compared to a wikipedia source to check the similarity <br>
<h2>Data: </h2>
    - The data belongs to a real computer science classroom assignment <br>
    - Training size:  70 <br>
    - Test size:  25 <br>
<h2> Features Engineering </h2>
    - Containment N-grams is calculated as the overlapping grams between the source text and the answer text. The score is then normalized over the total number of grams. <br>
    - Ultimately, containment of grams length of 1,3 and 5 were selected as features. <br>
    - The longest common subsequence (LCS) is the longest string of words (or letters) that are the same between the source text and the answer text. <br>
    - LCS is also normalized by dividing by the total number of words (or letters) in the Student Answer Text. LCS is treated as one feature, so we have 6 features in total.
<h2> Developed a machine learning model </h2>
- Since the problem is a binary classification and the data is small, Support Vector Machine is chosen for task.<br>
- Vectorizes the categories and the features as numericals. <br>
- Train and test the SVM model using AWS/SageMaker/EC2 that achieved 100% accuracy. <br>
