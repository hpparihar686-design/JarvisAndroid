# JARVIS Android – Starter Project

यह Android source project है। यह अभी एक सुरक्षित starter assistant है, Iron Man जैसी unrestricted system access नहीं।

## इसमें क्या काम करता है
- Hindi speech-to-text (डिवाइस की speech recognition service पर निर्भर)
- Text-to-speech जवाब
- OpenAI-compatible cloud chat (आपकी अपनी API key जरूरी)
- सीमित स्थानीय commands: YouTube/WhatsApp/Camera/Settings खोलना, Google search, dialer खोलना, alarm app खोलना
- App foreground में खुला हो तो experimental "Hey Jarvis" listening mode

## जरूरी सीमाएँ
- **Hey Jarvis स्क्रीन बंद होने पर हमेशा नहीं सुनेगा।** Android background microphone restrictions और battery optimization के कारण यह starter केवल app खुला रहने पर सुनता है।
- यह फोन के हर ऐप, फोटो, संदेश, पासवर्ड या सिस्टम सेटिंग को अपने-आप नियंत्रित नहीं करता।
- कॉल कमांड केवल Dialer खोलती है; कॉल खुद नहीं लगाती। Alarm command alarm screen खोलती है।
- AI को API key और इंटरनेट चाहिए। API usage पर शुल्क लग सकता है।
- API key इस starter में app की private preferences में रखी जाती है, लेकिन rooted/compromised device पर इसे पूरी तरह सुरक्षित नहीं माना जा सकता। APK या key किसी से साझा न करें।

## फोन पर सेटअप
1. ZIP extract करें।
2. Android पर कोई compatible Android IDE इस्तेमाल करें जो Android Gradle Plugin 8.7.3 और Kotlin 2.0.21 support करता हो। या project को Android Studio वाले कंप्यूटर पर खोलें।
3. `JarvisAndroid` project folder खोलें और Gradle sync/build पूरा होने दें। पहली build में इंटरनेट चाहिए।
4. App install/run करें और Microphone permission दें।
5. अपनी OpenAI API key app में डालकर **Save API key** दबाएँ। API key कभी किसी अनजान व्यक्ति को न दें। API key और API billing अलग चीजें हैं।
6. **Speak command** दबाकर बोलें, या **Start 'Hey Jarvis' mode** दबाकर app खुला रखते हुए "Hey Jarvis" कहें।

## शुरुआती commands
- "Open YouTube"
- "Open WhatsApp"
- "Open camera"
- "Open settings"
- "Search weather in Jodhpur"
- "Call 9876543210" (सिर्फ dialer खुलेगा)
- "Set alarm" (alarm screen खुलेगी)
- सामान्य सवाल पूछें — cloud AI जवाब देगा।

## Build details
- Package: `com.example.jarvis`
- Min Android: 8.0 (API 26)
- Target/Compile SDK: 35
- No API key is embedded in source.
- Gradle wrapper शामिल नहीं है; IDE में installed Gradle/Android build support से project खोलें।
