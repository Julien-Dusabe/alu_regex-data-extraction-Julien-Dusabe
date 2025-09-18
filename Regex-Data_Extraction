import re

sample_text = """
Email: user@example.com
URL: https://www.example.com
Phone: (123) 456-7890
Credit Card: 1234-5678-9012-3456
Time: 2:30 PM
HTML: <div class="example">
Hashtag: #ThisIsAHashtag
Price: $1,234.56
"""

patterns = {
    "Email": r"\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b",
    "URL": r"https?:\/\/(?:www\.)?[a-zA-Z0-9.-]+\.[a-z]{2,}(?:\/\S*)?",
    "Phone": r"(?:\(\d{3}\)\s?|\d{3}[-.])\d{3}[-.]\d{4}",
    "Credit Card": r"(?:\d{4}[-\s]?){3}\d{4}",
    "Time": r"(?:[01]?\d|2[0-3]):[0-5]\d(?:\s?[APMapm]{2})?",
    "HTML": r"<[^>]+>",
    "Hashtag": r"#\w+",
    "Currency": r"\$\d{1,3}(?:,\d{3})*(?:\.\d{2})?"
}

for name, pattern in patterns.items():
    matches = re.findall(pattern, sample_text)
    print(f"{name}: {matches}")
