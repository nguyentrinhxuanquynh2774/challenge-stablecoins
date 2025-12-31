# ĐỒ ÁN CHALLENGE 6: DECENTRALIZED STABLECOIN

## Introduction

Dự án này là lời giải cho **Challenge 6: Stablecoins** thuộc hệ sinh thái **SpeedRunEthereum**.  
Bài tập tập trung vào việc xây dựng một **stablecoin phi tập trung**, được phát hành dựa trên **tài sản thế chấp (collateral)** và cơ chế **over-collateralization** nhằm đảm bảo giá trị ổn định.

Stablecoin trong dự án được phát hành dưới dạng **ERC20 token (MyUSD)**, có thể được mint và burn dựa trên giá trị tài sản thế chấp mà người dùng gửi vào smart contract.

### Các tính năng đã hoàn thành
- **Deposit Collateral:** Cho phép người dùng gửi tài sản thế chấp vào smart contract.
- **Mint Stablecoin:** Phát hành token MyUSD dựa trên giá trị collateral và tỷ lệ thế chấp an toàn.
- **Burn Stablecoin:** Người dùng có thể đốt MyUSD để giảm nợ và rút collateral.
- **Theo dõi tỷ lệ thế chấp:** Smart contract kiểm tra collateral ratio để đảm bảo an toàn hệ thống.
- **Liquidation:** Tự động cho phép thanh lý vị thế nếu collateral giảm giá và không còn đủ an toàn.
- **On-chain Price Logic:** Toàn bộ logic tính toán đều được xử lý trực tiếp trên blockchain, không phụ thuộc frontend.

---

## Yêu cầu môi trường 

Để chạy dự án, máy tính cần cài đặt:
- **NodeJS** (v16.x hoặc mới hơn)
- **Yarn** (khuyến nghị)
- **Git**
- **Trình duyệt Chrome**
- **Ví MetaMask**

---

## Hướng dẫn chạy 

Mở **3 cửa sổ Terminal riêng biệt** và chạy các lệnh sau theo đúng thứ tự.

### Bước 1: Cài đặt thư viện và chạy Blockchain cục bộ (Hardhat Node)
```bash
yarn install
yarn chain
```
### Bước 3: Triển khai Smart Contract lên Localhost
```bash
yarn deploy
```
### Bước 4: Khởi chạy giao diện người dùng (Frontend)
```bash
yarn start
```
### Bước 5: Truy cập: http://localhost:3000 để tương tác.

## ⚙️ Cấu hình mạng & Triển khai (Deployment)

---

### Môi trường (Local)

- Dự án được cấu hình mặc định chạy trên **Hardhat local blockchain**.
- Cấu hình này nằm trong file `scaffold.config.ts`:

```ts
targetNetworks: [chains.hardhat]




