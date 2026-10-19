# data-gw

Koleksi aset tema Discord dan media pribadi milik **Raxxel**, untuk kustomisasi melalui Vencord.

## Isi repo

- [Pain.jpg](./Pain.jpg) — gambar untuk ikon Home Discord.
- [output.gif](./output.gif) — GIF animasi untuk ikon Home Discord.

Nama dan lokasi kedua file dipertahankan agar link yang sudah dipakai tidak berubah.

## Link langsung

Gunakan URL raw untuk gambar di CSS:

- **Gambar:** `https://raw.githubusercontent.com/Raxxel/data-gw/main/Pain.jpg`
- **GIF:** `https://raw.githubusercontent.com/Raxxel/data-gw/main/output.gif`

## Contoh pemakaian di Vencord

Buka **Settings -> Vencord -> Open QuickCSS**, lalu tempel kode berikut secara manual:

```css
/* Ganti artwork Home tanpa mengubah ikon server */
[data-list-item-id="guildsnav___home"] > [class*="childWrapper__"] {
  position: relative;
  overflow: hidden;
}

[data-list-item-id="guildsnav___home"] > [class*="childWrapper__"] > * {
  visibility: hidden !important;
}

[data-list-item-id="guildsnav___home"] > [class*="childWrapper__"]::before {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: inherit;
  background: url("https://raw.githubusercontent.com/Raxxel/data-gw/main/output.gif") center / cover no-repeat;
  pointer-events: none;
}
```

Untuk memakai gambar statis, ganti `output.gif` dengan `Pain.jpg`.

## Catatan

- Repo ini publik: jangan unggah token, password, atau data pribadi sensitif.
- Jangan ubah nama file yang sedang aktif agar tautan di CSS tidak putus.
