# Audio to summarised text using GCP 
Convert audio to sumarised text by using Google Cloud Platform tools (fully automated)

This project utilizes the following tools -
Google Cloud Storage (Bucket)
Google Speech to Text API 
Vertex AI (AutoML)

Basic workflow :
  speech_to_text.py 
-> Audio frame rate and channels are determined
-> creates a bucket in GCP and uploads the locally stored audio file. 
-> The Google speech to text API is used to find the transcript, which is then stored in the bucket. 
-> Repeats for all the audio files in the folder.
-> Transcripts are downloaded and the bucket is deleted.



  sentiment_prediction.py
-> Bucket is created in GCP and locally stored transcript is uploaded. 
-> AutoML's Sentiment Analysis model was trained on multiple appropriate datsets resulting in a accuracy of 92.6%
-> Utilizing the endpoints, we use the model to covert the text to a summarized version.


Note : 
Things you would need :
- JSON key from your GCP account 
- Endpoint ID from your AutoML model
- Project ID from your current project under your GCP account


Two applications of this projects were :
1. Business meeting summarizer : 
Efficient Time Management: A Business Meeting Summarizer can help professionals save valuable time by providing a concise summary of key discussions, decisions, and action items. It allows participants to quickly review important points without having to go through the entire meeting recording or notes.

Enhanced Productivity: By automating the process of summarizing business meetings, professionals can focus more on critical tasks and follow-up actions rather than spending excessive time on manual note-taking and transcription. This leads to increased productivity and allows for better utilization of resources.

Improved Collaboration and Communication: Business Meeting Summarizer can facilitate better collaboration among team members, especially in remote or distributed work environments. By providing a condensed overview of discussions, it ensures that everyone is on the same page and can contribute effectively to the next steps.

Accessibility and Knowledge Sharing: Summarized meeting notes are easier to access and share with relevant stakeholders. This accessibility promotes knowledge sharing within the organization, making it easier for team members who were unable to attend the meeting to catch up on important information and contribute to future discussions.

2. Automated sentiment analysis of feedback calls/audio : 
Enhanced Customer Experience: Automated Sentiment Analysis of feedback calls or audio can help organizations gain valuable insights into customer satisfaction levels, sentiment trends, and areas for improvement. By automatically analyzing and categorizing customer feedback, businesses can identify patterns and take necessary actions to enhance the customer experience.

Real-time Feedback Monitoring: With automated sentiment analysis, businesses can monitor customer feedback in real-time, allowing them to address any negative sentiment or issues promptly. This enables proactive customer support and helps in resolving concerns before they escalate.

Efficient Quality Assurance: By automating the sentiment analysis of feedback calls or audio, organizations can streamline their quality assurance processes. It eliminates the need for manual review of every customer interaction, saving time and resources. This automation ensures a more systematic and consistent evaluation of customer sentiment.

Data-driven Decision Making: Automated sentiment analysis provides businesses with valuable data that can be used for data-driven decision making. It helps identify trends, patterns, and areas of improvement, allowing organizations to make informed strategic decisions to enhance their products, services, and customer satisfaction.
