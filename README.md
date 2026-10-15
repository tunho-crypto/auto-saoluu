cat > README.md << 'EOF'
# NetAuto - Network Automation Platform

Hệ thống tự động hóa quản lý cấu hình thiết bị mạng đa vendor.

## ✨ Tính năng

- ✅ Sao lưu cấu hình tự động (scheduled + on-demand)
- ✅ Git-based versioning với SHA256 deduplication
- ✅ Phát hiện thay đổi cấu hình (config drift) với phân loại mức độ
- ✅ Khôi phục cấu hình an toàn (dry-run + auto-rollback)
- ✅ Giám sát hiệu năng (CPU, RAM, interface, BGP/OSPF)
- ✅ Cảnh báo qua Email/Slack/Telegram
- ✅ Hỗ trợ đa vendor: Cisco, Juniper, Huawei, Arista, Fortinet, Palo Alto, MikroTik

## 🚀 Quick Start

```bash
# Clone và setup
git clone <repo-url>
cd netauto
python -m venv .venv
source .venv/bin/activate  # Linux/Mac
pip install -e .

# Cấu hình
cp .env.example .env
# Edit .env với thông tin thực

# Chạy backup đầu tiên
netauto backup --device core-rtr-01