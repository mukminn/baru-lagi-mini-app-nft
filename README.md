# Unified Fee NFT Mini App

Mini aplikasi web lengkap untuk NFT minting dengan sistem fees terpadu menggunakan UnifiedFeeContract.

## 🚀 Fitur

### ✨ Mint NFT
- **Mint Single NFT** dengan ETH atau USDC
- **Batch Mint NFT** dengan ETH atau USDC
- Auto-approve USDC sebelum minting
- Validasi input dan error handling

### 📊 Dashboard
- Statistik lengkap (Total Supply, Max Supply, Progress Bar)
- Total Fees terkumpul (ETH & USDC)
- Contract Balance
- Harga mint saat ini
- Status minting (Aktif/Nonaktif)
- Statistik user (fees yang sudah dibayar)

### 🖼️ NFT Saya
- Lihat semua NFT yang dimiliki
- Load metadata otomatis dari IPFS
- Tampilkan gambar, nama, deskripsi, dan atribut
- Link ke token URI

### 👑 Owner Panel
- **Withdraw Fees**: ETH, USDC, atau semua sekaligus
- **Toggle Minting**: Aktifkan/nonaktifkan minting
- **Update Harga**: Set harga mint untuk ETH dan USDC
- **Owner Mint**: Mint NFT gratis untuk airdrop
- **Kelola Token URI**: 
  - Set Token URI (single)
  - Batch Set Token URI
  - Set Base URI

## 🎨 Design

- **Tema**: Biru langit (Sky Blue)
- **Framework**: Next.js 14 dengan App Router
- **Styling**: Tailwind CSS dengan custom theme
- **Responsif**: Mobile & Desktop friendly
- **UI/UX**: Modern dengan animasi dan transisi

## 🛠️ Tech Stack

- **Frontend**: Next.js 14, React 18, TypeScript
- **Web3**: Wagmi v2, Viem
- **Styling**: Tailwind CSS
- **Icons**: Lucide React

## 📦 Instalasi

```bash
npm install
```

## ⚙️ Konfigurasi

Buat file `.env.local` di root:

```env
NEXT_PUBLIC_CONTRACT_ADDRESS=0x...
NEXT_PUBLIC_USDC_ADDRESS=0x...
NEXT_PUBLIC_CHAIN_ID=8453
```

## 🚀 Menjalankan

```bash
npm run dev
```

Aplikasi akan berjalan di http://localhost:3000

## 📁 Struktur Project

```
.
├── app/              # Next.js App Router
│   ├── globals.css   # Global styles dengan tema biru langit
│   ├── layout.tsx    # Root layout
│   ├── page.tsx      # Halaman utama
│   └── providers.tsx # Web3 providers (Wagmi)
├── components/       # React components
│   ├── Dashboard.tsx      # Dashboard dengan statistik
│   ├── Header.tsx         # Header dengan wallet connection
│   ├── MintForms.tsx      # Form untuk mint NFT
│   ├── MintSection.tsx    # Section mint dengan toggle
│   ├── MyNFTs.tsx         # Komponen untuk melihat NFT
│   └── OwnerPanel.tsx     # Panel admin untuk owner
└── lib/              # Utilities
    ├── config.ts     # Konfigurasi contract
    └── contract.ts   # Contract ABI
```

## 🚀 Deploy ke Vercel

1. **Import project dari GitHub:**
   - Buka https://vercel.com
   - Klik "New Project"
   - Import repository: `mukminn/baru-lagi-mini-app-nft`

2. **Environment Variables:**
   - Tambahkan di Vercel dashboard:
     - `NEXT_PUBLIC_CONTRACT_ADDRESS`
     - `NEXT_PUBLIC_USDC_ADDRESS`
     - `NEXT_PUBLIC_CHAIN_ID`

3. **Deploy:**
   - Vercel akan otomatis detect Next.js
   - Build command: `npm run build`
   - Deploy otomatis setiap push ke main branch

## 🔗 Links

- **Repository**: https://github.com/mukminn/baru-lagi-mini-app-nft
- **Contract**: UnifiedFeeContract.sol

## 📝 License

MIT
