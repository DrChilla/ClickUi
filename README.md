# ClickUi - www.ClickUi.app<br>
<div align="center">
The best AI-assistant tool, built for every computer in pure Python. <br>🏗️ The starting ground for the most widely used computer-based AI-assistant, something most people will have installed 🌎<br><br>

![prompot](https://github.com/user-attachments/assets/b1feb373-ae54-4274-9fd0-2c1b2e30926d)<br>

![badge](https://img.shields.io/badge/100%25-Python-blue) 
![badge](https://img.shields.io/badge/STT-Whisper-red)
![badge](https://img.shields.io/badge/TTS-Kokoro-purple)
![badge](https://img.shields.io/badge/GUI-PySide6-cyan)
![badge](https://img.shields.io/badge/Webscraping-Playwright-pink)
![badge](https://img.shields.io/badge/Webscraping-Selenium-forestgreen)
![badge](https://img.shields.io/badge/Live%20Search-Google-orange)
![badge](https://img.shields.io/badge/Models-Ollama-orchid)
![badge](https://img.shields.io/badge/Models-OpenAI-black)
![badge](https://img.shields.io/badge/Models-Google-lightseagreen)
![badge](https://img.shields.io/badge/Models-Claude-darkorchid)
![badge](https://img.shields.io/badge/Models-Groq-darkgreen)
![badge](https://img.shields.io/badge/Models-OpenRouter-sienna)

</div>

# What is it?

ClickUi is a powerful, cross-platform open-source application that integrates various AI models, speech recognition, and web scraping capabilities. It provides a seamless interface for voice and text interactions, file attachments, property lookups, and web searches.

It's 100% Python, and aims to be the best AI-computer assistant. Help us build it to either get it there or keep it that way! See the Future Features & Ideas section

# Collaboration
Looking for Collaborators! Leave Voice mode running, have conversations throughout the day, experience how AI should be on the computer, and build it out to be even better for you/everyone.

Submit new features & ideas in the README as checkboxes so they can be added to the page

**Submit pull requests to main** and they will be reviewed.


---

1-min Demo: https://youtu.be/oH-A1hSdVKQ

---

The AI Assistant operates in two primary modes:
---

- **Voice Mode:** Allows users to interact with the AI using voice commands and receive spoken responses on either your headphones/local audio or a SONOS speaker.
- ![voice_mode](https://github.com/user-attachments/assets/975c762a-c3ef-4ba7-949a-4fe9feacce64)
  
- **Chat Mode:** Provides a text-based interface for typing queries and receiving written responses.
- ![google serch](https://github.com/user-attachments/assets/6716f673-c5d9-4338-8740-46e4588c0fa8)
- ![prompt3](https://github.com/user-attachments/assets/76fe3a4d-4023-4e1a-af73-75be9dba357a)
  
---
### Key Dependencies
---

The AI Assistant relies on two critical dependencies that must be installed and loaded into the global scope before the program can run:

- **Whisper:** An automatic speech recognition (ASR) system used for transcribing voice input.
- **Kokoro:** A text-to-speech engine used for generating spoken responses in Voice Mode.
- **API Keys:** You need to configure the API keys and Engine/Model information to be able to use that AI model.
- ![promtp4](https://github.com/user-attachments/assets/e52c1c85-e483-405b-8a9a-d7b3fe9e3aca)

> **Warning:**  
> The Whisper and Kokoro models are loaded into the global scope. They must be installed and properly configured before running the AI Assistant. Failure to do so will result in runtime errors.
> You can run without Voice functionality & dependencies by commenting the Whisper & Kokoro loading out (but the voice mode will not work)

---
## Future Features 🚀 & Issues ⁉️
- [X] Replace keyboard with pynput to allow cross-platform support for keyboard & mouse interactions (current keyboard library has issues with Mac/Linux) - @SteStein
- [ ] Add interrupt capability during Kokoro output to allow users to just speak to interrupt the current playback & trigger the recording mode loop again.
- [ ] Add Code Formatting to AI replies, with small a copy icon added to each code block output to easily copy the code.
- [ ] Add a Model/Engine functionality to settings via the SettingsWidget (perhaps 'Add New' in bottom of dropdown). Have to define in python right now to make available.
- [ ] Make UI Navigable with arrow keys (after launching with hotkey, cursor starts in Prompt area. From here, allow left arrow key to open settings, down arrow key to pop open conversation window below, etc.)
- [ ] Fix/Revise Voice mode start/stop toggling & related resets. If you click to exit voice mode during transcription or audio playback, sometimes quits entire program
- [ ] Add voice name selection (and model size) for kokoro in SettingsWidget
- [ ] Add hotkey to take selectable area screenshot (or Prnt Scrn) and have it auto-appended to the input chat to easily show the AI what you are looking at/working with.
- [ ] Build tests for all functionality (Prompt input chat, Reply input chat, Conversation History validation, etc)
- [ ] Add a model pricing table to calculate total price of input & output per message/websearch/file upload, etc. Could add option to display below message bubbles, etc.
- [ ] Add multi-file attachment capability (limited to 1 now)
- [ ] Track token usage per message. Could add option to display below message bubbles, etc.
- [ ] Determine the best way to provide executables that work for Windows, Mac, and Linux that will not require the user to do anything other than install our app and run it on a fresh install of each OS (without the user installing Python, CUDA, etc). Or an install script to help get things setup, or Docker, etc
- [ ] Add fine-tuning settings to allow Temp, Top P, Repeat Penalty, etc. to be defined in Settings Widget (something clean/intuitive, maybe a gray horizontal bar like the one to expand the chat window, but above the UI, that lets you adjust these things quickly?) Also need to allow max_tokens per-model for Claude (or get error on API call), new models have thinking tokens/effort, etc. Should add support for all that in the same clean/intuitive SettingsWidget style we have now.
- [ ] Merge to one main Window (right now 2 windows launch in taskbar, one for each area)
- [ ] Option to pop open another chat window with a magnet clip link between them, when selected it links the two input prompts so you can chat with two models at once easily. When not selected you can type different prompts into each. Perhaps a transparent + icon in the upper left of the initial chat bubble that lets you spawn in the other chat bubble?
- [ ] Add WebUI Browser-Use functionality & option to toggle in SettingsWidget: https://github.com/browser-use/web-ui (might need to create a mini version, WebUI is too slow for real-time usage). Have to scan input prompt/transcription for keywords or do tool call to trigger, options for headless to show/hide browser if desired, etc. Then respond once finished to confirm it was done, etc. (See below might want to create our own)
- [ ] Computer interactions that you'd actually want to use. For example, 'Update the system prompt we have in ClickUi. Keep the tool calls and most functionality, but do XYZ...' and it would open ClickUi, navigate to settings, and paste in the new prompt and then say it's done. Or 'Take this prompt and run it through Google AI Studio with Model 1 and Model 2, Anthropic Console with Claude 3 dash 7, and OpenAI o1'. These things would be awesome and revolutionary! Totally possible if we all put our heads together. **The solution has to be versatile and not require much setup/tuning for the user**

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=CodeUpdaterBot/ClickUi&type=Date)](https://www.star-history.com/#CodeUpdaterBot/ClickUi&Date)
---

## Setup/Run
```python
python clickui.py
```
---

### Easy Installation (Windows Only)

1. **Install Anaconda/Conda** <br>
   Download and install Anaconda/Conda from:  
   [https://www.anaconda.com/download/success](https://www.anaconda.com/download/success)<br>
   This allows for easier environment management and Python setup. Install system-wide (for all users) and add to the PATH.<br>

2. **Run Install.bat**<br>
   Available from ClickUi.app and in the GitHub repo<br>
   Running the Install.bat file will download this git repository, run the installation commands below for you, and start the program.<br><br>

   You can use the Install.bat file to launch the program, or `python clickui.py` in your command prompt.

---

### Manual Installation

1. **Install Anaconda/Conda** <br>
   Download and install Anaconda/Conda from:  
   [https://www.anaconda.com/download/success](https://www.anaconda.com/download/success)  
   Needed to install the conda_packages.txt

2. **Keep the files together in one folder**<br>
   You need the sonos.py, the .svg's, etc for the default program to run.<br>
   These are all provided in the GitHub folder, make sure your folder has the same contents as this Repo<br>

2. **Create new Conda environment**
   - Download/clone this repository, and cd to it (change directory). Your command prompt should look like this:
     
     ```bash
     C:\Users\PC\Downloads\ClickUi> 
     ```
   
   - Run `conda -h` in your terminal to check if conda is installed correctly. You should see the help/command options after running this.
     
   - Open Command Prompt/Terminal and run:

   ```bash
   conda create --name click_ui --file conda_packages.txt
   ```

   This creates a new Conda environment named `click_ui` where Python and required libraries will reside.

   - To activate the environment, run:

   ```bash
   conda activate click_ui
   ```

   Your terminal prompt should now display the environment name.

   - Now install all pip modules required:

   ```bash
   pip install -r requirements.txt
   ```

3. **Start the Program**
   - Your command prompt should look like this:
     
     ```bash
     (click_ui) C:\Users\PC\Downloads\ClickUi> 
     ```
   - Now that you are in the folder containing `clickui.py`, run:

   ```bash
   python clickui.py
   ```

   - Once you see the message `Ready!...`, press `Ctrl+k` to bring up the ClickUi interface.

### Configuration

The `.voiceconfig` file in the root directory is where the important settings are stored. 
 - Make edits through the Settings menu in the GUI, or edit the `.voiceconfig` directly. Clicking the Save Config button in the Settings menu overwrites this file.
 - Key settings include:
```json
{
  "use_sonos": false,
  "use_conversation_history": true,
  "BROWSER_TYPE": "chrome",
  "CHROME_USER_DATA": "C:\\Users\\PC\\AppData\\Local\\Google\\Chrome\\User Data",
  "CHROME_DRIVER_PATH": "C:\\Users\\PC\\Downloads\\chromedriver.exe",
  "CHROME_PROFILE": "Profile 10",
  "ENGINE": "OpenAI",
  "MODEL_ENGINE": "gpt-4o",
  "OPENAI_API_KEY": "your-api-key-here",
  "GOOGLE_API_KEY": "your-google-api-key-here",
  "days_back_to_load": 15,
  "HOTKEY_LAUNCH": "ctrl+k"
}
```

Adjust these settings according to your preferences and API keys.

### Conversation History
When enabled, it loads your chats for the last x days from your local `history` folder, and injects them into the chat you have:

![conv_history](https://github.com/user-attachments/assets/72a271c7-8ee0-4f5d-be4f-1f6492cf64a8)

  ⚠️ Conversation History **_can_** consume a lot of tokens quickly! The CLI will print the total tokens of your loaded conversation history when enabled/reloaded.

---

## Core Components

### Speech Recognition

The AI Assistant uses the Whisper model for speech recognition. Here's an implementation example:

```python
import whisper as openai_whisper

whisper_model = openai_whisper.load_model("base", device='cuda')

def record_and_transcribe_once() -> str:
    # ... recording logic ...

    silence_threshold = 70      # 0 = every noice triggers transcription, 100 = very direct input to recognize transcription, depends on your mic, room, etc
    max_silence_seconds = 0.9   # Silence recording loop duration
    MIN_RECORD_DURATION = 0.75  # The minimum speech input duration to be considered a valid input (will skip just 'Hi' but will process 'Hi who is this?', etc

    def transcribe_audio(audio_data, samplerate):
        with tempfile.NamedTemporaryFile(suffix=".wav", delete=False) as tmp:
            temp_wav_name = tmp.name
        sf.write(temp_wav_name, audio_data, samplerate)
        result = whisper_model.transcribe(temp_wav_name, fp16=False)
        return result["text"]

    # ... more recording and transcription logic ...
```

### AI Models Integration

The application supports multiple AI models (OpenAI, Google, Ollama, Claude, Groq, and OpenRouter). An example for the OpenAI model integration is:

```python
def call_openai(prompt: str, model_name: str, reasoning_effort: str) -> str:
    import openai
    import json
    global conversation_messages, OPENAI_API_KEY
    ensure_system_prompt()
    conversation_messages.append({"role": "user", "content": prompt})

    openai.api_key = OPENAI_API_KEY 

    if not openai.api_key:
        stop_spinner()
        print(f"{RED}No OpenAI API key found.{RESET}")
        return ""

    # ... API call logic ...

    try:
        response = openai.chat.completions.create(**api_params)
    except Exception as e:
        print(f"{RED}Error connecting to OpenAI: {e}{RESET}")
        return ""
    
    # ... response handling ...
```

### Web Scraping and External Tools

The AI Assistant includes web scraping capabilities for Google searches and property lookups. Below is an example for the Google search function:

```python
def google_search(query: str) -> str:
    global BROWSER_TYPE
    stop_spinner()
    print(f"{MAGENTA}Google search is: {query}{RESET}")
    encoded_query = quote_plus(query)
    url = f"https://www.google.com/search?q={encoded_query}"
    with sync_playwright() as p:
        browser = p.chromium.launch(headless=True, args=["--disable-blink-features=AutomationControlled"])
        if BROWSER_TYPE == 'chrome':
            context = browser.new_context(
                user_agent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 ..."
            )
        # ... more browser setup ...
        page = context.new_page()
        page.goto(url)
        page.wait_for_load_state("networkidle")
        html = page.content()
        browser.close()
    soup = BeautifulSoup(html, 'html.parser')
    text = soup.get_text()
    cleaned_text = ' '.join(text.split())[0:5000]
    print(cleaned_text)
    return cleaned_text
```

### GUI Implementation

The graphical user interface is implemented using PySide6 (Qt for Python). Below is an example of the main window class:

```python
class BottomBubbleWindow(QWidget):
    global last_chat_geometry
    response_ready = Signal(str, object, object)

    def __init__(self):
        global last_main_geometry, last_chat_geometry        
        super().__init__()
        self.setWindowFlags(Qt.FramelessWindowHint)
        self.setAttribute(Qt.WA_TranslucentBackground, True)
        self.setAttribute(Qt.WA_DeleteOnClose)
        self.response_ready.connect(self.update_ai_reply)

        # Initialize chat dialog with empty content
        self.chat_dialog = ChatDialog(host_window=self)
        if last_chat_geometry:
            self.chat_dialog.setGeometry(last_chat_geometry)
        self.chat_dialog.hide()

        # ... more initialization ...

    def on_message_sent(self, text):
        # ... message handling logic ...

    def process_ai_reply(self, text, container, lb, fresh):
        try:
            ai_reply = call_current_engine(text, fresh=fresh)
        except Exception as e:
            print(f"Error in AI thread: {e}")
            ai_reply = f"[Error: {e}]"
        self.response_ready.emit(ai_reply, container, lb)

    # ... more methods ...
```

---

## Features

### Voice Interaction

The AI Assistant supports voice interactions using the Whisper model for speech recognition and a text-to-speech engine for responses. An example implementation for voice recording is:

```python
def record_and_transcribe_once() -> str:
    global recording_flag, stop_chat_loop, whisper_model
    model = whisper_model
    if recording_flag:
        return ""
    recording_flag = True
    audio_q.queue.clear()
    samplerate = 24000
    blocksize = 1024
    silence_threshold = 70
    max_silence_seconds = 0.9
    MIN_RECORD_DURATION = 1.0
    recorded_frames = []
    speaking_detected = False
    silence_start_time = None

    with sd.InputStream(channels=1, samplerate=samplerate, blocksize=blocksize, callback=audio_callback):
        print(f"{YELLOW}Recording started. Waiting for speech...{RESET}")
        play_wav_file_blocking("recording_started.wav")
        while True:
            if stop_chat_loop:
                break
            # ... recording logic ...

    if stop_chat_loop:
        recording_flag = False
        return ""
    print(f"{GREEN}Recording ended. Transcribing...{RESET}")
    # ... transcription logic ...
    return text_result
```

### Text Chat

Users can interact via text input. The chat interface is implemented within the GUI:

```python
class ChatDialog(QWidget):
    global conversation_messages
    def __init__(self, host_window):
        global conversation_messages
        super().__init__()
        self.host_window = host_window
        self.setWindowFlags(Qt.FramelessWindowHint)
        self.setAttribute(Qt.WA_TranslucentBackground, True)
        self.setAttribute(Qt.WA_DeleteOnClose)

        # ... UI setup ...

        self.reply_line = QLineEdit()
        self.reply_line.setPlaceholderText("Type your reply...")
        reply_layout.addWidget(self.reply_line, stretch=1)
        self.reply_send_button = QToolButton()
        self.reply_send_button.setText("↑")
        self.reply_send_button.setToolTip("Send Reply")
        reply_layout.addWidget(self.reply_send_button)
        self.reply_send_button.clicked.connect(self.handle_reply_send)
        self.reply_line.returnPressed.connect(self.handle_reply_send)

    def handle_reply_send(self):
        text = self.reply_line.text().strip()
        if text:
            self.add_message(text, role="user")
            self.reply_line.clear()
            container, lb = self.add_loading_bubble()
            def do_ai_work():
                try:
                    ai_reply = call_current_engine(text, fresh=False)
                except Exception as e:
                    print("Error in AI thread:", e)
                    ai_reply = f"[Error: {e}]"
                self.host_window.response_ready.emit(ai_reply, container, lb)
            th = threading.Thread(target=do_ai_work, daemon=True)
            th.start()

    # ... more methods ...
```

### File Attachments

The AI Assistant supports file attachments for text-based files. File handling is implemented as follows:

```python
class FileDropLineEdit(QLineEdit):
    file_attached = Signal(list)  # Signal to notify when a file is attached

    def __init__(self, parent=None):
        super().__init__(parent)
        self.setAcceptDrops(True)
        self.attachments = []  # Holds dictionaries: {'filename': ..., 'content': ...}

    def dragEnterEvent(self, event):
        if event.mimeData().hasUrls():
            for url in event.mimeData().urls():
                file_path = url.toLocalFile()
                if os.path.splitext(file_path)[1].lower() in ['.txt', '.csv', '.xlsx', '.xls']:
                    event.acceptProposedAction()
                    return
            event.ignore()
        else:
            super().dragEnterEvent(event)

    def dropEvent(self, event):
        if event.mimeData().hasUrls():
            attachments = []
            for url in event.mimeData().urls():
                file_path = url.toLocalFile()
                ext = os.path.splitext(file_path)[1].lower()
                if ext in ['.txt', '.csv', '.xlsx', '.xls']:
                    file_name = os.path.basename(file_path)
                    try:
                        content = read_file_content(file_path)
                        attachments.append({'filename': file_name, 'content': content})
                    except Exception as e:
                        attachments.append({'filename': file_name, 'content': f"Error reading file: {str(e)}"})
            if attachments:
                self.attachments = attachments
                self.file_attached.emit(attachments)
            event.acceptProposedAction()
        else:
            super().dropEvent(event)
```

### Property Lookup

The assistant can retrieve property value estimates from Zillow and Redfin. An example implementation:

```python
def fetch_property_value(address: str) -> str:
    global driver
    # Kill any lingering Chromium instances before starting a new search.
    kill_chromium_instances()
    try:
        driver
    except NameError:
        # ... driver setup ...

    stop_spinner()
    print(f"{MAGENTA}Address for search: {address}{RESET}")
    stop_spinner()

    search_url = "https://www.google.com/search?q=" + address.replace(' ', '+')
    try:
        driver.get(search_url)
        time.sleep(3.5)
    except Exception as e:
        stop_spinner()
        print(f"{RED}[DEBUG] Exception during driver.get: {e}{RESET}")
        stop_spinner()
        return "Error performing Google search."

    # ... search for Zillow and Redfin links ...

    def open_in_new_tab(url):
        # ... open URL in new tab and return page HTML ...

    def parse_redfin_value(source):
        # ... parse Redfin value from HTML ...

    def parse_zillow_value(source):
        # ... parse Zillow value from HTML ...

    property_values = []
    for domain, link in links_found.items():
        if not link:
            continue
        page_html = open_in_new_tab(link)
        extracted_value = None
        if domain == 'Redfin':
            extracted_value = parse_redfin_value(page_html)
        elif domain == 'Zillow':
            extracted_value = parse_zillow_value(page_html)
        if extracted_value:
            property_values.append((domain, extracted_value))

    if not property_values:
        return "Could not retrieve property values."

    result_phrases = []
    for domain, value in property_values:
        result_phrases.append(f"{domain} estimates the home is worth {value}")
    return ", and ".join(result_phrases)
```

### Google Search Integration

The AI Assistant can perform Google searches to fetch up-to-date information:

```python
def google_search(query: str) -> str:
    global BROWSER_TYPE
    stop_spinner()
    print(f"{MAGENTA}Google search is: {query}{RESET}")
    encoded_query = quote_plus(query)
    url = f"https://www.google.com/search?q={encoded_query}"
    with sync_playwright() as p:
        browser = p.chromium.launch(headless=True, args=["--disable-blink-features=AutomationControlled"])
        if BROWSER_TYPE == 'chrome':
            context = browser.new_context(
                user_agent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 ..."
            )
        if BROWSER_TYPE == 'chromium':
            context = browser.new_context(
                user_agent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 ..."
            )
        page = context.new_page()
        page.goto(url)
        page.wait_for_load_state("networkidle")
        html = page.content()
        browser.close()
    soup = BeautifulSoup(html, 'html.parser')
    text = soup.get_text()
    cleaned_text = ' '.join(text.split())[0:5000]
    print(cleaned_text)
    return cleaned_text
```

---

## Advanced Usage

### Custom AI Model Integration

To integrate a custom AI model, add a new API call function and update the `ENGINE_MODELS` dictionary. For example:

```python
def call_custom_model(prompt: str, model_name: str) -> str:
    # Implement your custom model API call here
    # Example:
    response = requests.post(
        "https://api.custom-model.com/generate",
        json={"prompt": prompt, "model": model_name}
    )
    return response.json()["generated_text"]

# Add to ENGINE_MODELS
ENGINE_MODELS["CustomAI"] = ["custom-model-1", "custom-model-2"]

# Update call_current_engine
def call_current_engine(prompt: str, fresh: bool = False) -> str:
    global ENGINE, MODEL_ENGINE
    if ENGINE == "CustomAI":
        return call_custom_model(prompt, MODEL_ENGINE)
    elif ENGINE == "Ollama":
        return call_ollama(prompt, MODEL_ENGINE)
    # ... existing code for other engines ...
```

### Extending Functionality

To add new features or tools, create new functions and integrate them into the workflow. For example, to add a weather lookup feature:

```python
import requests

def weather_lookup(city: str) -> str:
    api_key = "your_weather_api_key"
    url = f"https://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}&units=metric"
    response = requests.get(url)
    data = response.json()
    if response.status_code == 200:
        temp
```

## Troubleshooting / Tips

### Browser/Web-Search related issues

If your ChromeDriver is proper for the version of Chrome/Chromium you are using in the paths, and you have the paths setup properly, and the code is actually getting triggered to run the web-search but it's returning errors, double check the UserAgent in the code and that no instance of Chrome or Chromium is running in the Task Manager (end all before running to verify). Also, use the profile you are setting to pull up the site manually via the browser, see if it let's you access the URL. Try using your main Chrome/Chromium profile info for the best results.



