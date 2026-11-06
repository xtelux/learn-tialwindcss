# learn-tialwindcss
belajar tailwind css


### Instalisasi
Buat folder pembelajaran Tailwind

#### 1. Inisialisasi project
```bash
npm init -y
```

#### 2. Install Tailwind CSS v4
```bash
npm install -D tailwindcss @tailwindcss/cli
```

Sekarang buat folder dan file berikut :
```text
belajar-tailwind/
│
├── node_modules/
│
├── src/
│   └── input.css
│
├── dist/
│   
│
├── konten/
│   └── index.html, file html
│
├── package.json
└── package-lock.json
```

Keterangan :
- src/input.css adalah CSS sumber yang akan diproses.
- dist/output.css adalah CSS hasil generate Tailwind.
- konten/index.html adalah halaman HTML tempat kita menggunakan utility class.

buka file src/input.css
```css
@import "tailwindcss";

@source "../konten";
```

konfigurasi paket package.json
```json
"scripts": {
  "dev": "npx @tailwindcss/cli -i ./src/input.css -o ./dist/output.css --watch",
  "build": "npx @tailwindcss/cli -i ./src/input.css -o ./dist/output.css --minify"
}
```


#### 3. Jalankan compiler
```bash
npm run dev
```

#### 4. Build untuk produksi
```bash
npm run build
```
