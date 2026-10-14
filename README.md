# FastST engine mirror

Kho dự phòng của engine ShardX (Chromium vá fingerprint), thư viện fingerprint và gói MCP server mà FastST Launcher dùng. Nguồn chính của launcher là CDN của ProxyShard; kho này chỉ được dùng tự động khi nguồn chính không truy cập được.

## Hai thế hệ launcher, hai manifest

| Launcher | Manifest | Tệp trong release mới nhất |
|---|---|---|
| FastST 2.x (Chromium 152+) | `v2/runtime.json`, bản sao nguyên văn manifest upstream ProxyShard/ShardBrowser | `ShardX-*.zip`, `ShardX-MCP.tar.gz` |
| FastST 0.x (Chromium 149, khách cũ) | `runtime.json` ở gốc, giữ nguyên bản 149 | `FastST-*.zip` (bản 149) |

Khách cũ vẫn tải được engine 149 cho đến khi cập nhật launcher lên 2.x; launcher 2.x sau đó tự nâng engine theo `v2/runtime.json`. Khi không còn khách 0.x, có thể bỏ `runtime.json` gốc và các tệp `FastST-*`.

`SHA256SUMS.txt` trong release là băm của các tệp đã tải từ CDN upstream. Đồng bộ bằng `scripts/engine-mirror/publish.ps1` trong kho FastST Launcher.
