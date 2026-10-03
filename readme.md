# **How to Create and Host Your Personal Daily Dashboard**

A complete step-by-step guide for creating, personalizing, and hosting your own single-page dark-mode productivity dashboard with news briefings, school assignments, homework tracking, interactive to-dos, and custom themes.

# **1\. Overview of the Dashboard**

The dashboard is a self-contained, single-file web application (`index.html`) featuring:

* **Glassmorphism Dark Mode Design**: High-contrast, clean aesthetic with customizable accent glows.  
* **Interactive Background**: Starry particle canvas reacting to mouse interaction.  
* **Daily Briefing**: Curated Tech & AI and World News feeds with search and live refresh.  
* **School & Homework Hub**: Due date countdowns, priority levels, and subject filtering.  
* **Interactive To-Do List**: Categorized tags, status filters, and drag-and-drop task reordering.  
* **Local Persistence**: Automatic browser saving via localStorage plus JSON backup export/import.  
* **Optional PIN Lock**: Privacy protection modal.

# **2\. The Customization Prompt**

Copy the prompt below, edit the customizable fields at the very top, and run it in an AI assistant (Google Gemini, ChatGPT, or Claude):

\#\#\# CUSTOMIZATION SETTINGS (Edit these before running)

\- \*\*YOUR\_NAME\*\*: "Alex" \<\!-- Your name displayed in the header greeting \--\>

\- \*\*ACCENT\_THEME\*\*: "Crimson Red" \<\!-- E.g., Crimson Red, Emerald Green, Indigo Blue, Violet Purple, Cyberpunk Amber \--\>

\- \*\*PRIMARY\_HEX\*\*: "\#ef4444" \<\!-- Main accent color hex code for glows, buttons, and borders \--\>

\- \*\*SECONDARY\_HEX\*\*: "\#e11d48" \<\!-- Secondary accent color for gradients and hover states \--\>

\- \*\*SUBJECTS\_OR\_CLASSES\*\*: \["AP Computer Science", "Calculus BC", "Physics", "English Literature", "Personal Projects"\]

\- \*\*SECURITY\_PIN\*\*: "None" \<\!-- Set a 4-digit PIN (e.g., "1234") to require unlocking on launch, or "None" to disable \--\>

\- \*\*BACKGROUND\_EFFECT\*\*: "Interactive Starfield" \<\!-- Options: "Interactive Starfield", "Ambient Glow", "Clean Minimal Dark" \--\>

\---

\#\#\# PROMPT INSTRUCTIONS FOR THE AI:

Please generate a complete, standalone, single-file HTML web application (\`dashboard.html\`) for a personal daily productivity dashboard using the customization settings defined above. The code must bundle all HTML, CSS (\`\<style\>\`), and JavaScript (\`\<script\>\`) into one file with zero external build tools or server dependencies so it can run directly in any web browser.

\#\#\#\# Design & Aesthetics:

1\. \*\*Glassmorphism Dark Mode\*\*:

   \- Deep dark base background (\`\#080305\` or dark palette matching the accent).

   \- Semi-transparent glass cards (\`backdrop-filter: blur(16px)\` with subtle borders and card drop-shadows).

   \- Use CSS custom properties in \`:root\` driven by \`PRIMARY\_HEX\` and \`SECONDARY\_HEX\` for active borders, buttons, badges, and glow effects.

2\. \*\*Interactive Background Canvas\*\*:

   \- If \`BACKGROUND\_EFFECT\` is "Interactive Starfield", render an interactive HTML5 \`\<canvas\>\` background with twinkling stars and gentle parallax reaction to mouse movement.

3\. \*\*Typography & Layout\*\*:

   \- Modern sans-serif font stack with clean spacing, micro-interactions, smooth hover transitions, and responsive grid layout.

\#\#\#\# Core Features & Modules:

1\. \*\*Header & Motivational Bar\*\*:

   \- Personalized greeting using \`YOUR\_NAME\` (e.g., "Welcome back, \[YOUR\_NAME\]").

   \- Live digital clock updating every second and formatted calendar date.

   \- Daily check-in streak counter (persisted across sessions).

   \- Real-time progress bar reflecting daily completed tasks and homework, paired with dynamic motivational quotes.

   \- If \`SECURITY\_PIN\` is configured, include a secure lock screen overlay modal that asks for the PIN on launch or when manually locked.

2\. \*\*School / Project Assignment Hub\*\*:

   \- Track assignments filtered by the custom \`SUBJECTS\_OR\_CLASSES\`.

   \- Fields: Title, Subject, Due Date/Time, Priority (High, Medium, Low), and Status (Not Started, In Progress, Completed).

   \- Dynamic urgency badges: "Due Soon (\<24h)" with glowing alert badge, "Upcoming (\<48h)", and "Overdue".

   \- Filtering by subject and status.

3\. \*\*Interactive Task & To-Do Manager\*\*:

   \- Full task management: Add, inline edit, delete, and toggle completion.

   \- Categorization tags (e.g., School, Personal, Work, Projects).

   \- Views: "Today", "Upcoming", "Completed", and "All".

   \- HTML5 drag-and-drop reordering for tasks.

4\. \*\*Daily Briefing & News Feed\*\*:

   \- Dual-tab news interface (e.g., "Tech & AI" and "World News").

   \- Headline cards with summary text, source metadata, and direct external links.

   \- Search/filter bar and a "Refresh News" button fetching live Hacker News top stories with fallback curated feeds.

5\. \*\*Local Persistence & Data Management\*\*:

   \- Automatically save all tasks, assignments, streaks, and settings to browser \`localStorage\`.

   \- Settings modal with options to export data to a JSON backup file and import previously saved JSON backups.

Please output the complete, fully implemented, and ready-to-run HTML code inside a single markdown code block without placeholders or truncated sections.

# **3\. How to Generate and Save the Website**

1. **Paste into an AI**: Open [Google Gemini](https://gemini.google.com), ChatGPT, or Claude. Paste the customized prompt and hit enter.  
2. **Copy the Output**: The AI will provide a complete code block starting with `<!DOCTYPE html>`. Click the **Copy** button on the code snippet.  
3. **Save as a File**:  
   * Open a text editor like **VS Code**, **Notepad** (Windows), or **TextEdit** (Mac; make sure TextEdit is set to Plain Text mode via `Format > Make Plain Text`).  
   * Paste the code into the editor.  
   * Save the file with the exact name **`index.html`**.  
4. **Test it Locally**: Double-click `index.html` on your computer. It will immediately open in Google Chrome, Safari, Edge, or Firefox. Everything works offline and saves locally.

# **4\. How to Host It Online for Free**

To access your dashboard from your phone, laptop, school computer, or anywhere on the web, choose one of these free hosting options:

## **Option A: GitHub Pages (Recommended — Permanent & Custom URL)**

1. Go to [GitHub](https://github.com) and sign up or log in.  
2. Click the **\+** icon in the top-right corner and select **New repository**.  
3. Name your repository (e.g., `my-dashboard`) and make sure it is set to **Public**. Click **Create repository**.  
4. Click **Upload an existing file**, drag your `index.html` file into the box, and click **Commit changes**.  
5. Go to the repository **Settings** tab (gear icon at the top).  
6. In the left sidebar, click **Pages**.  
7. Under **Build and deployment \> Branch**, select `main` (or `master`) and `/root`, then click **Save**.  
8. Wait 1–2 minutes. Refresh the page to see your live URL: `https://<your-username>.github.io/my-dashboard/`.

## **Option B: Netlify Drop (Easiest — 30 Seconds, No Code or Command Line)**

1. Place your `index.html` file into an empty folder on your desktop (name the folder anything, e.g., `dashboard-site`).  
2. Open your browser and navigate to [Netlify Drop](https://app.netlify.com/drop).  
3. Drag and drop the folder into the designated area.  
4. Netlify will instantly deploy your site and provide a live URL (e.g., `https://brave-curie-12345.netlify.app`).  
5. (Optional) Create a free account to change the site name to something personalized (e.g., `alex-dashboard.netlify.app`).

## **Option C: Vercel**

1. Create a free account at [Vercel](https://vercel.com).  
2. Install the Vercel desktop app or drag-and-drop the project folder, or link your GitHub repository.  
3. Vercel will build and assign a free `.vercel.app` production link.

# **5\. Important Tips for Friends Using the Dashboard**

* **Browser Storage (localStorage)**: All tasks, homework assignments, check-in streaks, and completed items are stored directly in your browser's local storage. This means your data remains private and will persist whenever you revisit your URL in the same browser.  
* **Backing Up Data**: Always use the **Export Backup** button in the dashboard settings to download a `.json` file periodically. If you ever switch computers or clear your browser cache, you can click **Import Backup** to restore everything in one second.  
* **Mobile Friendly**: The layout is responsive. On iPhone or Android, you can open your live website in Safari/Chrome and select **Add to Home Screen** to use the dashboard like a native app.

