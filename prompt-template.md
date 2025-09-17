# Code Generation

Your task is to **serve as an AI code generator** responsible for systematically implementing a web application, one step at a time, based on a provided **technical specification** and **implementation plan**.

You will:

1. Identify which step in the plan is next.
2. Write or modify the code files necessary for that specific step.
3. Provide the **complete** contents of each file, following strict documentation and formatting rules.

---

## **Required Inputs**

1. **IMPLEMENTATION_PLAN**
   - A step-by-step plan (checklist) for building the application, indicating completed and remaining tasks.
2. **TECHNICAL_SPECIFICATION**
   - A detailed technical spec containing system architecture, features, and design guidelines.
3. **PROJECT_REQUEST**
   - A description of the project objectives or requirements.

---

## **Optional Inputs**

1. **PROJECT_RULES**
   - Any constraints, conventions, or “rules” you must follow.
2. **EXISTING_CODE**
   - Any existing codebase or partial implementation.

---

## **Task Overview**

When this prompt runs, you will:

1. **Review** the provided inputs (Project Request, Rules, Spec, Plan, Code).
2. **Identify** the next incomplete step in the **IMPLEMENTATION_PLAN** (marked `- [ ]`).
3. **Generate** all the code required to fulfill that step.
   - Each **modified or created file** must be shown in **full**, wrapped in a code block.
   - Precede each file with “Here’s what I did and why:” to explain your changes.
4. **Apply** thorough documentation:
   - File-level doc comments describing purpose and scope.
   - Function-level doc comments detailing inputs, outputs, and logic flow.
   - Inline comments explaining complex logic or edge cases.
   - Type definitions and error handling as needed.
5. **End** with:
   - **“STEP X COMPLETE. Here’s what I did and why:”** summarizing changes globally.
   - **“USER INSTRUCTIONS:”** specifying any manual tasks (e.g., installing libraries).
   - If you **update** the plan, return the modified steps in a **code block**.

Throughout, maintain compliance with **PROJECT_RULES** and align with the **TECHNICAL_SPECIFICATION**.

---

## **Detailed Process Outline**

1. **Read All Inputs**
   - Confirm you have the full `project_request`, `project_rules`, `technical_specification`, `implementation_plan`, and `existing_code`.
2. **Find Next Step**
   - Look for the next bullet in the `implementation_plan` marked `- [ ]`.
3. **Generate/Update Files**
   - For each file required, create or update it with comprehensive code and documentation.
   - Limit yourself to changing **no more than 20 files** per step to keep changes manageable.
4. **Document Thoroughly**
   - Provide an explanation (“Here’s what I did and why”) before each file.
   - Output complete file contents in a Markdown code block.
5. **Finalize**
   - End with “STEP X COMPLETE” summary.
   - Provide any **USER INSTRUCTIONS** for manual tasks.
   - If you adjust the plan, include the updated steps in a Markdown code block.

---

## **Output Template**

Below is an example of how your output should look once you **implement** the next step:

```markdown
STEP X COMPLETE. Here's what I did and why:
- [Summarize the changes made across all files.]
- [Note any crucial details or known issues.]

USER INSTRUCTIONS: Please do the following:
1. [Manual task #1, e.g., install library or environment variable config]
2. [Manual task #2, e.g., run migration or set up .env file]
```

If you updated the implementation plan, record it here:

```markdown
# Updated Implementation Plan

## [Section Name]
- [x] Step 1: [Completed or updated step with notes]
- [ ] Step 2: [Still pending]
```

---

## **Appendix: Design Principles**

### Context-Driven Design Philosophy

The fundamental principle underlying these guidelines is **context-driven design differentiation**. Rather than applying a one-size-fits-all approach, the design strategy adapts to the specific purpose and constraints of each project type. This creates optimal user experiences by aligning visual choices with functional requirements and user expectations.

### Complex Applications: Function-First Design

For complex applications like Three.js scenes, games, and simulations, performance isn't just a consideration—it's the foundation upon which all other decisions rest. This means:

- **Target 60 fps:** `requestAnimationFrame`, object pooling, LOD, and regular profiling.
- **Memory:** dispose of unused assets, choose lean data structures, off-load heavy work to Web Workers.
- **Rendering:** batch draws, instanced geometry, frustum culling, lightweight shaders/textures.

#### User Experience Clarity

Complex applications require **cognitive load reduction** through thoughtful interface design:

- Clear hierarchies, progressive disclosure, consistent spacing.
- Instant feedback, accessible controls, debounced rapid inputs.
- Error-proof defaults, undo/redo, descriptive messages.

#### Functional Design Language

The visual design should **support rather than compete** with functionality:

- Neutral palettes, legible type, supportive icons.
- Responsive, space-efficient layouts; collapsible panels; multi-monitor awareness.

### Presentational Content: Emotion-First Design

For landing pages, marketing sites, and presentational content, the goal shifts to **emotional engagement and memorability**:

- **3-second hook:** bold visuals, smooth entry motion.
- Story-driven flow with strategic “delight” moments.
- Hierarchies and CTAs tested for conversion.

#### Contemporary Aesthetics

##### Trend Anticipation

Rather than following trends, aim to **anticipate and set them**:

- Study emerging design patterns from leading agencies and startups
- Experiment with new CSS features as they become available
- Incorporate elements from other design disciplines (architecture, fashion, industrial design)
- Balance innovation with usability principles

##### Visual Sophistication

- Use advanced CSS features like custom properties, grid, and container queries
- Implement complex animations using CSS transforms and keyframes
- Create custom SVG illustrations that align with brand identity
- Develop unique color palettes that evoke specific emotions

### Interactive Design

#### Animation as Communication

Animations should serve **functional and emotional purposes** simultaneously:

- Motion clarifies loading, transitions, and hovers; micro-interactions add personality.
- Prefer transform-based animations, judicious `will-change`, and “reduce motion” support.

#### Interactive Elements

##### Hover State Philosophy

Every interactive element should provide **clear feedback** about its functionality:

- Subtle scale or color changes for clickable elements
- Revealing additional information on hover
- Smooth transitions that feel natural and responsive
- Consistent behavior patterns across similar elements

##### Touch and Mobile Considerations

- Design for finger-friendly touch targets (minimum 44px)
- Implement appropriate touch gestures for different actions
- Consider haptic feedback where available
- Ensure hover effects translate meaningfully to touch interfaces

### Technology Boundary Pushing

#### Advanced CSS

##### Modern Layout Systems

- CSS Grid for complex, two-dimensional layouts
- Flexbox for one-dimensional alignment and distribution
- Container queries for truly responsive component design
- CSS custom properties for dynamic theming and state management

##### Visual Effects Innovation

- CSS filters and backdrop-filter for sophisticated visual effects
- Transform3d for hardware-accelerated animations
- CSS shapes for non-rectangular layouts
- Blend modes for creative color and texture combinations

##### Cutting-Edge Features

- CSS scroll-snap for controlled scrolling experiences
- CSS logical properties for internationalization
- CSS aspect-ratio for consistent proportions
- CSS clamp() for fluid typography and spacing

#### JavaScript Interaction

##### Event Handling Sophistication

- Implement gesture recognition for touch interfaces
- Use Intersection Observer for scroll-based animations
- Create custom event systems for component communication
- Implement keyboard navigation patterns for accessibility

##### State Management

- Design reactive systems that update UI based on data changes
- Implement efficient re-rendering strategies
- Use debouncing and throttling for performance optimization
- Create predictable state transitions for complex interactions

### Accessibility Integration

#### Universal Design

Accessibility shouldn't be an afterthought but **integrated into the design process** from the beginning:

WCAG-AA contrast, multi-cue interactivity, visible focus, keyboard paths, skip links, minimal cognitive load.

#### Semantic Structure & Progressive Enhancement

Semantic HTML headings, ARIA where needed, labeled forms.
Base experience works without JS; enhancements layered and tested with assistive tech.

### Quality, Scalability & Future-Proofing

- Clean, documented code; descriptive commits; version control.
- Cross-browser/device testing and analytics-driven iteration.
- Modular architecture, design tokens, readiness for new standards with graceful degradation.

This comprehensive approach to design principles creates a framework for making informed decisions that serve both users and business objectives while pushing the boundaries of what's possible in web design and development.

---

## **Context**

<implementation_plan>
# Implementation Plan

> **Package manager:** **npm (≥ v9)** with native work-spaces.  
> All workspace-specific commands are executed with  
> `npm run <script> --workspace <package>`.

---

## 1 Repository & Tooling
- [ ] **Step 1.1 Init mono-repo**
  - **Task**: `git init`, root `package.json` with `"workspaces"`.
  - **Files**  
    - `package.json`  
      ```jsonc
      {
        "private": true,
        "workspaces": ["frontend", "worker", "packages/*", "scripts"],
        "scripts": {
          "bootstrap": "npm install",
          "lint": "eslint . --ext .ts,.tsx",
          "test": "npm run test --workspaces"
        }
      }
      ```
  - **Dependencies**: None
  - **User Instructions**: Make sure Node ≥ 18 & npm ≥ 9 are installed, then run `npm run bootstrap`.

- [ ] **Step 1.2 Configure TypeScript & linting**
  - **Task**: Shared `tsconfig.base.json`, ESLint + Prettier, Husky pre-commit hook.
  - **Files**:  
    - `tsconfig.base.json`  
    - `.eslintrc.cjs`  
    - `.prettierrc`  
    - `.husky/*` (set up via `npx husky-init && npm install`)
  - **Dependencies**: Step 1.1

---

## 2 Cloudflare Basics
- [ ] **Step 2.1 Wrangler config**
  - **Task**: `wrangler.toml` with `dev`, `staging`, `production` envs; D1 & Images bindings.
  - **Files**: `wrangler.toml`
  - **Dependencies**: Step 1.2
  - **User Instructions**: Fill real CF account IDs & tokens later.

- [ ] **Step 2.2 Hello-World Worker**
  - **Task**: Create **workspace** `worker`:
    ```bash
    mkdir -p worker && cd worker && npm init -y
    ```
    Add `/worker/index.ts` responding `{ ok: true }`; build script using esbuild.
  - **Files**:  
    - `worker/package.json` (scripts: `dev`, `build`)  
    - `worker/index.ts`  
    - `worker/bindings.d.ts`
  - **Dependencies**: Step 2.1
  - **User Instructions**: `npm run dev --workspace worker` opens http://localhost:8787.

---

## 3 Database & Migrations
- [ ] **Step 3.1 Initial schema migration**
  - **Task**: `/worker/migrations/001_init.sql` defining `posts`, `tags`, `post_tags`.
  - **Files**: `worker/migrations/001_init.sql`
  - **Dependencies**: Step 2.2
  - **User Instructions**: `npx wrangler d1 migrations apply gm_dev`.

- [ ] **Step 3.2 DB utility layer**
  - **Task**: `packages/db` workspace (`npm init -y`) exporting typed queries via `@cfql/client`.
  - **Files**:  
    - `packages/db/index.ts`  
    - `packages/types/post.ts`
  - **Dependencies**: Step 3.1

---

## 4 Frontend Skeleton
- [ ] **Step 4.1 Create Vite React app**
  - **Task**: `npm create vite@latest frontend -- --template react-ts`; install Mantine, Lexend font, set yellow theme.
  - **Files**: ≤15 under `/frontend`.
  - **Dependencies**: Step 1.2
  - **User Instructions**: `npm run dev --workspace frontend`.

- [ ] **Step 4.2 Routing & Layout**
  - **Task**: Add React Router, `MainLayout`, placeholder pages (`Index`, `Tag`, `Post`, `Admin`).
  - **Files**:  
    - `/frontend/src/pages/*`  
    - `/frontend/src/App.tsx`
  - **Dependencies**: Step 4.1

---

## 5 State & Networking
- [ ] **Step 5.1 zustand stores & fetch client**
  - **Task**: `api/client.ts` (fetch wrapper), `postsSlice`, `tagsSlice`.
  - **Files**:  
    - `/frontend/src/store/index.ts`  
    - `/frontend/src/api/client.ts`
  - **Dependencies**: Step 4.2

---

## 6 Public API
- [ ] **Step 6.1 GET endpoints**
  - **Task**: `/worker/api/posts.ts`, `/worker/api/tags.ts` with Hono, Zod, edge caching.
  - **Files**: 4 under `/worker/api`.
  - **Dependencies**: Step 3.2

- [ ] **Step 6.2 Fetch hooks & PostCard**
  - **Task**: `usePosts`, `PostCard` with `<img srcSet>`.
  - **Files**:  
    - `/frontend/src/hooks/usePosts.ts`  
    - `/frontend/src/components/PostCard.tsx`
  - **Dependencies**: Step 6.1

---

## 7 Infinite Index & Tag Page
- [ ] **Step 7.1 react-virtuoso index**
  - **Task**: Infinite list, “Back to top” FAB.
  - **Files**:  
    - `/frontend/src/pages/Index.tsx`  
    - `/frontend/src/components/BackToTop.tsx`
  - **Dependencies**: Step 6.2

- [ ] **Step 7.2 Tag page**
  - **Task**: `/frontend/src/pages/Tag.tsx` reuse hook; 404 fallback.
  - **Files**: 1–2 modified.
  - **Dependencies**: Step 7.1

---

## 8 Permalink, SSR & Meta
- [ ] **Step 8.1 SSR HTML for single post**
  - **Task**: Worker template + OG meta.
  - **Files**:  
    - `/worker/templates/post.html`  
    - `/worker/api/renderPost.ts`
  - **Dependencies**: Step 6.1

- [ ] **Step 8.2 CSR hydration**
  - **Task**: `/frontend/src/pages/Post.tsx` centered layout.
  - **Files**: 1 modified
  - **Dependencies**: Step 8.1

---

## 9 Cloudflare Images
- [ ] **Step 9.1 Utility functions**
  - **Task**: `/packages/utils/cfImages.ts` with `getVariantUrl`, signed upload.
  - **Files**: 1 util
  - **Dependencies**: Step 6.1

---

## 10 Admin Authentication
- [ ] **Step 10.1 Access JWT middleware**
  - **Task**: `/worker/middleware/auth.ts`.
  - **Files**: 1
  - **Dependencies**: Step 2.2

- [ ] **Step 10.2 Route guard on front-end**
  - **Task**: `<AuthGate>` + lazy-loaded admin bundle.
  - **Files**: 2–3
  - **Dependencies**: Step 10.1

---

## 11 Admin CRUD
- [ ] **Step 11.1 POST/PUT/DELETE endpoints**
  - **Task**: Extend `/worker/api/posts.ts` with mutations + tag upsert.
  - **Files**: ≤3
  - **Dependencies**: Step 10.1

- [ ] **Step 11.2 Mantine DataTable**
  - **Task**: `AdminPostsTable` with pagination + filters.
  - **Files**: several under `/frontend/src/pages/admin`
  - **Dependencies**: Step 11.1

- [ ] **Step 11.3 CRUD modals & Dropzone**
  - **Task**: `PostModal` (Formik + Zod) with signed upload.
  - **Files**: 2 components
  - **Dependencies**: Step 9.1

---

## 12 Bulk Ops (optional)
- [ ] **Step 12.1 Multi-delete & tag ops**
  - **Task**: API + UI batch actions.
  - **Files**: extend ≤4 files
  - **Dependencies**: Step 11.2

---

## 13 Import CLI
- [ ] **Step 13.1 scripts/import.ts**
  - **Task**: Stream JSON dump, upload images, insert rows.
  - **Files**: `/scripts/import.ts`, `scripts/package.json`
  - **Dependencies**: Steps 3.2, 9.1
  - **User Instructions**: `npx ts-node scripts/import.ts --dump ./dump.json --images ./images`.

---

## 14 RSS & Sitemap
- [ ] **Step 14.1 XML generators**
  - **Task**: `/worker/api/rss.ts`, `/worker/api/sitemap.ts`.
  - **Files**: 2
  - **Dependencies**: Step 6.1

---

## 15 Analytics & Monitoring
- [ ] **Step 15.1 Plausible script & hook**
  - **Task**: Add `<script>` in `frontend/index.html`, `useTrackEvent`.
  - **Files**: 2
  - **Dependencies**: Step 4.1

- [ ] **Step 15.2 Logpush + Sentry**
  - **Task**: README snippet, `@sentry/react` installation.
  - **Files**: README, 1 config
  - **Dependencies**: Step 15.1

---

## 16 Testing
- [ ] **Step 16.1 Vitest setup**
  - **Task**: `vitest.config.ts`, sample db util test.
  - **Files**: 2
  - **Dependencies**: Step 3.2

- [ ] **Step 16.2 Playwright scenarios**
  - **Task**: E2E tests for public flow + admin CRUD.
  - **Files**: `/tests/e2e/*.spec.ts`
  - **Dependencies**: Step 11.2

- [ ] **Step 16.3 Lighthouse-CI budget**
  - **Task**: `lighthouserc.js`, GH Action step.
  - **Files**: 2
  - **Dependencies**: Step 14.1

---

## 17 CI/CD & Deployment
- [ ] **Step 17.1 GitHub Actions**
  - **Task**: `.github/workflows/ci.yml` (lint, test, build), `.github/workflows/deploy.yml` (wrangler pages deploy).
  - **Files**: 2 workflows
  - **Dependencies**: Steps 16.*

- [ ] **Step 17.2 Secrets & Pages project**
  - **Task**: README guide + `scripts/set-secrets.sh`.
  - **Files**: README update, `scripts/set-secrets.sh`
  - **Dependencies**: Step 17.1
  - **User Instructions**: Run script; configure CF Pages in dashboard.

---

## 18 Polish & Documentation
- [ ] **Step 18.1 Accessibility sweep**
  - **Task**: Run axe; fix color contrast or aria labels.
  - **Files**: minor tweaks (<5)
  - **Dependencies**: Steps 7–8

- [ ] **Step 18.2 Final docs & governance**
  - **Task**: Finish `README.md`, add `CODEOWNERS`, LICENSE.
  - **Files**: 3
  - **Dependencies**: All prior

---

### Summary

* Workspaces declared in root `package.json`.
* Commands use `npm run … --workspace <pkg>` and `npm install` for bootstrapping.
* One-off scripts executed with `npx`, e.g. `npx ts-node …`.

Follow steps sequentially; each touches ≤20 files and isolates concerns, enabling a code-generation AI (or human developers) to implement the micro-blog efficiently on the Cloudflare stack.
</implementation_plan>

<technical_specification>
# Tumblr — Technical Specification (New Project)

## 1. System Overview
| Item | Detail |
|------|--------|
| **Core Purpose** | A personal micro-blog that reproduces the feel of Tumblr for a single author, optimized for thousands of image-heavy posts and smooth infinite scrolling. |
| **Primary Goals** | • Zero-friction posting and management for the author<br>• Fast, mobile-first consumption for visitors<br>• Low-ops, CDN-backed delivery using Cloudflare edge platform |
| **Primary Use-Cases** | 1. Author signs in via Google, creates or edits a post with an image and tags.<br>2. Visitor lands on the index, scrolls endlessly through GIFs without jank.<br>3. Visitor clicks a tag to view a filtered timeline.<br>4. RSS consumers poll `/rss.xml` for latest entries. |
| **High-Level Architecture** | **Client** (React + Mantine) delivered from **Cloudflare Pages** → `fetch()` calls to **Cloudflare Worker API**. Worker connects to **D1** (SQLite) and **Cloudflare Images**. Assets cached at Cloudflare edge. Plausible script loaded on every page. |

```

Client (Vite → Pages) ──▶ Worker API ──▶ D1
▲                  │
│                  └─▶ Cloudflare Images (variants)
└── Plausible (analytics endpoint)

```

---

## 2. Technology & Tools
| Layer | Stack |
|-------|-------|
| **Languages** | TypeScript 5.x (strict), SQL (D1), Bash |
| **Frontend** | React 18, Mantine 7, Vite 5, React Router v6, zustand (state) |
| **Backend** | Cloudflare Workers (Service Workers API), Hono v4 (router), Zod (runtime validation) |
| **Database** | Cloudflare D1 (SQLite) accessed via `@cfql/client` |
| **Media** | Cloudflare Images (`1x1xs`, `1x1sm`, `1x1md`, `1x1lg`, `1x1xl`) |
| **DevOps** | GitHub + GitHub Actions, Wrangler v3, npm, Conventional Commits, Semantic-release |
| **CI/CD** | PR lint + unit tests → preview deploy to Pages preview env; merge to `main` → staging; tag `v*` → prod |
| **Testing** | Vitest (unit), Playwright (E2E), Lighthouse-CI (perf), tsc `--noEmit` |
| **Observability** | Cloudflare Logpush (API requests), Sentry (client errors), Plausible (usage) |

---

## 3. Project Structure
```

/frontend
/src
/components
/pages
/hooks
/styles
vite.config.ts
/worker
/api
posts.ts
tags.ts
auth.ts
bindings.d.ts
wrangler.toml
/scripts
import.ts
/packages
/types  # shared DTOs & Zod schemas
/utils
.eslintrc.cjs
.prettierrc
npm-workspace.yaml

````
- **Naming** · kebab-case filenames, Pascal components, `useX` hooks.  
- **Path Aliasing** · `@/components`, `@/types` via `tsconfig.paths`.  

---

## 4. Feature Specification

### 4.1 Public Frontend
| Requirement | Implementation Detail | Edge Cases / Errors | UX |
|-------------|----------------------|---------------------|----|
| Infinite-Scroll Index | `react-virtuoso` list; fetch `/api/posts?cursor=<id>` (50 posts) | Network fail → toast “Offline – retrying” | “Back to top” FAB appears after 3× viewport |
| Tag Page | Same component with `/api/posts?tag=<slug>&cursor=…` | Tag not found → 404 page | Title bar shows `#<tag>` |
| Permalink | SSR: Worker renders HTML w/ OG meta; CSR hydration | Post ID missing → 404 | Centered 640 px column |
| RSS & Sitemap | Worker routes `/rss.xml`, `/sitemap.xml` (edge-cached) | n/a | n/a |
| OG/Twitter Meta | `<meta property="og:image" content="https://imagedelivery.net/<hash>/cf_image_id/1x1lg">` | Animated GIFs auto-play preview disabled by specifying `content-type` gif | n/a |

### 4.2 Admin UI
| Requirement | Details | Edge Cases |
|-------------|---------|-----------|
| Auth | Cloudflare Access (Google) → `CF_Authorization` header forwarded to Worker; Worker verifies JWT via Access public keys | Token expired → redirect to Access login |
| Post Table | Mantine `DataTable` w/ server-side pagination (`page`, `size`) | Empty list shows “No posts yet” |
| CRUD Modal | Formik + Zod schema: `description` (markdown textarea), `image` (Dropzone), `tags` (multi-select) | Missing image → validation error |
| Bulk Ops | Checkbox column; actions “Delete”, “Add Tag”, “Remove Tag” | Confirm modal; cascade delete ensures `post_tags` rows removed |

### 4.3 Import CLI
- **Usage:** `npm ts-node scripts/import.ts --dump ./dump.json --images ./images`
- **Steps:**  
  1. Read JSON, iterate posts.  
  2. Upload each local image ⇒ Cloudflare Images; record returned `id` + variants URL list.  
  3. Insert into D1 with `title = NULL`.  
  4. Upsert tags, populate `post_tags`.  
- **Performance:** Stream-based reading; concurrent uploads limited to 10.

---

## 5. Database Schema

```sql
-- posts
CREATE TABLE posts (
  id            INTEGER PRIMARY KEY AUTOINCREMENT,
  title         TEXT,            -- nullable; shown as "(untitled)" if NULL
  description   TEXT NOT NULL,
  cf_image_id   TEXT NOT NULL UNIQUE,
  cf_variants   TEXT NOT NULL,   -- JSON string mapping size→URL
  tumblr_url    TEXT,
  tags_count    INTEGER DEFAULT 0,
  created_at    DATETIME DEFAULT CURRENT_TIMESTAMP,
  updated_at    DATETIME DEFAULT CURRENT_TIMESTAMP
);
CREATE INDEX idx_posts_created ON posts(created_at DESC);

-- tags
CREATE TABLE tags (
  id    INTEGER PRIMARY KEY AUTOINCREMENT,
  name  TEXT NOT NULL UNIQUE
);

-- post_tags (M2M)
CREATE TABLE post_tags (
  post_id INTEGER NOT NULL REFERENCES posts(id) ON DELETE CASCADE,
  tag_id  INTEGER NOT NULL REFERENCES tags(id)  ON DELETE CASCADE,
  PRIMARY KEY (post_id, tag_id)
);
CREATE INDEX idx_post_tags_tag ON post_tags(tag_id);
````

Migrations managed via `wrangler d1 migrations apply`.

---

## 6. Server Actions

### 6.1 REST Endpoints (Hono)

| Method | Path             | Auth   | Description                          |
| ------ | ---------------- | ------ | ------------------------------------ |
| GET    | `/api/posts`     | Public | Params: `cursor`, `size=50`, `tag?`  |
| GET    | `/api/posts/:id` | Public | Single post                          |
| GET    | `/api/tags`      | Public | List all tags + counts               |
| POST   | `/api/post`      | Admin  | Body: `description, imageId, tags[]` |
| PUT    | `/api/post/:id`  | Admin  | Update                               |
| DELETE | `/api/post/:id`  | Admin  | Remove                               |

* **Caching:** Public GETs wrapped with `caches.default.match/put` (5 min, SWR 10 min).
* **Validation:** Zod schema per route; errors → `400 JSON {error}`.

### 6.2 Other Backend Logic

* **Image Upload Proxy:** Signed URL from Worker → client uploads direct to Cloudflare Images.
* **Edge Redirect (optional):** If request path matches scraped Tumblr slug, return 301 to `/post/:id` (feature-flag).
* **Scheduled Cleanup:** Cron triggers weekly to purge orphaned images (not referenced in `posts`).

---

## 7. Design System

### 7.1 Visual Style

| Token         | Value                         |
| ------------- | ----------------------------- |
| Primary BG    | `#FFE627`                     |
| Primary Text  | `#1A1A1A`                     |
| Font Family   | `"Lexend", sans-serif`        |
| Radius        | `8 px`                        |
| Spacing Scale | `4 px · 8 px · 16 px · 32 px` |

### 7.2 UI Components

| Component   | States                           |
| ----------- | -------------------------------- |
| Button      | default, hover, focus, disabled  |
| Card (Post) | idle, hover (lift), focus-within |
| Tag Chip    | default, selected                |
| Dialog      | open/close, error shake          |

All components built on Mantine primitives; custom styles via Mantine `createStyles`.

---

## 8. Component Architecture

### 8.1 Backend

```
┌──────────────────────────┐
│  Hono Router (Worker)    │
├──────────────┬───────────┤
│ Controllers  │ /api/...  │
│ Services     │ DB logic  │
│ Lib          │ cf-images │
└──────────────┴───────────┘
```

### 8.2 Frontend

* **State Layer:** zustand store `postsSlice`, `tagsSlice`, `uiSlice`.
* **Routes:** `/` (index), `/tag/:slug`, `/post/:id`, `/admin/*` (lazy).
* **Code-Splitting:** `React.lazy` for Admin bundle.
* **Types:** Shared DTOs in `@gm/types`.

---

## 9. Authentication & Authorization

* **Flow:**

  1. `/admin` → Cloudflare Access Google OAuth.
  2. On success, browser receives `CF_Authorization` cookie.
  3. Worker validates JWT on each admin request using Access JWKS.
* **Roles:** `admin` (single email allow-list). All other traffic is anonymous.
* **Session Length:** 24 h; forced re-auth thereafter.

---

## 10. Data Flow

1. **Index Load** → Client SSR fallback HTML from Worker (empty list).
2. Hydration → React fetches first batch `/api/posts`.
3. Scroll event threshold triggers next fetch with `cursor` (last id).
4. Images load via `srcset` (browser picks variant).
5. Plausible event `post_view` fires via IntersectionObserver when post 50 % visible.

---

## 11. Payment Integration

*Not applicable.*

---

## 12. Analytics Integration

* **Tool:** Plausible self-hosted.
* **Events:**

  * `post_view` `{ id }`
  * `tag_view` `{ tag }`
* **Implementation:** Use `plausible()` global in `useEffect`.
* **Dashboard Access:** Author only (basic auth).

---

## 13. Security & Compliance

| Threat     | Mitigation                                                                |
| ---------- | ------------------------------------------------------------------------- |
| XSS        | `DOMPurify` on description render; Markdown limited to inline tags        |
| CSRF       | API only via `fetch` with same-origin; admin endpoints require Access JWT |
| Rate Limit | Cloudflare WAF rule: 1 000 requests / 10 min per IP                       |
| GDPR       | No PII stored; Plausible is cookieless                                    |

Secrets stored in Cloudflare environment variables (`IMAGES_TOKEN`, `PLAUSIBLE_DOMAIN`).

---

## 14. Environment Configuration & Deployment

| Stage          | Domain                       | Images Namespace | D1 DB   |
| -------------- | ---------------------------- | ---------------- | ------- |
| **Local**      | `localhost:5173`             | dev              | dev     |
| **Staging**    | `staging.example.com` | staging          | staging |
| **Production** | `example.com`         | prod             | prod    |

* `wrangler.toml` defines three environments.
* GitHub Actions matrix deploys on push → branch `staging`, `main`.
* Logpush to R2 bucket; alerts via Slack webhook.

---

## 15. Testing

| Layer             | Tool                                          | Coverage Target                      |
| ----------------- | --------------------------------------------- | ------------------------------------ |
| Unit              | Vitest + jsdom                                | ≥ 90 % lines                         |
| API Integration   | Vitest (Miniflare)                            | CRUD happy-path + auth failures      |
| E2E               | Playwright (Chromium, WebKit)                 | Index scroll, tag filter, admin CRUD |
| Performance       | Lighthouse-CI budget: < 1 s TTFB, < 2.5 s LCP |                                      |
| Accessibility     | `@axe-core/playwright` on index & post pages  |                                      |
| Visual Regression | Playwright screenshots (admin index)          |                                      |

---
</technical_specification>

<project_request>
**Draft Spec v1.0 (final)**.


```markdown
# Single-User Micro-Blog

A lightweight, Tumblr-style site for one author, serving ~2 000 image-centric posts with fast infinite scrolling.  
**Stack**: React + TypeScript + Mantine · Vite · Cloudflare Pages + Workers · D1 · Cloudflare Images · Plausible Analytics

---

## Target Audience
| Role | Needs |
|------|-------|
| **Owner/Admin** | Quick CRUD, one-time import, Google login |
| **Visitors**    | Smooth endless feed, tag browsing, fast images |

---

## Desired Features

### 1 · Public Frontend
- **Infinite-Scroll Index**  
  Virtualized; “Back to top” button after 3× viewport.
- **Tag Pages** — `/tag/:slug` (same endless UX).
- **Permalink** — `/post/:id` (numeric).  
  Meta tags use original image as OG/Twitter card.
- **RSS & Sitemap**  
  `/rss.xml` (20 latest), `/sitemap.xml`.
- **Plausible Analytics**  
  Script + events `post_view`, `tag_view`.
- **Performance**  
  `<img srcset>` referencing Cloudflare Images variants (`1x1xs … 1x1xl`); lazy-load except first screen.

### 2 · Admin UI `/admin`
| Feature | Details |
|---------|---------|
| **Auth** | Cloudflare Access (Google OIDC) — prod & staging |
| **Post Table** | Paginated, sortable, filter by tag |
| **CRUD** | Mantine modal forms, Zod validation |
| **Uploads** | Drag-drop ➜ Cloudflare Images · returns image ID |
| **Bulk Ops** | Multi-delete, tag add/remove (nice-to-have) |

### 3 · Data Layer
| Item | Tech / Fields |
|------|---------------|
| **DB** | Cloudflare D1 |
| **Tables** | `posts(id, title?, description, cf_image_id, cf_variants JSON, tumblr_url, tags_count, created_at, updated_at)`<br>`tags(id, name)`<br>`post_tags(post_id, tag_id)` |
| **Images** | Cloudflare Images originals + pre-defined variants `1x1xs / sm / md / lg / xl` |
| **API** | Worker routes: public `GET /api/posts`, `GET /api/tags`; auth-gated `POST /api/post` etc. |
| **Caching** | `Cache-Control: s-maxage=300, stale-while-revalidate=600` on public GETs |

### 4 · Import Script
```

node import.js --dump ./dump.json --images ./images

```
- Reads Tumblr JSON + local image folder.  
- Uploads each image to Cloudflare Images, records variant IDs.  
- Inserts rows; sets `title` = null (display as “(untitled)”) and stores original `tumblr_url`.

---

## Design Requests

| Element | Spec |
|---------|------|
| **Palette** | Full-bleed yellow `#FFE627`; deep gray/black text for AA contrast |
| **Logo** | Supplied sun SVG/PNG in sticky top-header |
| **Typography** | Google Font **Lexend** — 1.4 rem base, 700 for titles |
| **Layout** | 640 px max-width column, centered; mobile-first |
| **Mode** | Light-only |
| **Accessibility** | Alt text required; focus states via Mantine defaults |

---

## Dev-Ops & Repo

| Item | Detail |
|------|--------|
| **Mono-repo (GitHub)** | `/frontend` (Vite React) ➜ Cloudflare Pages<br>`/worker` (API + SSR) ➜ Wrangler deploy |
| **Shared Code** | `/packages/types` for DTOs & Zod schemas |
| **CI** | GitHub Actions → lint, test, build, deploy-to-staging, promote on `main` |
| **Secrets** | D1 binding, Images token, Plausible domain |

---

## Notes & Final Checks
- No titles in legacy data: UI shows “(untitled)” or first 50 chars of description; titles required on new posts.
- Permalinks are new (`/post/:id`); original Tumblr URLs stored for potential 301 Worker if ever needed.
- OG/Twitter meta simply references original image URL (often animated GIF). No dynamic image generation for now.

**All outstanding questions resolved. Spec is ready for implementation.** 🚀
</project_request>

---