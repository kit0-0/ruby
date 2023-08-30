**Lesson 12: Web Scraping**

**1. Introduction to Web Scraping**
Web scraping is the process of extracting information from websites. Ruby provides libraries like Nokogiri and Mechanize for scraping web content.

**2. Nokogiri Library**
Nokogiri is a powerful library for parsing and manipulating HTML and XML documents.

**3. Installing Nokogiri**
You can install Nokogiri using the following command:

```bash
gem install nokogiri
```

**4. Scraping with Nokogiri**
Here's how you can use Nokogiri to scrape content from a web page:

```ruby
require 'nokogiri'
require 'open-uri'

url = 'https://example.com'
doc = Nokogiri::HTML(open(url))

# Extracting data
titles = doc.css('h2.title')
titles.each do |title|
  puts title.text
end
```

**5. Mechanize Library**
Mechanize is a library that automates interaction with websites, including form submission and navigation.

**6. Installing Mechanize**
You can install Mechanize using the following command:

```bash
gem install mechanize
```

**7. Web Scraping with Mechanize**
Here's how you can use Mechanize to automate interactions with a website:

```ruby
require 'mechanize'

agent = Mechanize.new
page = agent.get('https://example.com')

form = page.form_with(action: '/login')
form.field_with(name: 'username').value = 'myusername'
form.field_with(name: 'password').value = 'mypassword'

page = form.submit

puts page.body
```

**Code Sample: web_scraping.rb**
Here's a code sample to practice web scraping using Nokogiri:

```ruby
require 'nokogiri'
require 'open-uri'

url = 'https://news.ycombinator.com/'
doc = Nokogiri::HTML(open(url))

# Extracting article titles
titles = doc.css('.storylink')
titles.each_with_index do |title, index|
  puts "#{index + 1}. #{title.text}"
end
```

**Next Steps**
Web scraping is a powerful technique for gathering data from websites. As you continue learning, you can explore more advanced topics like handling different types of content (e.g., JSON, XML), navigating complex websites, and implementing rate limits to be respectful of the site's policies.
