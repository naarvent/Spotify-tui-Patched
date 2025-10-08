## 0.25.0-patched (2025-10-08)
- Vendorized chrono 0.4.37 and patched derive for ustc-serialize (Windows/MSVC).
- Pinned socket2 = 0.3.19 for compatibility with 	okio 0.2.
- Added ClientConfig::get_redirect_uri() and fixes in src/config.rs.
- OAuth instructions: use http://127.0.0.1:8888/callback.
- Build tested on Windows with stable Rust.
