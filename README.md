# Next.js Documentation

## File Structure

Next.js loyihasida fayl va papkalar tartibi juda muhim. App Router’da sahifalar `src/app` papkasi ichida yaratiladi.

```txt
src/
  app/
    page.tsx
    layout.tsx
    about/
      page.tsx
    signin/
      page.tsx
```

Bu strukturada har bir `page.tsx` fayli alohida sahifani bildiradi.

---

## Layouts and Pages

Next.js’da `page.tsx` va `layout.tsx` fayllari asosiy rol o‘ynaydi.

### `page.tsx`

`page.tsx` — bu route uchun asosiy sahifa fayli.

Masalan:

```txt
src/app/page.tsx
```

Bu fayl quyidagi route’ga mos keladi:

```txt
/
```

Yana bir misol:

```txt
src/app/about/page.tsx
```

Bu fayl quyidagi route’ga mos keladi:

```txt
/about
```

### `layout.tsx`

`layout.tsx` — sahifalar uchun umumiy layout yaratadi. Masalan, header, footer yoki umumiy dizayn elementlarini shu fayl orqali barcha sahifalarda ishlatish mumkin.

```tsx
export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body>
        <header>Header</header>
        {children}
        <footer>Footer</footer>
      </body>
    </html>
  );
}
```

Bu yerda `children` har bir sahifaning kontentini bildiradi.

---

## Next.js nima?

Next.js — React ustiga qurilgan zamonaviy full-stack framework. U React imkoniyatlarini kengaytiradi va web ilovalar yaratish uchun routing, server-side rendering, API routes, layouts va deployment kabi tayyor imkoniyatlarni beradi.

Oddiy React’da sahifalar orasida yurish uchun odatda `react-router-dom` kabi kutubxona o‘rnatiladi. Next.js’da esa routing tizimi tayyor keladi.

---

## File-Based Routing

Next.js’da route yaratish uchun alohida router yozish shart emas. Sahifa yaratish uchun `src/app` papkasi ichida kerakli folder va `page.tsx` faylini yaratish kifoya.

Misollar:

```txt
src/app/page.tsx          → /
src/app/about/page.tsx    → /about
src/app/signin/page.tsx   → /signin
```

Masalan, `about` sahifasini yaratish:

```tsx
export default function AboutPage() {
  return <h1>About Page</h1>;
}
```

Fayl joylashuvi:

```txt
src/app/about/page.tsx
```

Natijada sahifa quyidagi URL orqali ochiladi:

```txt
http://localhost:3000/about
```

---

## React va Next.js farqi

React asosan foydalanuvchi interfeysini yaratish uchun ishlatiladi. Next.js esa React asosida qurilgan framework bo‘lib, katta web ilovalar uchun kerakli ko‘plab imkoniyatlarni tayyor holda beradi.

| React                         | Next.js                      |
| ----------------------------- | ---------------------------- |
| UI yaratish uchun kutubxona   | Full-stack framework         |
| Routing alohida sozlanadi     | File-based routing tayyor    |
| Backend qismi yo‘q            | API routes mavjud            |
| SSR alohida sozlanadi         | Server-side rendering mavjud |
| Layout tizimi qo‘lda qilinadi | Layout system tayyor         |

---

## Next.js’ning asosiy ustunliklari

Next.js quyidagi imkoniyatlarni tayyor holatda beradi:

* File-based routing
* Layout system
* Server-side rendering
* API routes
* SEO uchun qulay tuzilma
* Static va dynamic page yaratish
* Full-stack app yaratish imkoniyati
* Vercel orqali oson deployment

---


Qisqa qilib aytganda:

```txt
React  → UI yaratish uchun
Next.js → To‘liq web application yaratish uchun
```



## Edge Runtime
Last updated February 2, 2026
Next.js has two server runtimes you can use in your application:

The Node.js Runtime (default), which has access to all Node.js APIs and is used for rendering your application.
The Edge Runtime which contains a more limited set of APIs, used in Proxy.
