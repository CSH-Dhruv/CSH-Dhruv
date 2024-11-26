- 👋 Hi, I’m @CSH-Dhruv
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
CSH-Dhruv/CSH-Dhruv is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
---><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dark Theme Website Builder</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #121212;
            color: #ffffff;
        }

        header {
            background-color: #1f1f1f;
            padding: 15px;
            text-align: center;
        }

        header h1 {
            margin: 0;
            color: #ff5722;
        }

        .container {
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .input-section {
            width: 80%;
            margin-bottom: 20px;
            padding: 15px;
            background-color: #1f1f1f;
            border-radius: 10px;
        }

        .input-section h2 {
            color: #ff9800;
        }

        .input-section input,
        .input-section textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #333333;
            border-radius: 5px;
            background-color: #2b2b2b;
            color: #ffffff;
        }

        .input-section button {
            background-color: #ff5722;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
        }

        .input-section button:hover {
            background-color: #e64a19;
        }

        .preview-section {
            width: 80%;
            padding: 15px;
            background-color: #1f1f1f;
            border-radius: 10px;
        }

        .preview-section h2 {
            color: #ff9800;
        }

        iframe {
            width: 100%;
            height: 400px;
            border: 1px solid #333333;
        }
    </style>
</head>
<body>
    <header>
        <h1>Dark Theme Website Builder</h1>
    </header>

    <div class="container">
        <div class="input-section">
            <h2>Create Your Website</h2>
            <input type="text" id="title" placeholder="Enter your website title" />
            <textarea id="content" rows="10" placeholder="Enter your website content"></textarea>
            <button onclick="generateWebsite()">Generate Website</button>
        </div>

        <div class="preview-section">
            <h2>Website Preview</h2>
            <iframe id="preview"></iframe>
        </div>
    </div>

    <script>
        function generateWebsite() {
            const title = document.getElementById('title').value;
            const content = document.getElementById('content').value;

            const websiteTemplate = `
                <!DOCTYPE html>
                <html lang="en">
                <head>
                    <meta charset="UTF-8">
                    <meta name="viewport" content="width=device-width, initial-scale=1.0">
                    <title>${title}</title>
                    <style>
                        body {
                            font-family: Arial, sans-serif;
                            background-color: #121212;
                            color: #ffffff;
                            padding: 20px;
                        }

                        h1 {
                            color: #ff5722;
                        }
                    </style>
                </head>
                <body>
                    <h1>${title}</h1>
                    <p>${content}</p>
                </body>
                </html>
            `;

            const previewFrame = document.getElementById('preview');
            const previewDoc = previewFrame.contentDocument || previewFrame.contentWindow.document;
            previewDoc.open();
            previewDoc.write(websiteTemplate);
            previewDoc.close();
        }
    </script>
</body>
</html>

