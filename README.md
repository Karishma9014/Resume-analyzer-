# Resume-analyzer-
Resume Analyzer is a Python-based application that analyzes a candidate’s resume and checks important details such as skills, education, experience, and keywords. It compares the resume with a job description and gives a matching score along with suggestions for improvement.
# Resume Analyzer

print("===== RESUME ANALYZER =====")

resume = input("Enter your resume text:\n").lower()

# Skills to check
skills = [
    "python", "java", "c", "c++", "html", "css",
    "javascript", "sql", "machine learning",
    "artificial intelligence", "arduino", "communication"
]

found_skills = []
missing_skills = []

# Check skills
for skill in skills:
    if skill in resume:
        found_skills.append(skill)
    else:
        missing_skills.append(skill)

# Calculate score
score = (len(found_skills) / len(skills)) * 100

print("\n===== ANALYSIS RESULT =====")
print("Skills Found:", ", ".join(found_skills))

print("\nMissing Skills:", ", ".join(missing_skills))

print(f"\nResume Score: {score:.2f}%")

# Suggestions
print("\n===== SUGGESTIONS =====")

if score >= 70:
    print("Your resume has a good skill match.")
elif score >= 40:
    print("Your resume is average. Consider adding more relevant skills.")
else:
    print("Your resume needs improvement. Add more job-related skills.")

print("\nThank you for using Resume Analyzer!")
