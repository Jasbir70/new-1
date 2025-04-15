# new-1
import zipfile
import os

# Create website folder structure
website_dir = "/mnt/data/jasbir_website"
os.makedirs(website_dir, exist_ok=True)

# HTML content
html_content = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jasbir Singh - Writer & Editor</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }
        header {
            background-color: #222;
            color: white;
            padding: 40px 20px;
            text-align: center;
        }
        section {
            padding: 30px 20px;
            max-width: 800px;
            margin: auto;
        }
        h1, h2 {
            color: #222;
        }
        .skills, .languages {
            list-style-type: square;
            margin-left: 20px;
        }
        .footer {
            text-align: center;
            padding: 20px;
            background-color: #222;
            color: white;
            margin-top: 30px;
        }
        a {
            color: #f5b301;
        }
    </style>
</head>
<body>
    <header>
        <h1>Jasbir Singh</h1>
        <p>Writer & Editor</p>
    </header>

    <section>
        <h2>About Me</h2>
        <p>Hello! I'm Jasbir Singh, a passionate writer and editor who loves refining ideas and transforming words into clear, compelling content. With a sharp eye for detail and a love for storytelling, I work with brands, writers, and creators to craft content that resonates.</p>
    </section>

    <section>
        <h2>Skills</h2>
        <ul class="skills">
            <li>Content Editing & Proofreading</li>
            <li>Technical & Creative Writing</li>
            <li>SEO Content Structuring</li>
            <li>Prompt Engineering Basics</li>
            <li>AI Content Optimization Tools (ChatGPT, Grammarly)</li>
        </ul>
    </section>

    <section>
        <h2>Portfolio</h2>
        <p>Check out some of my sample work (coming soon!).</p>
    </section>

    <section>
        <h2>Contact</h2>
        <p>Email: <a href="mailto:jasbirsingh@email.com">jasbirsingh@email.com</a></p>
        <p>LinkedIn: <a href="https://linkedin.com/in/jasbirsingh" target="_blank">linkedin.com/in/jasbirsingh</a></p>
    </section>

    <div class="footer">
        <p>&copy; 2025 Jasbir Singh. All rights reserved.</p>
    </div>
</body>
</html>
"""

# Save HTML file
html_path = os.path.join(website_dir, "index.html")
with open(html_path, "w") as file:
    file.write(html_content)

# Create ZIP file
zip_path = "/mnt/data/Jasbir_Singh_Personal_Website.zip"
with zipfile.ZipFile(zip_path, 'w') as zipf:
    zipf.write(html_path, os.path.basename(html_path))

# Return the ZIP path
zip_path

