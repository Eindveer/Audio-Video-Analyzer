Audio/Video Analyzer

Step 1: Installs tools like Whisper, spaCy, and PyAnnote for:
- Transcribing audio, Detecting speakers, Summarizing and analyzing speech

Downloads language tools for
- Keyword detection, Name/place/date recognition
  
  ![Screen Shot 2025-04-02 at 3 33 34 AM](https://github.com/user-attachments/assets/380cafb3-167a-4f2c-a702-e07eb72c5a5a)

Step 2: Upload your audio or video file
- This step lets the user upload a file from their computer into Colab. The uploaded file is stored in the variable file_path, which will be used later for transcription and speaker detection.

![Screen Shot 2025-04-02 at 3 38 02 AM](https://github.com/user-attachments/assets/228dd934-ce3d-4eb7-8afa-1b6f0cc53db0) 

Step 3: Extract audio from video (if needed)
- This code checks if the uploaded file is a video (like .mp4) and extracts the audio. If the file is already an audio file (like .mp3 or .wav), it skips the conversion and just returns the original path.
  
![Screen Shot 2025-04-02 at 3 39 28 AM](https://github.com/user-attachments/assets/ceefd3a2-b3db-43ae-b52d-66a8b0fb6536) 

Step 4: Transcribe the audio with Whisper
- This step loads OpenAI’s Whisper model and transcribes the uploaded audio file into text. You can choose a faster model like "tiny" to save time.
- Use this to generate text from your audio. The transcript holds the full text, and segments include timestamps for each line.
  
![Screen Shot 2025-04-02 at 3 40 19 AM](https://github.com/user-attachments/assets/66c64830-604a-4f6a-b3e8-8940bec2bbc3) 

Step 5: Summarize the transcript
- This step uses a pre-trained transformer model to turn long transcripts into short, readable summaries. It splits the transcript into chunks so even long audio can be summarized smoothly.
- Use this when you want a quick summary of your full audio or interview without reading the entire transcript.
- The file I used was unnder 100 words so there was not need for it to be summarized.
  
![Screen Shot 2025-04-02 at 3 46 34 AM](https://github.com/user-attachments/assets/c0cc64aa-5528-481d-8563-bd6ec56acb37) 

Step 6: Extract keywords from the transcript
- This step uses KeyBERT to find the most important words and short phrases in the transcript. These keywords represent the main topics discussed in the audio.
- Use this to quickly find the key themes or topics in your interview, podcast, or meeting recording. 

![Screen Shot 2025-04-02 at 3 47 50 AM](https://github.com/user-attachments/assets/6cbbdf71-b1aa-4220-9fc4-833749cb1e14) 

Step 7: Identify speakers in the audio (Speaker Diarization)
- This step uses pyannote.audio to detect who is speaking and when. It prints the start and end times for each speaker segment with a speaker label (like SPEAKER_00).
- Use this to break the audio into speaker sections — especially helpful in interviews, meetings, or multi-person podcasts.

![Screen Shot 2025-04-02 at 3 49 15 AM](https://github.com/user-attachments/assets/c556814d-7dcc-4dbe-8086-ea9e0a4d8b23)

Step 8: Print timestamped transcript segments
- This step prints each line of the transcript along with its start and end time. These timestamps help you locate when something was said in the audio.
- Use this to get a timeline of what was said, great for note-taking, syncing subtitles, or reviewing long recordings.

![Screen Shot 2025-04-02 at 3 49 52 AM](https://github.com/user-attachments/assets/9f212fad-5699-4a5f-a582-682f44e95ec8) 

Step 9: Extract names, places, and dates (Named Entity Recognition)
- This step uses spaCy to find and label people, organizations, places, and dates mentioned in the transcript.
- Use this to identify key details from your audio, like who was mentioned, what locations were referenced, and when events took place.

![Screen Shot 2025-04-02 at 3 52 04 AM](https://github.com/user-attachments/assets/831b84df-dc0e-499b-b277-7d8eb443ca85) 

Step 10: Detect emotional tone in the audio
- This step uses a BERT-based model to detect the emotional tone of your transcript — emotions like joy, anger, sadness, etc.

![Screen Shot 2025-04-02 at 3 53 05 AM](https://github.com/user-attachments/assets/c6aa3793-83d7-40cc-a53b-e3735dfa20ee) 

Step 11: Save results to text and Excel
- This step saves your summary, keywords, named entities, and emotion analysis to downloadable files — perfect for reports or sharing.
- Use this to export your analysis for documentation or reports, everything is saved and downloadable.

![Screen Shot 2025-04-02 at 3 54 36 AM](https://github.com/user-attachments/assets/0a0ce5d6-7bb6-48fd-a7b2-be6040e4b7e7) ![Screen Shot 2025-04-02 at 3 54 46 AM](https://github.com/user-attachments/assets/cdab3911-1820-49ab-bfb9-ab35c0166cac)


