# Privacy Policy — Okiff Chrome Extension

**Last updated:** 01/09/2026  

**Applies to:** the Okiff browser extension for Google Chrome, version 3.2.1 and later.

---

## In short

Okiff is an administration console for your organization's federated Infrastructure. It runs in your browser and talks to your ressources: the servers your organization operates on.

- **We receive nothing.** No data from the extension is sent to Okiff or to any third party. Every request goes to your organization's own ressources.
- **Nothing leaves your device except what you ask for.** Your sign-in session is stored locally in your browser. The only outbound requests are the ones needed to sign you in and to show you the screens you open.
- **The extension does not watch your browsing.** It has no access to the content of the web pages you visit, does not read your browsing history, and does not read your cookies.
- **No analytics, no tracking, no advertising.** The extension contains no analytics, telemetry, or advertising code of any kind.

The rest of this page explains each of those points in detail.

---

## 1. Who is responsible for your data

Okiff extension is  a front-end software. The identity data it displays and edits — user accounts, groups, roles, and application registrations — lives on **your organization's servers**, which your organization operates and controls.

- **Your organization** is the controller of that identity data. Its own privacy policy and data protection practices govern it. If you want to know how long your employer retains your account data, or you want your account deleted, that is a request to your organization, not to us.
- **[LEGAL ENTITY NAME]**, [COUNTRY], publishes the Okiff extension. We do not operate your identity server, we do not receive its data, and we have no access to the accounts you manage through the extension.

If your organization licenses Okiff from us, any separate agreement between us and your organization governs that relationship. This policy covers only what the browser extension itself does on your device.

---

## 2. What the extension stores on your device

All of the following is stored **locally in your browser profile** and is never transmitted to us.

| What | Where | Why |
|---|---|---|
| Session tokens — the access, refresh, and identity tokens issued by your identity server when you sign in | `chrome.storage.local` | So that closing and reopening the panel does not make you sign in again |
| The organization you signed in to, and its application identifier | Browser local storage | So the extension knows which organization your session belongs to |
| The last screen you were viewing | `chrome.storage.local` | So the panel reopens where you left off |
| Display preferences, such as theme and layout settings | Browser local storage | So the interface looks the way you set it |

**Please note:** browser extension storage is not encrypted at rest. It is protected by your operating system's user account and your browser profile, in the same way as the rest of your browser data. Anyone with access to your unlocked computer and your browser profile could read it. Sign out when you finish working on a shared or unattended machine.

---

## 3. What the extension sends, and to whom

The extension contacts exactly one destination: **your organization's servers**.

It sends requests there in order to:

- complete your sign-in, by exchanging the authorization code your identity server issues for a session;
- refresh your session when it is about to expire;
- end your session on the server when you sign out;
- read and write the data behind every screen you open — users, permission groups, applications, roles, scopes, and token mappings.

Every one of those requests carries your session token so the server can confirm who you are and what you are allowed to do. **The server decides what you may see and change.** The extension enforces nothing on its own; it displays what your account is authorized to access and nothing more.

No other host is contacted. There is no Okiff server in this picture, no third-party API, no content delivery network, and no analytics endpoint.

---

## 4. How you sign in

Okiff uses the OpenID, OAuth 2.0 or basic Auth authorization flows with PKCE — an industry-standard sign-in method — through self private built-in identity service.

When you sign in, Chrome opens your identity server's own login page in a separate window. **You type your password into your identity server's page, not into Okiff.** The extension never sees, receives, or stores your password. It receives only the session tokens your identity server issues afterwards.

---

## 5. What the extension does not do

We want to be specific, because browser extensions can do a great deal and this one deliberately does very little:

- It does **not** read, modify, or inject anything into the web pages you visit. It contains no content scripts.
- It does **not** read your browsing history.
- It does **not** read or modify your cookies.
- It does **not** record clicks, keystrokes, mouse movement, scrolling, or any other measure of your activity.
- It does **not** capture, store, or transmit passwords for any site.
- It does **not** contain analytics, telemetry, crash reporting, advertising, or tracking code.
- It does **not** sell, rent, or transfer your data to anyone. There is nobody to transfer it to.
- It does **not** use your data to assess creditworthiness or for lending purposes.

---

## 6. The browser permissions it asks for, and why

Chrome requires an extension to declare the capabilities it uses. Okiff asks for five, plus access to a single web address.

| Permission | What it is used for |
|---|---|
| `secret` | serves as the first app embedding key. You need approved captcha secret key from okiff marketplace. |
| `identity` | To sign you in to your organization's identity server through Chrome's own authentication window. No Google account information is requested or accessed. |
| `storage` | To keep your session and preferences on your device, as described in section 2. |
| `tabs` | To open an application you select. Before opening a new tab, the extension checks whether that application is already open so it can bring you to it instead of creating a duplicate. It reads no other tab, and no page content. |
| `sidePanel` | To display the console in Chrome's side panel, which is the extension's interface. |
| Access to your identity server's address | To make the requests described in section 3. This is the only address the extension is permitted to contact. |

We do not request permission to access all websites, to read your cookies, or to run scripts on pages you visit.

---

## 7. How long data is kept, and how to remove it

Everything the extension stores stays on your device until one of the following happens:

- **You sign out.** Your session tokens are deleted from your device, and the extension asks your identity server to end the session.
- **You remove the extension.** Chrome deletes all of its stored data.
- **You clear browsing data.** Clearing your browser's site data removes the extension's local storage.

Because we never receive your data, there is nothing for us to delete on our side. Requests concerning the account data held on your identity server — access, correction, deletion, export — go to your organization, which controls that server.

---

## 8. Your rights

Depending on where you live, you may have rights over your personal data, including the right to access it, correct it, delete it, restrict or object to its processing, and receive a copy of it.

Because the personal data involved here is held by your organization on its identity server, **direct those requests to your organization.** Its data protection contact can act on them; we cannot, as we hold no copy of that data.

If you believe the extension itself behaves differently from what this page describes, contact us at the address in section 11. You may also lodge a complaint with your local data protection authority.

---

## 9. Changes to this policy

If the extension's data practices change, we will update this page and change the "Last updated" date above. Material changes will be reflected in the extension's Chrome Web Store listing at the same time, because the store requires the two to agree.

---

## 10. Contact

Questions about this policy or about the extension's data handling:

**[LEGAL ENTITY NAME]**
[POSTAL ADDRESS]
[COUNTRY]

Email: **[privacy@okiff.com]**

---

*This page describes the data behaviour of the Okiff browser extension as implemented. It is not legal advice, and it does not replace review by your own counsel before publication.*
