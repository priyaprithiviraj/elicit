# Elicit

Elicit is a browser-based tool for researchers, clinicians, and educators who need a lightweight, portable solution to elicit and record speech for language sample analysis. It can support speech production or comprehension tasks that involve pictorial stimuli presented individually or sequentially. 

Elicit was developed specifically for use with bilingual and multilingual populations, and is also designed to collect demographic and language background metadata that such research requires. The session metadata (including participant demographics, language background, elicitor information, stimulus set, and task type) is recorded alongside audio onset and offset timestamps in a single exportable CSV file. A CLAN-compatible CHAT header file with prepopulated lines is also automatically generated from the session metadata, which can significantly reduce manual preparation time before transcription.

To support data collection in low-resource or access-constrained contexts, Elicit runs as a single HTML file and requires no installation, server infrastructure, or even internet connection (if downloaded). All audio recording, processing, and file export are performed locally within the browser, and no participant data is transmitted to any external system at any point.

### System Requirements

A standards-compliant browser with support for the Web Audio API and MediaRecorder (Chrome or Edge version 90 or later is recommended; Firefox and Safari are also supported). Microphone access is required and must be granted by the user. The file must be opened as a local file or served over HTTPS for microphone access to function; this constraint is imposed by browser security policy, not by the tool itself.

### How to Use

**Step 1 - Session Details** 

Before recording, click on button 1 and enter the session metadata into the Session Details panel. A session ID is generated automatically in the format SES-{timestamp}-{random}, but it can be edited. There is a checkbox to record whether any warm-up protocol was administered. All metadata fields are optional but are recommended for research use, as they populate both the CSV output and the CHAT header.

![Screenshot 1](https://github.com/user-attachments/assets/e4ba45de-cbfd-47f0-a2b6-bf5be17c7f53)


**Step 2 - Upload Images** 

Click on button 2 and upload the stimulus images from the local file system (JPG, PNG, or GIF format). The images are sorted alphanumerically upon loading and presented in a forward-only carousel to prevent inadvertent re-exposure to earlier stimuli. However, individual images can be displayed or deleted by hovering over the thumbnail and selecting the control, provided recording is not in progress.

![Screenshot 2](https://github.com/user-attachments/assets/34437cc4-fcd9-4d42-9c04-e5cfd739ba9f)

**Step 3 - Record** 

Click on the Record button to initiate audio capture via the device microphone. A timer will display the elapsed recording time. Click on the Stop button to terminate recording and save the audio for the current session. A tick mark on the thumbnail indicates a completed recording for that image. The Redo button will replace the recording for the current image following user confirmation. Recording will continue across images unless manually stopped; to produce a separate file per image, the user should stop recording after each image before advancing.

![Screenshot 3](https://github.com/user-attachments/assets/e49e083a-2bad-424c-949d-1e8a5a8344a2)

**Step 4 - Review and Transcribe** 

Click on the Play button for a playback of the current audio recording. The Transcript panel and the Notes panel, displayed to the right of the image viewer, can be used to transcribe the speech sample and to note down observations. The transcripts and notes are stored per image in the session CSV file, and the transcript is also saved as a CHAT file (.cha) on export.

![Screenshot 4](https://github.com/user-attachments/assets/f486abe7-6ace-4881-9ef4-1796fdc51dbb)

**Step 5 - Download and Reset** 

Click on the Download button to export all the output files for the session (see Output section). The autosave state will be cleared following a successful download. The Reset button, displayed in the session bar once images have been loaded, clears all recordings, images, and metadata. If recordings are present, the user is prompted to download before proceeding.

---

### Output

Three file types are exported per session.

**1. WAV audio files**

A session, which spans from "record" to "stop", produces a single WAV audio file for each image. These files are recorded in mono format, using 16-bit PCM at a sample rate of 44,100 Hz. The files are named in sequence as {ParticipantID} image01.wav, {ParticipantID} image02.wav, and so on. This file format is compatible with CLAN, Praat, and SALT.

**2. Session CSV ({ParticipantID}_session.csv)**

The session CSV file will include the following columns for each image: session_id, corpus, participant_id, age, gender, l1, l2, l2_onset, elicitor_id, stimulus_set, task_type, warmup, date, image_number, filename, onset_ms, offset_ms, duration_ms, and notes. The onset and offset times are recorded in milliseconds, measured from the first recording event in the session. The file includes columns for transcripts and notes related to each image. Both fields are optional, and any cells without content will remain empty.

**3. CHAT transcript file ({ParticipantID}.cha)**

A transcript file in CHAT format (.cha) is generated for download and is pre-populated with headers, including @Languages, @Corpus, @Participants, and @ID lines for both the child participant (CHI) and the investigator (INV), as well as @Media, @Date, and @Situation. The corpus field in the CHAT header is derived from the Corpus entry in the Session Details panel. Transcripts consisting of multiple sentences are divided into separate utterance lines. For images without any entered transcript, a placeholder comment is used. If no transcript content has been provided for the session, the file will feature a prompt stating "Paste transcription below" in its place. Regardless of this, the header will remain complete, ensuring that the file is ready to be opened in CLAN. The user has the option to manually add the transcript beneath the header and before the @End line, or they can utilise CLAN to do so.

---

### Notes for Researchers

Users are responsible for obtaining appropriate ethical approval and informed consent from the participants. Child assent and parental consent must be taken when eliciting/recording speech from children.

---

### Citation

If you use Elicit in research or adapt it for your own work, please cite:

> Prithiviraj, P. (2026). Elicit: A picture-based elicitation tool (Version 1.0) [Computer software]. https://priyaprithiviraj.github.io/elicit

---

### License

MIT License © 2026 Priya Prithiviraj. See LICENSE for full terms.
