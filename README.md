<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GitHub Profile README Generator</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    textarea { font-family: monospace; }
  </style>
</head>
<body class="bg-gray-100 min-h-screen p-6">
  <div class="max-w-5xl mx-auto">
    <h1 class="text-3xl font-bold mb-6 text-center">🚀 Samyak's GitHub Profile README Generator</h1>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">

      <!-- Input Fields -->
      <div class="space-y-4">
        <input id="name" type="text" placeholder="Your Full Name" class="w-full p-2 border rounded">
        <textarea id="summary" rows="4" placeholder="Professional Summary" class="w-full p-2 border rounded"></textarea>
        <input id="skills" type="text" placeholder="Skills (comma-separated)" class="w-full p-2 border rounded">
        <input id="projects" type="text" placeholder="Top Projects (comma-separated)" class="w-full p-2 border rounded">
        <input id="github" type="text" placeholder="GitHub Username" class="w-full p-2 border rounded">
        <input id="linkedin" type="text" placeholder="LinkedIn Username" class="w-full p-2 border rounded">
        <button onclick="generateMarkdown()" class="bg-blue-600 text-white px-4 py-2 rounded">Generate README</button>
      </div>

      <!-- Markdown Preview -->
      <div>
        <h2 class="text-xl font-semibold mb-2">📝 Generated Markdown</h2>
        <textarea id="output" rows="20" class="w-full p-2 border rounded"></textarea>
        <button onclick="copyToClipboard()" class="mt-2 bg-green-600 text-white px-4 py-2 rounded">Copy to Clipboard</button>
      </div>
    </div>
  </div>

  <script>
    function generateMarkdown() {
      const name = document.getElementById('name').value;
      const summary = document.getElementById('summary').value;
      const skills = document.getElementById('skills').value.split(',');
      const projects = document.getElementById('projects').value.split(',');
      const github = document.getElementById('github').value;
      const linkedin = document.getElementById('linkedin').value;

      let md = `# 👋 Hi, I'm ${name}\n\n`;
      md += `${summary}\n\n`;
      md += `## 🧠 Skills\n`;
      skills.forEach(skill => {
        md += `- ${skill.trim()}\n`;
      });
      md += `\n## 💼 Top Projects\n`;
      projects.forEach(project => {
        md += `- ${project.trim()}\n`;
      });
      md += `\n## 📫 Connect with me\n`;
      md += `- GitHub: [${github}](https://github.com/${github})\n`;
      md += `- LinkedIn: [${linkedin}](https://linkedin.com/in/${linkedin})\n`;

      document.getElementById('output').value = md;
    }

    function copyToClipboard() {
      const text = document.getElementById('output');
      text.select();
      text.setSelectionRange(0, 99999);
      document.execCommand('copy');
      alert('Markdown copied to clipboard!');
    }
  </script>
</body>
</html>

