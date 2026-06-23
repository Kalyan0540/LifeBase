---
type: source
source_title: "App Store Approval Checklist"
source_url: ""
raw_path: "raw/knowledge/technology/ai/App Store Approval Checklist.md"
created: 2026-06-16
updated: 2026-06-18
---

<aside> 💡

**How to use this template:**

**The 2026 Vibe Coding Crackdown:** Between March and May 2026, Apple launched a massive enforcement wave, completely banning or freezing updates for major AI building platforms like **Replit**, **Vibecode**, and **Anything**.

Apple used **Guideline 2.5.2 (Executable Code)** to target these platforms because they allowed users to build apps from text prompts and run a live preview inside the mobile app itself. Apple considers unreviewed, dynamically generated code running on a phone to be a massive security risk.

**What this means for you:** While Apple banned the _creator tools_ themselves, they are now reviewing any app built _by_ AI with a magnifying glass. Automated bots are instantly pre-rejecting apps that have sloppy layouts, hidden bugs, or security vulnerabilities (like leaking your private AI keys into the code).

As a vibe coder, your code's origin doesn't matter to Apple—but **security, stability, and data privacy do.** If you use the Claude Code + Expo cloud build pipeline (eas build) and tick off every item on this checklist, your app will bypass the automated blocks and sail straight through human review on the first try.

</aside>

## 🔐 1. Hiding Your Money & Secrets

- [ ] **1. Clear Frontend Code of Database Master Keys:** Your database password or master keys (like SUPABASE_SERVICE_ROLE_KEY or admin tokens) must never sit anywhere in your layout files. Make sure Claude processes database edits via a secure backend rather than directly inside the mobile app.
- [ ] **2. Isolate Private Third-Party API Keys:** Look through your files or ask Claude: _"Are any of our private API tokens (like Anthropic, OpenAI, or tracking keys) written in plain text inside files like App.js?"_ They must be isolated in a secure .env environment file on a separate server layer. If a bad actor unpacks your live app bundle and finds exposed keys, they can run up a massive bill on your credit card.

## 📱 2. Passing the "Dynamic Code Execution" Test (Guideline 2.5.2)

- [ ] **3. Remove Any In-App Code Previews or Editors:** Ensure your application does not feature an interior terminal, a script compiler, or an interactive window that lets users execute unreviewed code blocks post-approval.
- [ ] **4. Build via Isolated Cloud Compiles Only:** Ensure your entire production codebase is bundled into a finished, self-contained app profile using your cloud pipeline via eas build. Because your output is static native code, it completely bypasses the automated dynamic script flags that got platforms like Replit blocked.

## 🧩 3. Stability & Professional Polish (Guideline 2.1)

- [ ] **5. Pass the "No Wi-Fi" Mobile Stress Test:** Turn off your phone’s Wi-Fi and mobile data completely, launch your app, and try to trigger your core feature (like scanning a coin). If the app crashes, freezes, or goes entirely white, Apple will reject it. Ensure Claude adds a clean "network fallback error" popup that reads: _"Connection lost. Please check your internet and try again."_
- [ ] **6. Clean Out the AI Developer Leftovers:** Search your codebase files for leftover placeholder elements like Lorem Ipsum, TODO: fix this later, or generic blank graphics. Reviewers scan apps for these exact strings to catch sloppy AI mockups.
- [ ] **7. Organize Your Code Modules Properly:** Check that Claude hasn't lumped your entire app into one giant, confusing single-file script. Ask it to organize your logic into clean, modular folders (Components, Navigation, Hooks). This stops your token processing costs from exploding when making minor edits down the line.

## 🔒 4. AI Rules & Transparency (Guideline 5.1.2)

- [ ] **8. Add a Mandatory AI Consent Screen:** Before a user triggers their very first AI scan or prompt, you must display an onboarding message or popup. It must explicitly name the AI provider you use and get consent.
    - _What to tell Claude:_ _"Create a clear popup screen that runs on the first app launch. It must state: 'Coin Vault uses Anthropic Claude AI to analyze your imagery. By hitting continue, you agree to securely share your photo with our AI processing partner.'"_
- [ ] **9. Embed the Privacy Policy Inside the App Menu:** Don't just paste your privacy web link into Apple's online dashboard. You must place a clickable link or button right inside your app’s native Settings or Profile screen.
- [ ] **10. Write an Explicit AI Data Disclaimer:** Your privacy policy documentation must explicitly state in plain language that user-uploaded files are transmitted to an external AI vendor (like Anthropic or OpenAI) for live classification.
- [ ] **11. Provide a Native "Delete Account" Button:** If your app forces users to register an account with an email login, Apple strictly requires a clear button inside the profile menu that reads **"Delete Account."** You are no longer allowed to make users email customer support to delete their data.

## 💰 5. App Store Payment Rules (Guideline 3.1.1)

- [ ] **12. Force Native Apple In-App Purchases (No Stripe on Mobile):** For premium digital content or monthly tiers inside an iOS app, you cannot use web credit card links or standard Stripe forms. You must configure Apple’s native payment system. (Asking Claude to use a helper tool like _RevenueCat_ makes setting this up painless).
- [ ] **13. Include a "Restore Purchases" Link:** You must place a visible button right on your paywall or subscription screen that says **"Restore Purchases."** This ensures that if a user deletes the app or upgrades their iPhone, they can retrieve their paid membership status instantly without paying twice.

## 📦 6. Packaging & SDK Compliance

- [ ] **14. Target the Latest required Apple SDK Version:** Because you are bypassing local Xcode apps via Expo cloud servers, ensure your configuration coordinates match the modern App Store standard. Tell Claude Code: _"Please look at our app.json profile and ensure our Expo SDK framework targets the latest required Apple deployment version."_
- [ ] **15. Verify Third-Party Privacy Manifests:** Even if your custom code is safe, any free utility plugin Claude finds on the web (for charting, custom animations, or tracking data) can get you blocked. Ask Claude: _"Scan our integrated packages and dependencies. Make sure everything is updated to the latest version containing an approved Apple Privacy Manifest (PrivacyInfo.xcprivacy)."_
- [ ] **16. Run the 44-Point Tap-Target Design Check:** Ensure every clickable interface button, link, or menu icon has a minimum dimension of **44x44 points**. If a human reviewer struggles to tap your navigation tools because they are too small or crowded, they will issue a layout rejection.

## 👤 7. Beating the Reviewer Queue Bots

- [ ] **17. Provide an Active Demo Guest Account:** When completing your details inside App Store Connect, you must fill out the "App Review Notes" box with a pre-registered, working test username and password so the reviewer can bypass your signup screens instantly.
- [ ] **18. Include a Private Explainer Screen Recording Link:** Because backend AI calls can take a few seconds to parse, a reviewer might assume a spinning load wheel means the app is broken. Record a quick, unedited 30-second video of your app scanning an item successfully on your phone, upload it as an unlisted link, and paste it into your Reviewer Notes along with an explanation of your processing times.
