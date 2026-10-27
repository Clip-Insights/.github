<div align="center">

# Clip Insights

### Turn learning videos into notes you can keep.

Capture the moments that matter, understand the content with AI, and build a personal library of study notes.

[Website](https://clipinsights.org) · [Web app](https://app.clipinsights.org) · [Chrome extension](https://chromewebstore.google.com/detail/ccgechmifoecebnimnccgahnoklklilj) · [Architecture](https://github.com/Clip-Insights/.github/blob/main/docs/ARCHITECTURE.md)

</div>

## What is Clip Insights?

Clip Insights is an AI-assisted learning tool for YouTube videos. A browser extension brings timestamped screenshots, notes, summaries, and a conversational assistant into the video page. Learners can export their work as a PDF and organize saved documents in a web dashboard.

The project combines natural language processing, retrieval-augmented generation (RAG), browser integration, and a shared backend. It was developed as a final year project for the BS in Data Science at the University of the Punjab, Lahore.

## Explore the source

| Repository | Purpose | Built with |
| --- | --- | --- |
| [chrome-extension](https://github.com/Clip-Insights/chrome-extension) | The study workspace on video pages: screenshots, notes, AI insights, chat, and PDF export. | React, TypeScript, Vite, Manifest V3 |
| [web-app](https://github.com/Clip-Insights/web-app) | The account dashboard for saved PDFs, folders, storage usage, and plans. | React, JavaScript, Vite, Tailwind CSS |
| [backend](https://github.com/Clip-Insights/backend) | The shared API for authentication, AI processing, retrieval, file storage, and usage limits. | Python, Django, Django REST Framework |
| [main-site](https://github.com/Clip-Insights/main-site) | The public website, product guides, articles, and information pages. | Next.js, TypeScript, Velite |

Each repository includes its own setup instructions. Start with the [system architecture](https://github.com/Clip-Insights/.github/blob/main/docs/ARCHITECTURE.md) for an overview of the components and data flow.

## A learning session

1. Open a YouTube video and use the Clip Insights study panel.
2. Capture screenshots and write notes linked to moments in the video.
3. Generate a summary and key points, or ask questions about the transcript.
4. Export a PDF to keep locally, or save it to your account.
5. Open the web app to find and organize your saved documents.

## How the system fits together

![Clip Insights system overview](./docs/diagrams/system-overview.svg)

The extension keeps working notes and screenshots in the browser. The backend generates AI insights and handles account services; saved PDFs live in object storage and appear in the web app. The public website provides information and guides independently of the authenticated tools.

## AI grounded in the video

Summaries and key points are generated from the video transcript. For chat, the backend divides the transcript into chunks, stores their embeddings, and retrieves the three most relevant chunks for each question. Those excerpts and recent conversation history provide context for a streamed answer.

AI services are configured through a provider registry, with Fireworks AI and Google Gemini available for language-model generation. The [architecture guide](https://github.com/Clip-Insights/.github/blob/main/docs/ARCHITECTURE.md#video-question-answering) explains retrieval, caching, and fallback behavior.

## Read the implementation

| Area | Entry point |
| --- | --- |
| Extension architecture and platform adapters | [Extension architecture](https://github.com/Clip-Insights/chrome-extension/blob/main/ARCHITECTURE.md) |
| API modules, providers, and retrieval | [Backend architecture](https://github.com/Clip-Insights/backend/blob/main/ARCHITECTURE.md) |
| Dashboard routing and authentication | [Web app architecture](https://github.com/Clip-Insights/web-app/blob/main/ARCHITECTURE.md) |
| Local setup and verification | The README in each repository |

## Academic background

**BS in Data Science, 2021–2025**

Faculty of Computing & Information Technology, University of the Punjab, Lahore

**Supervisor:** Prof. Dr. Kamran Malik

**Project team:** Muhammad Zubair, Anas Waleed Tahir, Abdullah Ashfaq, Abdullah Ghazi, and Etisam Ul Haq.

For questions about the project, open an issue in the relevant repository or contact [zubayrahmad0308@gmail.com](mailto:zubayrahmad0308@gmail.com).
