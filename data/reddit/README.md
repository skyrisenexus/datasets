# Reddit Data Collection

This directory contains the `subreddits.json` file, which lists various technology and programming-related subreddits for data collection and analysis purposes. The configuration file is located at [`subreddits.json`](https://github.com/skyrisenexus/datasets/blob/main/data/reddit/subreddits.json).

## 📊 Data Structure

### File: `subreddits.json`

The configuration file contains a simple array structure with a list of subreddit names:

```json
[
  {
    "subreddits": [
      "technology",
      "artificial",
      "science",
      "MachineLearning",
      "datascience",
      "programming",
      // ... other subreddits
    ]
  }
]
```

### Subreddit Categories

The included subreddits cover various technology-related topics:

1. **General Technology**
   - technology
   - technews
   - futurism

2. **Artificial Intelligence & Machine Learning**
   - artificial
   - MachineLearning
   - AI
   - artificialintelligence
   - deeplearning
   - neuralnetworks

3. **Programming & Development**
   - programming
   - learnprogramming
   - Python
   - javascript
   - rust
   - golang
   - cplusplus

4. **Computer Science**
   - computerscience
   - datastructures
   - algorithms
   - functionalprogramming

5. **Web Development**
   - webdev
   - reactjs
   - javascript

6. **Security**
   - cybersecurity
   - hacking
   - netsec
   - ethicalhacking
   - cryptography

7. **Cloud & DevOps**
   - devops
   - cloudcomputing

8. **Data Science**
   - datascience
   - bigdata

## 🚀 Usage

### Accessing Subreddit Data

1. Each subreddit can be accessed through Reddit's API at:
   ```
   https://www.reddit.com/r/{subreddit_name}.json
   ```
   Example: [https://www.reddit.com/r/technology.json](https://www.reddit.com/r/technology.json)

2. For subreddit metadata:
   ```
   https://www.reddit.com/r/{subreddit_name}/about.json
   ```
   Example: [https://www.reddit.com/r/technology/about.json](https://www.reddit.com/r/technology/about.json)

### API Guidelines

When collecting data from these subreddits:
- Follow Reddit's API Terms of Service
- Respect rate limiting
- Use appropriate authentication
- Include proper User-Agent headers

## 🔒 Security & Privacy

- Follow Reddit's content policies
- Respect user privacy
- Handle data according to Reddit's API terms
- Store collected data securely

## 📝 Notes

- Subreddit availability may change
- Some subreddits might have additional rules
- Content quality and volume varies by subreddit
- Regular updates to the list may occur

## ⚠️ Limitations

- Subject to Reddit API limitations
- Some subreddits may become private
- Content may be removed or archived
- API changes may affect data collection

---

*Last updated: [Current Date]*

For questions or issues, please create a GitHub issue or contact the maintainers.