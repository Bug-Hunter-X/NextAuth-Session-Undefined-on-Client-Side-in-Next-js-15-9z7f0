## NextAuth Session Undefined on Client-Side in Next.js 15

This repository demonstrates a bug encountered when using NextAuth.js with Next.js 15.  The issue is that the session object, while correctly populated on the server-side, becomes undefined on the client-side.  The provided solution offers a workaround to access the session data.

**Bug:**
The session object passed to the About page component via `getServerSideProps` is undefined in the client-side rendering. This leads to errors and prevents the conditional rendering based on login status from working as expected.

**Solution:**
The solution utilizes the `useSession` hook from `next-auth` to access the session on the client-side, eliminating the reliance on the prop passed from the server.

**Steps to Reproduce:**
1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the development server: `npm run dev`
4. Navigate to `/about`
5. Observe the undefined session behavior.