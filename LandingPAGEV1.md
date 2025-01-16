###FounderSOS Landing Page Documentation

## **ProjectOverview**

FounderSOS is a simple, one-page landing page designed to collect early sign-ups from solo founders. The page will include an engaging form to collect:

* **First Name**  
* **Email Address**  
* **Guess** (an optional field for users to share what they think the app is about).

The data will be collected and stored in **Supabase** and used to trigger an **auto email campaign** for early users. The project follows a modern, modular approach with a focus on maintainability, readability, and best practices.

---

## **App Flow**

1. **Frontend Design (Next.js \+ Tailwind CSS \+ TypeScript):**  
   * Designed initially in **V.o Dev by Vercel** for rapid prototyping.

Frontend code will be exported into **Cursor** using the command:  
`npx shadcn add [url]`

*   
  * The app uses the **Next.js App Router** and adheres to the **modularized component architecture** for reusability.  
2. **Backend (Supabase):**  
   * All data from the sign-up form will be sent securely to a Supabase database.  
   * Supabase will also handle:  
     * Storing **First Name**, **Email Address**, and **Guess**.  
     * Triggering an **auto email campaign** using Supabase's functions or integrations.  
3. **Deployment:**  
   * The app will be deployed using **Vercel**, leveraging its seamless Next.js integration.  
   * The deployment will be connected to a **GitHub repository** for version control.

---

## 

## **Folder and File Structure**

python  
CopyEdit  
`app/`  
`├── globals.css          # Global CSS styles`  
`├── layout.tsx           # Main layout wrapper`  
`├── page.tsx             # Landing page`  
`components/`  
`├── faq.tsx              # FAQ section component`  
`├── FlipCard.tsx         # Flip card component for problems/solutions`  
`├── logo-carousel.tsx    # Carousel component for partner tools/logos`  
`├── navbar.tsx           # Navbar component`  
`utils/`  
`├── isMobile.ts          # Utility function to detect mobile devices`  
`.eslintrc.json           # ESLint configuration`  
`.prettierrc              # Prettier configuration`  
`package.json             # Project dependencies`  
`tsconfig.json            # TypeScript configuration`

---

## **Frontend**

### **Tech Stack:**

* **Framework:** Next.js (using the **App Router**, not the legacy `src` directory).  
* **Styling:** Tailwind CSS for modern, responsive styles.  
* **Language:** TypeScript for strong typing and maintainability.  
* **Linting & Formatting:**  
  * **ESLint** (latest version) for linting to ensure clean and consistent code.  
  * **Prettier** (latest version) for formatting, strictly enforced.

### **Frontend Architecture Principles:**

1. **Modular Components:**  
   * Each component is designed to be reusable and self-contained (e.g., `FlipCard.tsx`, `logo-carousel.tsx`).  
2. **Type Safety:**  
   * Ensure proper **TypeScript type definitions** for all props and state.  
3. **CSS Utility Classes:**  
   * Use Tailwind CSS to simplify styling and minimize custom CSS.  
4. **Responsive Design:**  
   * Ensure mobile-first responsiveness using Tailwind's utilities.  
5. **Folder Organization:**  
   * Keep components in the `components` folder, utilities in `utils`, and global styles in `globals.css`.

---

## **Backend**

### **Tech Stack:**

* **Database:** Supabase (PostgreSQL-based).  
* **Data Storage:** All collected form data is stored in a secure Supabase table.

### **Email Campaign Integration:**

* Supabase will trigger an **auto email campaign** based on form submissions using:  
  * **Supabase Functions** for serverless backend logic.  
  * Integration with third-party email services (e.g., Mailgun or SendGrid).

---

## **GitHub Version Control**

### **Workflow:**

1. **Branch Management:**  
   * Use the `main` branch for production-ready code.  
   * Create feature branches for new components or changes (e.g., `feature/flip-card`).  
   * Merge via Pull Requests (PRs) to ensure code review before merging.  
2. **Commit Guidelines:**  
   * Write descriptive commit messages (e.g., *"Add FlipCard component for problem/solution UI"*).  
   * Commit frequently with small, focused updates.  
3. **Push Updates:**

Ensure all code adheres to **Prettier** and **ESLint** rules before pushing.

Push to GitHub:  
bash  
CopyEdit  
`git add .`  
`git commit -m "Your message"`  
`git push origin branch-name`

*   
4. **Bug-Free Standards:**  
   * Follow systematic debugging. Never assume or guess:  
     * Log and inspect errors.  
     * Consult official documentation for the latest versions of libraries/frameworks.  
     * Collaborate effectively to resolve gaps in knowledge.

---

## **Deployment**

### **Platform: Vercel**

* Automatically deploys changes from the `main` branch of the GitHub repository.  
* Ensure environmental variables are set for:  
  * **Supabase URL**  
  * **Supabase API Key**

### **Deployment Workflow:**

Test locally:  
bash  
CopyEdit  
`npm run dev`

1.   
2. Push updates to `main` after testing.  
3. Monitor deployment status on Vercel’s dashboard.

---

## **Key Rules**

1. Always modularize Next.js components for reusability.  
2. Strictly adhere to **Prettier** and **ESLint** configurations for consistent, error-free code.  
3. Follow the **App Router** structure; do not use `src`.  
4. Think like an engineer:  
   * Never assume or guess; debug methodically.  
   * Clarify uncertainties to find factual solutions.  
5. Maintain type safety by defining props and state with TypeScript.  
6. Document all significant changes and decisions for better collaboration.

---

## **Development Tools**

1. **Frontend:**

V.o Dev for design, exported using:  
bash  
CopyEdit  
`npx shadcn add [url]`

*   
  * Refine and integrate in Cursor IDE.  
2. **Backend:** Supabase for data storage and email automation.  
3. **Version Control:** GitHub for commits, branching, and collaborative workflows.  
4. **Deployment:** Vercel for serverless hosting.

---

## **Final Notes**

This project adheres to **clean coding practices**, modular architecture, and a strong debugging-first mindset to ensure a smooth development experience. Every decision made during development will focus on scalability, simplicity, and maintainability.

Best Practices & Rules
No Assumptions:

If unsure, state it clearly and look up the correct info.
Systematic Debugging:

Rely on console logs, error messages, and official documentation to resolve issues.
TypeScript Everywhere:

Always define types for components and utilities.
Maintain clarity for props, state, and function returns.
ESLint & Prettier:

Keep your code consistently styled and error-free.
Update configs only if you understand the changes.
Frequent Commits:

Small, atomic commits that represent meaningful progress or fixes.
Deployment Checks:

Run npm run build locally before pushing if you suspect major changes.
Check the deployed site thoroughly on Vercel.