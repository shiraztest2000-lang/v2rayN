<p align="center">
  <img src="assets/logo.png" alt="SHZv2rayN" width="180">
</p>

# SHZv2rayN

**A Windows-focused fork of [v2rayN](https://github.com/2dust/v2rayN), maintained by [@shiraztest2000-lang](https://github.com/shiraztest2000-lang).**

**فورک ویندوزی v2rayN** با تغییرات اختصاصی، نگهداری‌شده در حساب [@shiraztest2000-lang](https://github.com/shiraztest2000-lang).

[English](#english) · [فارسی](#فارسی)

---

## English

### About

SHZv2rayN is a customized fork of the open-source v2rayN client. It keeps the upstream application's core functionality while maintaining fork-specific changes and a Windows-only release pipeline.

- **Repository:** https://github.com/shiraztest2000-lang/v2rayN
- **Configured next release version:** `7.25.6.008` (release build pending)
- **Supported release platforms:** Windows x64 and Windows x86 (32-bit)
- **License:** GPL-3.0
- **First-run routing default:** Global

This repository is a fork of [2dust/v2rayN](https://github.com/2dust/v2rayN). It is not the official upstream project.

### Fork-specific changes

#### 1. Xray TLS — Allow Insecure option

- Restores a functional per-profile **Allow Insecure** setting for Xray TLS configurations.
- When enabled for a profile, the generated Xray configuration includes the corresponding `allowInsecure` option.
- For newly created Xray TLS profiles, Allow Insecure is enabled by default. Existing saved profiles keep their current setting.
- This fork-specific handling applies to **Xray** configurations. It does not change sing-box behavior.

**Security warning:** Enabling Allow Insecure disables normal TLS certificate verification for that connection and can expose the connection to man-in-the-middle attacks. Because this disables certificate verification and increases MITM risk, turn it off whenever it is not specifically required.

#### 2. Windows-only release packages

- Release workflow builds **Windows x64** and **Windows x86** packages.
- The extracted application folder is named `SHZv2rayN-7.25.6.008`.
- Each release is checked to contain exactly these two ZIP files:
  - `SHZv2rayN-7.25.6.008-windows-64.zip`
  - `SHZv2rayN-7.25.6.008-windows-86.zip`
- Linux and macOS client packages are not produced by this fork's release workflow.
- Release version input is validated against the project version before publishing.

### Download

Get the latest release and its files from this fork:

**[SHZv2rayN Releases](https://github.com/shiraztest2000-lang/v2rayN/releases)**

Current release: **7.25.6.008**

| Package | Architecture | Download |
| --- | --- | --- |
| Windows x64 | 64-bit | [SHZv2rayN-7.25.6.008-windows-64.zip](https://github.com/shiraztest2000-lang/v2rayN/releases) |
| Windows x86 | 32-bit | [SHZv2rayN-7.25.6.008-windows-86.zip](https://github.com/shiraztest2000-lang/v2rayN/releases) |

Choose the package that matches your Windows architecture. Extract the ZIP file to a writable folder and run `SHZv2rayN.exe`. Back up your configuration and profiles before replacing an existing installation.

### Basic usage

1. Download the x64 or x86 package from the Releases page.
2. Extract the archive.
3. Start `SHZv2rayN.exe`.
4. Import your own server profile, share link, QR code, or subscription.
5. Select a profile and connect using the application's system proxy or other supported network mode.

This project is a client application. It does **not** provide proxy servers, subscriptions, accounts, or connection credentials. You must provide your own.

### Documentation and links

- **This fork:** https://github.com/shiraztest2000-lang/v2rayN
- **Releases:** https://github.com/shiraztest2000-lang/v2rayN/releases
- **Actions / build status:** https://github.com/shiraztest2000-lang/v2rayN/actions
- **Source project:** https://github.com/2dust/v2rayN
- **Xray-core:** https://github.com/XTLS/Xray-core
- **sing-box:** https://github.com/SagerNet/sing-box
- **Upstream v2rayN Wiki:** https://github.com/2dust/v2rayN/wiki

The upstream Wiki describes the original v2rayN project. Fork-specific release behavior and changes are documented here and in this repository's release notes.

### Disclaimer

This is an independent community fork and is not affiliated with or endorsed by the upstream v2rayN maintainers. Product names and trademarks belong to their respective owners. Use the software and any security-sensitive options at your own risk.

---

## فارسی

### معرفی پروژه

**SHZv2rayN** نسخه‌ای سفارشی‌شده از پروژه متن‌باز v2rayN است. این فورک قابلیت‌های اصلی برنامه را حفظ می‌کند و در کنار آن، تغییرات اختصاصی و فرایند انتشار ویژه ویندوز را ارائه می‌دهد.

- **مخزن پروژه:** https://github.com/shiraztest2000-lang/v2rayN
- **نسخه تنظیم‌شده برای انتشار بعدی:** `7.25.6.008` (ساخت و انتشار در انتظار)
- **معماری‌های قابل دریافت:** ویندوز ۶۴ بیتی و ویندوز ۳۲ بیتی
- **مجوز:** GPL-3.0
- **مسیریابی پیش‌فرض در اجرای نخست:** Global

این مخزن فورکی از پروژه اصلی [2dust/v2rayN](https://github.com/2dust/v2rayN) است و نسخه رسمی توسعه‌دهندگان اصلی محسوب نمی‌شود.

### تغییرات اختصاصی این فورک

#### ۱. بازگردانی گزینه Allow Insecure برای TLS در Xray

- گزینه کاربردی **Allow Insecure** برای پروفایل‌های مبتنی بر TLS در Xray پشتیبانی می‌شود.
- با فعال‌کردن این گزینه برای یک پروفایل، مقدار مربوط به `allowInsecure` در پیکربندی تولیدشده Xray قرار می‌گیرد.
- در پروفایل‌های جدید Xray مبتنی بر TLS، این گزینه به‌صورت پیش‌فرض فعال است؛ تنظیم پروفایل‌های ذخیره‌شده قبلی تغییر نمی‌کند.
- این تغییر اختصاصی برای پیکربندی‌های **Xray** است و رفتار sing-box را تغییر نمی‌دهد.

**هشدار امنیتی:** فعال‌کردن Allow Insecure بررسی معمول گواهی TLS را برای آن اتصال غیرفعال می‌کند و می‌تواند خطر حمله مرد میانی (MITM) را افزایش دهد. اگر به این قابلیت نیاز ندارید، آن را غیرفعال کنید؛ زیرا بررسی گواهی TLS را خاموش کرده و خطر حمله مرد میانی (MITM) را افزایش می‌دهد.

#### ۲. انتشار نسخه مخصوص ویندوز

- فرایند انتشار، فایل‌های مخصوص **Windows x64** و **Windows x86** را می‌سازد.
- در پایان فرایند انتشار بررسی می‌شود که هر Release دقیقاً شامل دو فایل ZIP زیر باشد:
  - `SHZv2rayN-7.25.6.008-windows-64.zip`
  - `SHZv2rayN-7.25.6.008-windows-86.zip`
- پوشه برنامه پس از استخراج با نام `SHZv2rayN-7.25.6.008` ساخته می‌شود.
- در فرایند انتشار این فورک، نسخه‌های مخصوص Linux و macOS ساخته نمی‌شوند.
- پیش از انتشار، شماره نسخه واردشده با نسخه تعریف‌شده در پروژه تطبیق داده می‌شود.

### دانلود

برای دریافت آخرین نسخه، فقط از صفحه انتشار همین فورک استفاده کنید:

**[صفحه دانلود و Releaseهای SHZv2rayN](https://github.com/shiraztest2000-lang/v2rayN/releases)**

نسخه فعلی: **7.25.6.008**

| فایل | معماری | لینک دانلود |
| --- | --- | --- |
| Windows x64 | ویندوز ۶۴ بیتی | [دانلود نسخه ۶۴ بیتی](https://github.com/shiraztest2000-lang/v2rayN/releases/download/7.25.6.008/SHZv2rayN-7.25.6.008-windows-64.zip) |
| Windows x86 | ویندوز ۳۲ بیتی | [دانلود نسخه ۳۲ بیتی](https://github.com/shiraztest2000-lang/v2rayN/releases/download/7.25.6.008/SHZv2rayN-7.25.6.008-windows-86.zip) |

فایلی را دانلود کنید که با معماری ویندوز شما مطابقت دارد. فایل ZIP را در یک پوشه قابل‌نوشتن استخراج و سپس فایل `SHZv2rayN.exe` را اجرا کنید. پیش از جایگزین‌کردن نسخه قبلی، از تنظیمات و پروفایل‌های خود نسخه پشتیبان تهیه کنید.

### راهنمای شروع سریع

۱. از صفحه Releases نسخه ۶۴ یا ۳۲ بیتی متناسب با ویندوز خود را دریافت کنید.

۲. فایل ZIP را استخراج کنید.

۳. فایل `SHZv2rayN.exe` را اجرا کنید.

۴. پروفایل سرور، لینک اشتراک، کد QR یا Subscription متعلق به خودتان را وارد کنید.

۵. یک پروفایل را انتخاب و از طریق System Proxy یا سایر حالت‌های پشتیبانی‌شده برنامه متصل شوید.

این نرم‌افزار صرفاً یک **کلاینت** است و هیچ سرور پروکسی، اشتراک، حساب کاربری یا اطلاعات اتصال آماده‌ای ارائه نمی‌کند. تهیه اطلاعات اتصال بر عهده کاربر است.

### مستندات و لینک‌های رسمی

- **مخزن همین فورک:** https://github.com/shiraztest2000-lang/v2rayN
- **دانلود نسخه‌ها:** https://github.com/shiraztest2000-lang/v2rayN/releases
- **وضعیت ساخت و Workflowها:** https://github.com/shiraztest2000-lang/v2rayN/actions
- **پروژه اصلی:** https://github.com/2dust/v2rayN
- **مخزن Xray-core:** https://github.com/XTLS/Xray-core
- **مخزن sing-box:** https://github.com/SagerNet/sing-box
- **ویکی پروژه اصلی v2rayN:** https://github.com/2dust/v2rayN/wiki

ویکی پروژه اصلی، راهنمای نسخه upstream است. تغییرات اختصاصی و روش انتشار این فورک در همین README و توضیحات Releaseهای این مخزن درج می‌شود.

### سلب مسئولیت

این پروژه یک فورک مستقل و جامعه‌محور است و وابستگی یا تأیید رسمی از سوی توسعه‌دهندگان اصلی v2rayN ندارد. نام‌ها و علائم تجاری متعلق به صاحبان مربوطه هستند. استفاده از نرم‌افزار و گزینه‌های حساس امنیتی بر عهده کاربر است.
