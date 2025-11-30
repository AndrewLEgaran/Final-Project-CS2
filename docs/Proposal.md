Project Title:
Software Reconstruct

Problem Statement:
The Software needs to be improved further for the client's satisfaction level to reach the desired satisfaction level and to make the software much more better for more users in the future. Solving this will help us find what the clients' want and we will be able to acquire empathy to others in order to help them in solving their problem and helping in their need. According to the Survey data that we have acquired, We can mostly see very positive results but there are still some reviews that had a few problems when using the software and we want to improve it to fit it to their tastes.

Project Objectives:
1. Collect and analyze the reviews to find which part of the software needs to improve.
2. Find out which feature of the software needs improvement by averaging questions 1 to questions 6
3. Understand how to code datasets to find the data that we want to get.

Planned Features:
1. What is the average score for each question (q1_satisfaction to q6_overall)?
2. Which question received the highest average rating overall?
3. Which question received the lowest average rating overall?
4. Show what comments replied with suggestions of improvement.
5. Show which comments are satisfied with the results.

Planned Inputs and Outputs:

Inputs:
No inputs

Outputs:
Lowest average rating overall, highest average rating overall, Comments with suggestions, Comments that are satisfied

Logic Plan:

Flowchart:
<img width="1678" height="556" alt="Screenshot 2025-11-30 135105" src="https://github.com/user-attachments/assets/b55cd64f-4434-4acc-aae1-e386eb5d3c7c" />

Pseudocode:
q1_satisfaction ← [4, 3, 5, 2, 4, 5, 3, 4, 2, 5]
q2_usability     ← [5, 3, 4, 3, 4, 5, 2, 4, 2, 5]
q3_design        ← [4, 3, 5, 2, 5, 4, 3, 4, 2, 5]
q4_clarity       ← [5, 4, 5, 3, 4, 5, 3, 4, 2, 5]
q5_recommend     ← [5, 3, 5, 2, 5, 5, 2, 4, 1, 5]
q6_overall       ← [5, 3, 5, 2, 4, 5, 3, 4, 2, 5]

q7_comments ← [
    "Very helpful and easy to use. I'd recommend it to friends.",
    "It's okay but could be improved in terms of navigation.",
    "I really liked the experience! It was engaging.",
    "Some parts were confusing. Needs clearer instructions.",
    "Good balance of design and usability. Pretty solid.",
    "Really smooth and enjoyable to use!",
    "The layout is fine but loading speed should be faster.",
    "Consistent performance. Works well on mobile.",
    "I had trouble figuring out some features. Needs improvement.",
    "Perfect! Everything worked just as expected."
]

Function calculate_average(scores_list):
    total ← 0
    For each score in scores_list:
        total ← total + score
    Return total ÷ length(scores_list)

q1average ← calculate_average(q1_satisfaction)
q2average ← calculate_average(q2_usability)
q3average ← calculate_average(q3_design)
q4average ← calculate_average(q4_clarity)
q5average ← calculate_average(q5_recommend)
q6average ← calculate_average(q6_overall)

Print "Average Satisfaction Score:", q1average
Print "Average Usability Score:",    q2average
Print "Average Design Score:",       q3average
Print "Average Clarity Score:",      q4average
Print "Average Recommendation Score:", q5average
Print "Average Overall Score:",      q6average

substrings_positive     ← ["helpful", "engaging", "smooth", "perfect", "consistent", "pretty solid"]
substrings_improvement  ← ["confusing", "improvement", "trouble", "should be", "could be improved", "poor"]

For each comment in q7_comments:
    lower_text ← to_lowercase(comment)

    If any(sub in lower_text for sub in substrings_positive):
        Print "Positive Feedback:", comment

    Else if any(sub in lower_text for sub in substrings_improvement):
        Print "Feedback Needing Improvement:", comment

