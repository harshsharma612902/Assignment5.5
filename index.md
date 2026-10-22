The External Stylesheet (style.css)
CSS
/* Step 1 & 5: CSS Variables & Design Tokens */
:root {
    --primary-color: #1e3a8a;   /* Deep Navy */
    --accent-color: #0d9488;    /* Teal Accent */
    --bg-color: #f8fafc;        /* Off-white Background */
    --card-bg: #ffffff;         /* Pure White */
    --text-main: #1e293b;       /* Dark Slate */
    --text-muted: #64748b;      /* Gray Muted Text */
    --border-color: #cbd5e1;    /* Light Border */
    
    --spacing-sm: 8px;
    --spacing-md: 16px;
    --spacing-lg: 24px;
    --spacing-xl: 40px;
}

/* Universal Selector */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

/* Step 2 & 3: Typography & Body Styling */
body {
    background-color: var(--bg-color);
    color: var(--text-main);
    font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    line-height: 1.6;
    padding-bottom: var(--spacing-xl);
}

/* Step 3: Navigation Styling */
nav {
    background-color: var(--primary-color);
    padding: var(--spacing-md) var(--spacing-xl);
    display: flex;
    justify-content: space-between;
    align-items: center;
}

nav .logo {
    color: #ffffff;
    font-weight: 700;
    font-size: 1.25rem;
}

nav ul {
    list-style: none;
    display: flex;
    gap: var(--spacing-lg);
}

nav a {
    color: #ffffff;
    text-decoration: none;
    font-weight: 600;
    transition: color 0.2s ease;
}

nav a:hover {
    color: var(--accent-color);
}

/* Container Layout */
.container {
    max-width: 900px;
    margin: var(--spacing-xl) auto;
    padding: 0 var(--spacing-md);
}

/* Step 3: Headings and Paragraphs */
h1 {
    color: var(--primary-color);
    font-size: 2.25rem;
    margin-bottom: var(--spacing-md);
}

h2 {
    color: var(--primary-color);
    font-size: 1.5rem;
    margin-bottom: var(--spacing-md);
    border-bottom: 2px solid var(--accent-color);
    padding-bottom: var(--spacing-sm);
}

p {
    color: var(--text-muted);
    font-size: 1rem;
    margin-bottom: var(--spacing-md);
}

/* Step 3: Buttons */
.btn {
    background-color: var(--accent-color);
    color: #ffffff;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
    text-decoration: none;
    display: inline-block;
    transition: background-color 0.2s ease;
}

.btn:hover {
    background-color: #0f766e;
}

/* Step 4: Readable Tables */
table {
    width: 100%;
    border-collapse: collapse;
    background-color: var(--card-bg);
    margin-bottom: var(--spacing-xl);
    border-radius: 6px;
    overflow: hidden;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
}

th, td {
    padding: var(--spacing-md);
    text-align: left;
    border-bottom: 1px solid var(--border-color);
}

th {
    background-color: var(--primary-color);
    color: #ffffff;
    font-weight: 600;
}

tr:nth-child(even) {
    background-color: #f1f5f9;
}

/* Step 4: Readable Forms */
form {
    background-color: var(--card-bg);
    padding: var(--spacing-lg);
    border-radius: 6px;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    gap: var(--spacing-md);
}

.form-group {
    display: flex;
    flex-direction: column;
    gap: var(--spacing-sm);
}

label {
    font-weight: 600;
    color: var(--text-main);
}

input, select {
    padding: 10px;
    border: 1px solid var(--border-color);
    border-radius: 4px;
    font-size: 1rem;
    font-family: inherit;
}

input:focus, select:focus {
    outline: none;
    border-color: var(--accent-color);
    box-shadow: 0 0 0 3px rgba(13, 148, 136, 0.15);
}
2. Sample HTML Page (index.html)
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>College Coding Club</title>
    <!-- Step 1: External CSS -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation -->
    <nav>
        <div class="logo">CodeClub</div>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#schedule">Schedule</a></li>
            <li><a href="#join">Join</a></li>
        </ul>
    </nav>

    <main class="container">
        
        <!-- Headings and Paragraphs -->
        <section id="home">
            <h1>Welcome to the College Coding Club</h1>
            <p>We build cool projects, host coding workshops, and prepare students for tech careers through collaborative learning. Whether you are a beginner or an advanced developer, there is a place for you here.</p>
            <a href="#join" class="btn">Become a Member</a>
        </section>

        <br>

        <!-- Table Section -->
        <section id="schedule">
            <h2>Weekly Meeting Schedule</h2>
            <table>
                <thead>
                    <tr>
                        <th>Day</th>
                        <th>Topic</th>
                        <th>Location</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Tuesdays</td>
                        <td>HTML & CSS Workshops</td>
                        <td>Hall 101</td>
                    </tr>
                    <tr>
                        <td>Thursdays</td>
                        <td>JavaScript & Problem Solving</td>
                        <td>Lab 3B</td>
                    </tr>
                    <tr>
                        <td>Fridays</td>
                        <td>Hackathon Prep & Project Review</td>
                        <td>Online (Zoom)</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <!-- Form Section -->
        <section id="join">
            <h2>Club Membership Sign-Up</h2>
            <form action="#" method="POST">
                <div class="form-group">
                    <label for="fullname">Full Name</label>
                    <input type="text" id="fullname" name="fullname" placeholder="Enter your full name" required>
                </div>
                <div class="form-group">
                    <label for="major">Major / Field of Study</label>
                    <input type="text" id="major" name="major" placeholder="e.g., Computer Science" required>
                </div>
                <div class="form-group">
                    <label for="experience">Experience Level</label>
                    <select id="experience" name="experience">
                        <option value="beginner">Beginner</option>
                        <option value="intermediate">Intermediate</option>
                        <option value="advanced">Advanced</option>
                    </select>
                </div>
                <button type="submit" class="btn">Submit Application</button>
            </form>
        </section>

    </main>

</body>
</html>
3. Design Choices Explanation
We chose a professional corporate-tech color palette utilizing deep navy blues and vibrant teal accents to convey reliability and modern energy for the college club website. Centralized CSS variables in :root ensure consistent hierarchy, fluid spacing, and effortless future theme updates across all pages. Tables and forms feature clear grid borders, alternating row colors, and focus rings to maximize readability and user interaction. Finally, modular class selectors and clean flexbox layouts maintain a scalable, organized codebase that is fully responsive for student visitors.