# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.



----------------------------------------------------*******--------------------------------------------------------------------


✅ React Folder Structure (Easy Explanation)
Jab tum React project create karte ho (Vite ya CRA se), toh kuch basic folders milte hain:
my-app/
│
├── node_modules/
├── public/
├── src/
├── package.json
├── vite.config.js
└── README.md







📌 1. node_modules/
node_modules/
✅ Ye folder React ke saare installed packages rakhta hai
Example:
react
react-dom
axios
tailwind
⚠️ Isko kabhi manually edit nahi karte
Ye automatically manage hota hai.









📌 2. public/
public/
   ├── index.html
   ├── favicon.ico
✅ Ye folder static files ke liye hota hai
images
icons
robots.txt
Example:
👉 Agar tum direct image use karna chaho bina import ke:
public/logo.png
Use like:
<img src="/logo.png" />










📌 3. src/ (Most Important Folder)
src/
   ├── main.jsx
   ├── App.jsx
   ├── components/
   ├── pages/
   ├── assets/
   ├── styles/
   ├── utils/
React ka actual kaam yahi hota hai.
✅ main.jsx
src/main.jsx
Ye entry point hota hai React ka.
ReactDOM.createRoot(document.getElementById("root")).render(
  <App />
);
Matlab React app start yaha se hoti hai.
✅ App.jsx
src/App.jsx
Ye root component hota hai.
function App() {
  return <h1>Hello Ayan bhai</h1>;
}
App ke andar tum pages/components add karte ho.











📌 4. components/ Folder
src/components/
   ├── Navbar.jsx
   ├── Footer.jsx
   ├── Button.jsx
✅ Reusable UI parts ke liye hota hai
Example:
<Navbar />
<Button />











📌 5. pages/ Folder
src/pages/
   ├── Home.jsx
   ├── About.jsx
   ├── Contact.jsx
✅ Website ke main pages yaha hote hain
React Router use karte time pages folder must hota hai.
Example:
<Route path="/" element={<Home />} />










📌 6. assets/ Folder
src/assets/
   ├── logo.png
   ├── banner.jpg
✅ Images, icons, fonts store karne ke liye
Use like:
import logo from "../assets/logo.png";
<img src={logo} />
📌 7. styles/ Folder (CSS/Tailwind)
src/styles/
   ├── global.css
   ├── navbar.css
Agar tum CSS files separate rakhna chaho.












📌 8. utils/ Folder
src/utils/
   ├── helper.js
   ├── constants.js
✅ Extra functions ya reusable logic ke liye
Example:
export const API_URL = "https://api.com";











📌 9. services/ Folder (API Calls)
src/services/
   ├── api.js
API related functions yaha.
import axios from "axios";
export const fetchUsers = () => axios.get("/users");










📌 10. hooks/ Folder
src/hooks/
   ├── useFetch.js
Custom hooks yaha rakhte hain.
✅ Best Professional React Folder Structure
Agar tum full-stack developer ban rahe ho, toh best structure:
src/
│
├── components/
├── pages/
├── layouts/
├── routes/
├── assets/
├── hooks/
├── context/
├── services/
├── utils/
├── styles/
│
├── App.jsx
└── main.jsx
🔥 Example Real Project Structure
src/
│
├── components/
│     ├── Navbar.jsx
│     ├── ProductCard.jsx
│
├── pages/
│     ├── Home.jsx
│     ├── Login.jsx
│
├── context/
│     ├── AuthContext.jsx
│
├── services/
│     ├── api.js
│
├── App.jsx
└── main.jsx












✅ Ayan bhai Quick Summary
Folder	Use
components	Reusable UI parts
pages	Website screens
assets	Images, icons
styles	CSS files
services	API calls
utils	Helper functions
hooks	Custom hooks