# AI Browser for Rokid glasses

A hands‑free web browser for **Rokid AI Glasses (RV101)** — TV‑remote controls on the glasses, voice commands, and a remote control page on your phone.

*Trình duyệt web rảnh tay cho **kính Rokid AI (RV101)** — điều khiển kiểu remote TV ngay trên kính, ra lệnh bằng giọng nói, và trang điều khiển trên điện thoại.*

> **Download / Tải về:** see **[Releases](https://github.com/ThienMLP/rokid-browser/releases/latest)** → `rokid-browser-<version>.apk`
>
> Source code will be published once the app is complete. · *Mã nguồn sẽ được công bố khi app hoàn thiện.*

---

## Features · Tính năng

- **TV‑remote controls** — swipe the temple touch strip to move a highlighted selection, tap (or press the temple button) = OK, double‑tap = Back, hold the button = talk to the assistant.
  *Điều khiển kiểu remote TV — vuốt bàn di trên gọng để chuyển khung chọn, chạm (hoặc bấm nút thái dương) = OK, chạm 2 lần = Quay lại, giữ nút = nói với trợ lý.*
- **Voice commands** in English or Vietnamese — "open youtube", "search …", "scroll down", "pause", "go back", "louder"… Anything more complex goes to a Gemini AI assistant that can read and operate web pages.
  *Lệnh giọng nói tiếng Anh hoặc tiếng Việt — "mở youtube", "tìm …", "cuộn xuống", "tạm dừng", "quay lại", "to lên"… Việc phức tạp hơn do trợ lý AI Gemini đọc và thao tác trang web.*
- **Phone remote** — open `http://rokid.local:8765` on a phone on the same Wi‑Fi: address bar, AI assistant, video controls, touchpad, live view of the glasses. No app to install on the phone.
  *Điều khiển từ điện thoại — mở `http://rokid.local:8765` trên điện thoại cùng Wi‑Fi: thanh địa chỉ, trợ lý AI, điều khiển video, bàn di, xem màn hình kính. Không cần cài app trên điện thoại.*
- **English / Vietnamese interface** — the **VI | EN** button at the top of the phone page.
  *Giao diện tiếng Anh / tiếng Việt — nút **VI | EN** trên cùng trang điện thoại.*

## Install · Cài đặt

**Option A — Hi Rokid app (no cable)** · *Cách A — app Hi Rokid (không cần cáp)*
1. Download the APK from **Releases** to your phone. · *Tải APK ở mục Releases về điện thoại.*
2. Hi Rokid → **Toolbox** → **Glasses app management** → install the APK. · *Hi Rokid → Hộp công cụ → Quản lý ứng dụng kính → cài APK.*

**Option B — ADB** (developer mode + debug cable) · *Cách B — ADB (bật chế độ nhà phát triển + cáp debug)*
```bash
adb install -r rokid-browser-1.46.0.apk
```

## First use · Dùng lần đầu

1. Put the glasses and your phone on the same Wi‑Fi (the phone's hotspot also works). · *Cho kính và điện thoại chung Wi‑Fi (hoặc bắt hotspot của điện thoại).*
2. On the glasses: open **AI Browser** → select the cast button (bottom‑right) → **START REMOTE**. · *Trên kính: mở AI Browser → chọn nút cast (góc dưới phải) → BẮT ĐẦU ĐIỀU KHIỂN.*
3. On the phone open `http://rokid.local:8765` (or the IP shown on the glasses). · *Trên điện thoại mở `http://rokid.local:8765` (hoặc địa chỉ IP hiện trên kính).*
4. For voice & the AI assistant, paste your own **Gemini API key** in *⚙ Settings → AI assistant*. It is stored on the glasses only. Get a key at [aistudio.google.com](https://aistudio.google.com/apikey).
   *Để dùng giọng nói & trợ lý AI, dán **khoá API Gemini** của bạn ở ⚙ Cài đặt → Trợ lý AI. Khoá chỉ lưu trên kính.*
5. A page misbehaves (a video won't play…)? Turn on *⚙ Settings → Diagnostics → Record web page errors*, reopen the page, then open *Connection log*: it lists the requests that failed or came back empty. Addresses and error codes only; it turns itself off after 30 minutes.
   *Trang bị lỗi (video không phát…)? Bật ⚙ Cài đặt → Chẩn đoán → Ghi lỗi trang web, mở lại trang, rồi mở Nhật ký kết nối: thấy ngay yêu cầu nào hỏng hoặc trả về rỗng. Chỉ ghi địa chỉ và mã lỗi; tự tắt sau 30 phút.*

## Privacy · Quyền riêng tư

The app has no account and no server of its own. The phone remote talks to the glasses directly over your local network. Voice and AI features send audio/text to Google Gemini using **your** API key.

*App không có tài khoản, không có máy chủ riêng. Trang điện thoại nói chuyện thẳng với kính trong mạng nội bộ. Giọng nói và trợ lý AI gửi âm thanh/chữ tới Google Gemini bằng khoá API **của bạn**.*

## Credits · Nguồn gốc

Based on [xnohat/rokid-glass-browser](https://github.com/xnohat/rokid-glass-browser) by Hong Phuc Nguyen (xnohat), MIT License.

Modifications by Van Thien Nguyen ([ThienMLP](https://github.com/ThienMLP)).

Not affiliated with or endorsed by Rokid. "Rokid" is a trademark of its owner. · *Không liên kết và không được Rokid bảo trợ.*

## License

MIT — see [LICENSE](LICENSE).
