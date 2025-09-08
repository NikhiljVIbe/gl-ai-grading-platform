GL AI Grading Platform
An AI-powered platform for automatically evaluating and grading subjective assignments using custom rubrics generated from teaching assistant evaluations.

🚀 Features
Custom Rubric Generation: Automatically creates grading rubrics based on TA evaluations
AI-Powered Evaluation: Uses advanced language models to grade student submissions
Batch Processing: Evaluate multiple submissions efficiently
Confidence Scoring: Provides confidence levels for each evaluation
Detailed Feedback: Generates constructive feedback for students
Analytics: Comprehensive statistics and evaluation insights
📋 Prerequisites
Python 3.8+
OpenAI API key (optional - includes mock evaluation for testing)
pandas, numpy, scikit-learn
🛠️ Installation
Clone the repository:
bash
git clone https://github.com/yourusername/gl-ai-grading-platform.git
cd gl-ai-grading-platform
Install dependencies:
bash
pip install -r requirements.txt
Set up your OpenAI API key (optional):
bash
export OPENAI_API_KEY="your-api-key-here"
🚀 Quick Start
python
from src.gl_ai_grading import GLAIGradingPlatform

# Initialize the platform
platform = GLAIGradingPlatform(api_key="your-openai-api-key")

# Load training data
platform.load_training_data('data/training_data.csv')

# Generate rubrics
rubrics = platform.generate_all_rubrics()

# Evaluate a submission
result = platform.evaluate_submission(
    question_num=1, 
    answer="Student's answer here"
)

print(f"Score: {result.score}/5")
print(f"Feedback: {result.feedback}")
📊 Training Data Format
Your CSV file should include these columns:

Question_Number: Integer identifier for each question
Question: The question text
Answer: Student's answer
Evaluator_Score: TA's score (1-5)
Evaluator_Feedback: TA's detailed feedback
🔧 Configuration
The platform supports various configuration options:

python
platform = GLAIGradingPlatform(
    api_key="your-api-key",
    model_name="gpt-4",  # or "gpt-3.5-turbo"
)
📖 Documentation
User Guide
API Reference
Examples
🧪 Testing
Run tests with:

bash
python -m pytest tests/
📈 Workflow
Training Phase: Load 5+ sample evaluations per question from TAs
Rubric Generation: AI creates custom rubrics based on TA patterns
Evaluation Phase: Use rubrics to grade new student submissions
Quality Assurance: Review confidence scores and statistics
🤝 Contributing
Fork the repository
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request
📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙋‍♀️ Support
If you have any questions or need help:

Open an issue on GitHub
Check our documentation
Review the examples
🔮 Roadmap
 Web interface for easy deployment
 Support for multiple question types
 Integration with popular LMS platforms
 Advanced analytics dashboard
 Multi-language support
⭐ Star History
If this project helps you, please give it a star! ⭐

