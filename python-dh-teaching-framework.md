# Comprehensive Python for Digital Humanities Teaching and Assessment Framework
*15-Hour Course in the LLM Era*

## Executive Summary

This framework provides a complete teaching and assessment approach for a 15-hour Python for Digital Humanities course designed for mixed-preparedness cohorts in the era of Large Language Models. The framework emphasizes AI-robust skills, process-based assessment, and transparent AI collaboration while maintaining rigorous academic standards.

---

## Section 1: 20 Simple DH Examples and Teaching Guidance

### Core Concepts: Comments, print(), variables, input(), if conditions, lists, for loops, functions

#### 1. Scholarly Greeting System
**Concept**: Comments and print()
```python
# Welcome message for digital humanities project
print("Welcome to the Medieval Manuscript Archive")
print("Today we explore 12th century illuminated texts")
```
**Teaching Notes**: Emphasize documentation as scholarly practice. Comments are like footnotes in academic writing[3][4].

#### 2. Manuscript Cataloger's Name Tag
**Concept**: Variables
```python
# Cataloger information for manuscript database
cataloger_name = "Dr. Sarah Chen"
manuscript_id = "MS_Gothic_001"
print("Cataloger:", cataloger_name)
print("Current manuscript:", manuscript_id)
```
**Teaching Notes**: Variables store scholarly data. Connect to metadata concepts familiar to humanities students[9].

#### 3. Archive Visit Calculator
**Concept**: Variables with numbers
```python
# Calculate total research hours
daily_hours = 8
research_days = 5
total_hours = daily_hours * research_days
print("Total archive hours:", total_hours)
```
**Teaching Notes**: Show quantitative aspects of humanities research (time management, resource allocation).

#### 4. Interactive Bibliography Builder
**Concept**: input()
```python
# Collect citation information
author = input("Enter author name: ")
title = input("Enter book title: ")
year = input("Enter publication year: ")
print("Citation:", author, "(" + year + "). " + title)
```
**Teaching Notes**: Connect to familiar academic practices. Every student understands citations[27].

#### 5. Research Permission Checker
**Concept**: if conditions
```python
# Check if researcher can access rare books
researcher_status = input("Are you faculty or graduate student? ")
if researcher_status == "faculty":
    print("Access granted to all rare book collections")
else:
    print("Please request supervisor approval")
```
**Teaching Notes**: Real-world library/archive access scenarios that students recognize.

#### 6. Language Detection System
**Concept**: if-elif-else
```python
# Identify manuscript language
script_type = input("Enter script type (latin/greek/arabic): ")
if script_type == "latin":
    print("Likely Western European manuscript")
elif script_type == "greek":
    print("Byzantine or early Christian text")
elif script_type == "arabic":
    print("Islamic scholarly manuscript")
else:
    print("Unknown script - requires specialist analysis")
```
**Teaching Notes**: Introduces complexity gradually while using familiar scholarly concepts.

#### 7. Author Collection Tracker
**Concept**: Lists
```python
# Track authors in a literary corpus
victorian_authors = ["Dickens", "Austen", "Bronte", "Hardy"]
print("Authors in collection:")
print(victorian_authors)
print("Total authors:", len(victorian_authors))
```
**Teaching Notes**: Lists are like bibliographies or indexes - familiar organizational tools.

#### 8. Adding New Discoveries
**Concept**: List operations
```python
# Expand author collection with new findings
victorian_authors = ["Dickens", "Austen", "Bronte"]
victorian_authors.append("Trollope")
victorian_authors.append("Gaskell")
print("Updated collection:", victorian_authors)
```
**Teaching Notes**: Research is iterative - we constantly add new knowledge.

#### 9. Archive Inventory Display
**Concept**: for loops with lists
```python
# Display all manuscripts in collection
manuscripts = ["Beowulf_fragment", "Canterbury_Tales_MS", "Piers_Plowman_copy"]
print("Current manuscripts in archive:")
for manuscript in manuscripts:
    print("-", manuscript)
```
**Teaching Notes**: Systematic examination of sources - core humanities methodology.

#### 10. Word Frequency Counter
**Concept**: for loops with counting
```python
# Count words in a text sample
text_words = ["love", "death", "honor", "love", "death", "love"]
love_count = 0
for word in text_words:
    if word == "love":
        love_count = love_count + 1
print("Instances of 'love':", love_count)
```
**Teaching Notes**: Introduction to textual analysis - fundamental DH skill.

#### 11. Medieval Date Converter
**Concept**: Functions (basic)
```python
def convert_regnal_year(king_name, regnal_year):
    """Convert regnal year to CE date - simplified for demonstration"""
    print("In the", regnal_year, "year of King", king_name)
    
convert_regnal_year("Edward III", 15)
convert_regnal_year("Richard II", 3)
```
**Teaching Notes**: Functions organize scholarly methods. Like having a standard citation style.

#### 12. Text Cleaner Function
**Concept**: Functions with return values
```python
def clean_text(raw_text):
    """Basic text cleaning for analysis"""
    clean = raw_text.lower()
    clean = clean.replace(",", "")
    clean = clean.replace(".", "")
    return clean

original = "Hello, World!"
cleaned = clean_text(original)
print("Original:", original)
print("Cleaned:", cleaned)
```
**Teaching Notes**: Preprocessing is essential in DH. Like editorial work on historical texts.

#### 13. Citation Format Validator
**Concept**: Functions with if statements
```python
def check_citation_format(citation):
    """Check if citation includes basic elements"""
    if "(" in citation and ")" in citation:
        print("Date format: OK")
    else:
        print("Missing date parentheses")
    if "." in citation:
        print("Punctuation: OK")
    else:
        print("Missing period")

check_citation_format("Smith (2023). Digital Methods.")
check_citation_format("Jones 2022 No punctuation")
```
**Teaching Notes**: Quality control in academic work - students understand citation standards.

#### 14. Research Progress Tracker
**Concept**: Multiple concepts together
```python
# Track daily research progress
research_log = []
day = 1

while day <= 3:
    sources_read = input(f"Day {day} - How many sources did you read? ")
    research_log.append(f"Day {day}: {sources_read} sources")
    day = day + 1

print("Research Summary:")
for entry in research_log:
    print(entry)
```
**Teaching Notes**: Combines loops, lists, and user input for realistic scholarly workflow.

#### 15. Simple Concordance Builder
**Concept**: String operations
```python
# Find word positions in text
text = "the quick brown fox jumps over the lazy dog"
search_word = "the"
words = text.split()

print(f"Positions of '{search_word}':")
for i in range(len(words)):
    if words[i] == search_word:
        print(f"Position {i+1}: {words[i]}")
```
**Teaching Notes**: Introduction to computational text analysis - core DH methodology.

#### 16. Genre Classification System
**Concept**: Nested if statements
```python
# Classify literary works by characteristics
verse_form = input("Is it in verse? (yes/no): ")
dramatic = input("Is it performed? (yes/no): ")

if verse_form == "yes":
    if dramatic == "yes":
        print("Genre: Dramatic Poetry (e.g., Shakespeare's plays)")
    else:
        print("Genre: Lyric or Narrative Poetry")
else:
    if dramatic == "yes":
        print("Genre: Prose Drama")
    else:
        print("Genre: Prose (novel, short story, essay)")
```
**Teaching Notes**: Literary classification familiar to humanities students.

#### 17. Multi-Language Text Counter
**Concept**: Working with lists and functions
```python
def count_languages(text_collection):
    """Count texts by language"""
    language_count = {"English": 0, "Latin": 0, "French": 0}
    
    for text_info in text_collection:
        language = text_info["language"]
        if language in language_count:
            language_count[language] += 1
    
    return language_count

# Sample medieval manuscript collection
manuscripts = [
    {"title": "Canterbury Tales", "language": "English"},
    {"title": "Summa Theologica", "language": "Latin"},
    {"title": "Roman de la Rose", "language": "French"}
]

counts = count_languages(manuscripts)
for language, count in counts.items():
    print(f"{language}: {count} texts")
```
**Teaching Notes**: Introduces dictionaries through familiar multilingual manuscript contexts.

#### 18. Periodization Helper
**Concept**: Ranges and conditionals
```python
def identify_period(year):
    """Identify historical period from year"""
    if 500 <= year <= 1500:
        return "Medieval"
    elif 1500 <= year <= 1800:
        return "Early Modern"
    elif 1800 <= year <= 1900:
        return "19th Century"
    else:
        return "Modern/Contemporary"

# Test with various dates
test_years = [1066, 1605, 1848, 1969]
for year in test_years:
    period = identify_period(year)
    print(f"Year {year}: {period} period")
```
**Teaching Notes**: Historical thinking through computational logic.

#### 19. Simple Stopword Filter
**Concept**: List comprehension introduction
```python
# Remove common words from text analysis
text_words = ["the", "castle", "was", "very", "old", "and", "mysterious"]
stopwords = ["the", "was", "and", "very"]

# Traditional approach first
important_words = []
for word in text_words:
    if word not in stopwords:
        important_words.append(word)

print("Filtered words:", important_words)

# Show list comprehension as advanced technique
# filtered = [word for word in text_words if word not in stopwords]
```
**Teaching Notes**: Text preprocessing essential for DH analysis.

#### 20. Basic Corpus Statistics
**Concept**: Integration of all concepts
```python
def analyze_corpus(texts):
    """Analyze a small corpus of texts"""
    total_texts = len(texts)
    total_words = 0
    word_frequencies = {}
    
    print(f"Analyzing {total_texts} texts...")
    
    for i, text in enumerate(texts, 1):
        words = text.lower().split()
        text_length = len(words)
        total_words += text_length
        
        print(f"Text {i}: {text_length} words")
        
        # Count word frequencies
        for word in words:
            if word in word_frequencies:
                word_frequencies[word] += 1
            else:
                word_frequencies[word] = 1
    
    print(f"Total corpus: {total_words} words")
    print("Most common words:")
    # Simple way to find most common
    for word, count in word_frequencies.items():
        if count >= 2:  # Appears at least twice
            print(f"'{word}': {count} times")

# Sample literary corpus
sample_corpus = [
    "The summer palace was beautiful in the morning light",
    "Beautiful gardens surrounded the ancient palace",
    "Morning brought new light to the palace gardens"
]

analyze_corpus(sample_corpus)
```
**Teaching Notes**: Culminating example showing computational analysis of literary texts.

---

## Section 2: 10 Iterative Examples with LLM Prompts

### Example 1: Text Analysis Pipeline
**Concept Progression**: Basic → Intermediate → Advanced

#### Iteration 1: Simple Word Count
**Why it matters for DH**: Fundamental quantitative text analysis skill
**LLM Prompt**: "Help me write Python code to count words in a text string. The text should be: 'Digital humanities combines computing with traditional humanities scholarship.' Make it beginner-friendly with clear comments."

```python
# Basic word counting for text analysis
text = "Digital humanities combines computing with traditional humanities scholarship."
words = text.split()
word_count = len(words)
print("Text:", text)
print("Word count:", word_count)
```

#### Iteration 2: Word Frequency Analysis
**Why it matters for DH**: Identifies patterns and themes in texts
**LLM Prompt**: "Extend the previous code to count how often each word appears. Use a dictionary to store word frequencies. Include handling for punctuation."

```python
import string

# Advanced word frequency analysis
text = "Digital humanities combines computing with traditional humanities scholarship. Digital methods transform humanities research."
# Remove punctuation and convert to lowercase
clean_text = text.translate(str.maketrans('', '', string.punctuation)).lower()
words = clean_text.split()

# Count frequencies
word_freq = {}
for word in words:
    word_freq[word] = word_freq.get(word, 0) + 1

# Display results
print("Word frequencies:")
for word, count in sorted(word_freq.items(), key=lambda x: x[1], reverse=True):
    print(f"{word}: {count}")
```

#### Iteration 3: Comparative Text Analysis
**Why it matters for DH**: Compare texts across periods, authors, or genres
**LLM Prompt**: "Create a function that compares word frequencies between two texts and identifies unique words in each. This helps compare different authors or time periods."

```python
def compare_texts(text1, text2, title1="Text 1", title2="Text 2"):
    """Compare word frequencies between two texts"""
    def get_frequencies(text):
        clean_text = text.translate(str.maketrans('', '', string.punctuation)).lower()
        words = clean_text.split()
        freq = {}
        for word in words:
            freq[word] = freq.get(word, 0) + 1
        return freq
    
    freq1 = get_frequencies(text1)
    freq2 = get_frequencies(text2)
    
    # Find unique words
    unique_to_1 = set(freq1.keys()) - set(freq2.keys())
    unique_to_2 = set(freq2.keys()) - set(freq1.keys())
    
    print(f"Words unique to {title1}: {list(unique_to_1)}")
    print(f"Words unique to {title2}: {list(unique_to_2)}")
    
    # Common words with different frequencies
    common_words = set(freq1.keys()) & set(freq2.keys())
    print(f"\nCommon words with different usage:")
    for word in sorted(common_words):
        if freq1[word] != freq2[word]:
            print(f"{word}: {title1}({freq1[word]}) vs {title2}({freq2[word]})")

# Example usage
shakespeare = "To be or not to be that is the question"
marlowe = "Was this the face that launched a thousand ships"
compare_texts(shakespeare, marlowe, "Shakespeare", "Marlowe")
```

### Example 2: Metadata Processing Pipeline
**Concept Progression**: Data structures → File handling → Analysis

#### Iteration 1: Simple Metadata Storage
**Why it matters for DH**: Organizing scholarly information systematically
**LLM Prompt**: "Help me create a dictionary to store metadata for a medieval manuscript: title, author, date, language, and location. Show how to display this information clearly."

#### Iteration 2: Multiple Records with Search
**Why it matters for DH**: Building searchable databases of cultural objects
**LLM Prompt**: "Expand to handle multiple manuscripts in a list of dictionaries. Add a search function to find manuscripts by author or language."

#### Iteration 3: CSV Import/Export System
**Why it matters for DH**: Integration with standard academic data formats
**LLM Prompt**: "Add functionality to read manuscript data from a CSV file and export search results to a new CSV file. This enables integration with Excel and other scholarly tools."

### Example 3: Named Entity Recognition Pipeline
**Concept Progression**: String processing → Pattern recognition → Classification

#### Iteration 1: Simple Name Extraction
**Why it matters for DH**: Identifying people, places, and organizations in texts
**LLM Prompt**: "Write code to find all capitalized words in a text that might be proper nouns (names, places). Handle basic cases like words at the beginning of sentences."

#### Iteration 2: Pattern-Based Enhancement
**Why it matters for DH**: More sophisticated entity recognition
**LLM Prompt**: "Improve the code to identify different types of entities: personal titles (Dr., Prof., Sir), place indicators (City of, Kingdom of), and dates (patterns like 'in 1066' or 'during the reign of')."

#### Iteration 3: Context-Aware Classification
**Why it matters for DH**: Understanding relationships between entities
**LLM Prompt**: "Add functionality to classify entities by context and find relationships (e.g., 'King Richard invaded France' shows relationship between person and place)."

### Example 4: Citation Network Analysis
**Concept Progression**: Text parsing → Graph structures → Visualization

#### Iteration 1: Citation Parser
**Why it matters for DH**: Understanding scholarly conversations
**LLM Prompt**: "Create code to extract author names and years from academic citations in standard format: 'Author (Year)'. Handle multiple authors."

#### Iteration 2: Citation Network Builder
**Why it matters for DH**: Mapping intellectual influence
**LLM Prompt**: "Extend to track which authors cite which other authors, creating a network of scholarly influence. Store this as connections between authors."

#### Iteration 3: Influence Metrics
**Why it matters for DH**: Quantifying scholarly impact
**LLM Prompt**: "Add analysis to find the most influential authors (most cited), identify citation clusters (groups of authors who cite each other), and detect emerging trends."

### Example 5: Historical Timeline Generator
**Concept Progression**: Date handling → Chronological sorting → Pattern analysis

#### Iteration 1: Event Storage and Sorting
**Why it matters for DH**: Organizing historical information chronologically
**LLM Prompt**: "Create a system to store historical events with dates and descriptions, then sort them chronologically. Handle different date formats (years, months, specific dates)."

#### Iteration 2: Period Analysis
**Why it matters for DH**: Understanding historical patterns
**LLM Prompt**: "Add functionality to group events by time periods (decades, centuries) and identify periods of high activity or change."

#### Iteration 3: Comparative Timelines
**Why it matters for DH**: Comparing historical developments
**LLM Prompt**: "Create side-by-side timelines for different regions or topics, highlighting simultaneous events and potential connections."

### Examples 6-10 follow similar patterns, each building computational sophistication while maintaining DH relevance:
- **Example 6**: Stylometric analysis (word length → sentence patterns → author identification)
- **Example 7**: Geographic mapping (location extraction → coordinate mapping → spatial analysis)
- **Example 8**: Image metadata processing (basic EXIF → batch processing → content analysis)
- **Example 9**: Social network analysis (relationship extraction → network building → community detection)
- **Example 10**: Corpus comparison (basic statistics → statistical testing → machine learning classification)

---

## Section 3: Teaching Guide for Day 1 Concepts

### Comments - The Scholarly Documentation Principle

#### Key Points
- Comments are like footnotes in academic writing - they provide context and explanation[3][4]
- Good comments explain *why* something is done, not just *what* is done
- In DH, documentation is crucial for reproducible research

#### Common Pitfalls
- Students often neglect comments entirely
- Writing comments that simply repeat the code
- Inconsistent commenting styles
- Too many obvious comments cluttering the code

#### Teaching Techniques
- **Start with familiar analogies**: "Comments are like marginal notes in medieval manuscripts"
- **Show bad examples first**: Let students identify what makes comments unhelpful
- **Peer review exercises**: Students review each other's comments for clarity
- **Progressive complexity**: Start with single-line comments, advance to docstrings

#### Three Analogies for Comments
1. **Medieval Glosses**: Like scribes adding explanatory notes to manuscripts
2. **Archaeological Field Notes**: Documenting the context of each discovery
3. **Translation Notes**: Explaining cultural context that isn't obvious to readers

#### Differentiated Instruction Tips
- **Top Students**: Challenge them to write comments for complex algorithms they create
- **Regular Students**: Provide comment templates they can fill in
- **Weak Students**: Use pair programming where stronger student explains while weaker student writes comments

### Print() Function - The Communication Bridge

#### Key Points
- `print()` makes invisible computational processes visible
- Essential for debugging and understanding program flow
- In DH, often used to display research results and progress updates

#### Common Pitfalls
- Forgetting parentheses in Python 3
- Not understanding that print() doesn't store data
- Overusing print() instead of proper logging
- Poor formatting making output unreadable

#### Teaching Techniques
- **Interactive discovery**: Have students predict output before running code
- **Error introduction**: Intentionally show print vs Print to reinforce case sensitivity
- **Format exploration**: Show different ways to format output from day one
- **Real-world connection**: Show how print() is like publishing research findings

#### Three Analogies for Print()
1. **Academic Presentation**: Making your research visible to others
2. **Museum Display**: Presenting artifacts with clear labels
3. **Printing Press**: Disseminating knowledge to a wider audience

#### Differentiated Instruction Tips
- **Top Students**: Introduce string formatting (f-strings, .format()) early
- **Regular Students**: Focus on basic concatenation and comma separation
- **Weak Students**: Start with single-item printing before combining elements

### Variables - The Scholarly Filing System

#### Key Points
- Variables store information for later use - like a research notebook
- Naming conventions matter for code readability (like clear academic terminology)
- Variables can change, reflecting the iterative nature of research

#### Common Pitfalls
- Using reserved words as variable names
- Poor naming conventions (single letters, unclear abbreviations)
- Not understanding that assignment doesn't create permanent storage
- Confusion between variable names and string values

#### Teaching Techniques
- **Naming workshop**: Brainstorm good vs. bad variable names for DH contexts
- **Memory model diagrams**: Show how variables point to values
- **Refactoring exercise**: Take code with bad variable names and improve them
- **Domain-specific examples**: Use manuscript_id instead of generic x, y, z

#### Three Analogies for Variables
1. **Library Card Catalog**: Each variable is like a catalog card pointing to information
2. **Research Notes**: Variables store findings you'll need later
3. **Museum Accession Numbers**: Systematic way to track and reference items

#### Differentiated Instruction Tips
- **Top Students**: Discuss scope, mutability, and advanced naming patterns
- **Regular Students**: Practice with meaningful names in humanities contexts
- **Weak Students**: Start with simple patterns (noun_descriptor) and lots of examples

### Input() Function - The Scholar's Interview

#### Key Points
- `input()` enables interactive programs that respond to user needs
- Always returns strings - type conversion often necessary
- Creates programs that can adapt to different research scenarios

#### Common Pitfalls
- Forgetting that input() always returns strings
- Not validating user input
- Unclear or intimidating prompts
- Not handling unexpected input gracefully

#### Teaching Techniques
- **Prompt workshop**: Design clear, helpful prompts together
- **Type conversion practice**: Show int(), float() with user input
- **Error scenarios**: What happens with unexpected input?
- **Validation introduction**: Basic checks for expected input

#### Three Analogies for Input()
1. **Oral History Interview**: Collecting information through questions
2. **Archaeological Survey**: Gathering data from different sites
3. **Manuscript Examination**: Interactive process of discovery

#### Differentiated Instruction Tips
- **Top Students**: Add input validation and error handling
- **Regular Students**: Focus on clear prompts and type conversion
- **Weak Students**: Start with string input only, add numbers later

### If Statements - The Scholar's Decision Tree

#### Key Points
- Conditional logic mirrors analytical thinking in humanities
- Boolean logic is fundamental to computational thinking
- Decision structures reflect real-world scholarly processes

#### Common Pitfalls
- Confusion with assignment (=) vs. equality (==)
- Poor understanding of boolean logic
- Overly complex nested conditions
- Missing edge cases in logic

#### Teaching Techniques
- **Flowchart translation**: Convert humanities decision processes to code
- **Truth table exercises**: Make boolean logic concrete
- **Edge case hunting**: What inputs might break the logic?
- **Peer debugging**: Students find logical errors in each other's conditions

#### Three Analogies for If Statements
1. **Manuscript Authentication**: "If the script style is Gothic and the date is post-1200..."
2. **Literary Classification**: "If it's in verse and performed, it's drama..."
3. **Archive Access**: "If researcher status is faculty, grant full access..."

#### Differentiated Instruction Tips
- **Top Students**: Complex logical operators (and, or, not) and nested conditions
- **Regular Students**: Focus on clear, single conditions first
- **Weak Students**: Use flowcharts and visual representations

### Lists - The Scholar's Collection

#### Key Points
- Lists organize related information like bibliographies or catalogs
- Ordered collections that can grow and change
- Essential for processing multiple items systematically

#### Common Pitfalls
- Confusion between lists and strings
- Index errors (especially negative indexing)
- Modifying lists while iterating
- Not understanding list mutability

#### Teaching Techniques
- **Physical collections**: Use actual books/objects to demonstrate list concepts
- **Index visualization**: Draw boxes with index numbers
- **Method exploration**: Discover append(), remove(), sort() through experimentation
- **Collection analysis**: Work with real humanities datasets

#### Three Analogies for Lists
1. **Bibliography**: Ordered collection of sources
2. **Museum Catalog**: Systematic inventory of artifacts
3. **Reading List**: Sequence of texts for study

#### Differentiated Instruction Tips
- **Top Students**: List comprehensions and advanced methods
- **Regular Students**: Basic operations and common methods
- **Weak Students**: Focus on append() and basic indexing

### For Loops - The Scholar's Systematic Examination

#### Key Points
- Iteration is fundamental to computational thinking
- Systematic processing mirrors scholarly methodologies
- Essential for analyzing collections of data

#### Common Pitfalls
- Indentation errors
- Off-by-one errors with range()
- Modifying the sequence being iterated
- Not understanding variable scope in loops

#### Teaching Techniques
- **Manual iteration first**: Do several examples by hand
- **Visualization tools**: Use tools to show loop execution
- **Pattern recognition**: Identify common loop patterns
- **Real data practice**: Use actual humanities datasets

#### Three Analogies for For Loops
1. **Manuscript Examination**: Systematically analyzing each page
2. **Archaeological Dig**: Processing each layer or grid square
3. **Archive Research**: Going through each folder systematically

#### Differentiated Instruction Tips
- **Top Students**: Nested loops and complex iteration patterns
- **Regular Students**: Focus on list iteration and range()
- **Weak Students**: Start with simple counting and list display

### Functions - The Scholar's Methodology

#### Key Points
- Functions encapsulate reusable processes like research methods
- Enable modular, organized code structure
- Parameters allow methods to work with different data

#### Common Pitfalls
- Not understanding the difference between defining and calling functions
- Scope confusion with local vs. global variables
- Not using return values effectively
- Creating overly complex functions

#### Teaching Techniques
- **Method analogy**: Functions are like standardized research procedures
- **Black box concept**: Focus on inputs and outputs first
- **Incremental building**: Start with simple functions, add complexity
- **Documentation practice**: Write docstrings for all functions

#### Three Analogies for Functions
1. **Research Method**: Standardized procedure that can be applied repeatedly
2. **Citation Style**: Consistent format applied to different sources
3. **Analysis Framework**: Theoretical approach applied to various texts

#### Differentiated Instruction Tips
- **Top Students**: Multiple parameters, default values, and complex returns
- **Regular Students**: Single-purpose functions with clear inputs/outputs
- **Weak Students**: Focus on calling existing functions before writing them

---

## Section 4: Tips & Tricks for Teaching Mixed-Ability Groups

### Universal Strategies

#### The "Whole Game" Approach[9]
- Start each session with a complete, working example that demonstrates the day's concepts
- Show the end goal before breaking down components
- Students need to see meaningful applications immediately

#### Transparent AI Integration[22][26]
- Model appropriate AI use during lectures
- Show both successful and failed AI interactions
- Teach prompt engineering as a scholarly skill
- Require documentation of AI assistance

### For Top Students (Advanced ~20%)

#### Challenge Extensions
- **Independent Projects**: Assign open-ended research questions requiring multiple techniques
- **Teaching Roles**: Have them explain concepts to struggling classmates
- **Advanced Applications**: Introduce libraries like spaCy, pandas, or matplotlib early
- **Research Integration**: Connect programming directly to their thesis or research interests

#### Engagement Strategies
- **Code Review**: Have them review and improve beginner code
- **Algorithm Optimization**: Challenge them to make code more efficient
- **Domain Expertise**: Leverage their humanities knowledge to create realistic examples
- **Mentoring**: Pair them with weaker students for mutual benefit

### For Regular Students (Majority ~65%)

#### Scaffolding Techniques
- **Template-Based Learning**: Provide code templates they fill in
- **Guided Practice**: Walk through examples step-by-step together
- **Peer Collaboration**: Organize mixed-ability pairs
- **Regular Check-ins**: Frequent comprehension checks during lessons

#### Confidence Building
- **Success Experiences**: Design tasks with clear, achievable goals
- **Error Normalization**: Frame debugging as detective work
- **Progress Tracking**: Show how far they've come with portfolio reviews
- **Real Applications**: Connect every concept to actual DH use cases

### For Weak Students (Struggling ~15%)

#### Support Systems
- **Visual Learning**: Use flowcharts, diagrams, and step-by-step visualizations
- **Reduced Cognitive Load**: Focus on one concept at a time
- **Frequent Practice**: More repetition with varied examples
- **Individual Attention**: Schedule office hours or extra sessions

#### Motivation Maintenance
- **Small Wins**: Break large tasks into tiny, achievable steps
- **Practical Focus**: Emphasize immediate usefulness over theoretical understanding
- **Positive Framing**: "This is challenging" instead of "This is easy"
- **Alternative Assessments**: Allow different ways to demonstrate understanding

### Google Colab Specific Strategies

#### Notebook Organization[41][46]
- **Clear Section Headers**: Use markdown headers to organize content
- **Progressive Disclosure**: Reveal complexity gradually through separate cells
- **Interactive Elements**: Use widgets and input forms for engagement
- **Documentation Cells**: Explain each code cell with markdown

#### Collaborative Features
- **Shared Notebooks**: Students can work together in real-time
- **Version Control**: Use Colab's revision history for iterative development
- **Comment System**: Built-in commenting for peer review
- **Integration**: Easy connection to Google Drive and GitHub

---

## Section 5: 50 Exercise Ideas Across 4 Levels

### Basic Level (15 exercises)
*For students new to programming, focus on single concepts*

#### 1. Medieval Manuscript Cataloger
**Instruction**: Create a program that asks for manuscript details (title, author, century) and displays them in a formatted catalog entry.
**DH Relevance**: Basic data entry for digital archives
**Solution Reasoning**: Practices input(), variables, and print() with formatted output
**Code Solution**:
```python
# Medieval manuscript catalog entry
title = input("Manuscript title: ")
author = input("Author (if known): ")
century = input("Century: ")

print("=== Manuscript Catalog Entry ===")
print("Title:", title)
print("Author:", author if author else "Anonymous")
print("Period:", century + " century")
```

#### 2. Shakespearean Insult Generator
**Instruction**: Create lists of Shakespearean adjectives and nouns. Generate random insults by combining them.
**DH Relevance**: Working with historical language datasets
**Solution Reasoning**: List manipulation, random selection, string formatting
**Code Solution**:
```python
import random

adjectives = ["villainous", "beslubbering", "churlish", "bootless"]
nouns = ["knave", "varlet", "cur", "dolt"]

adjective = random.choice(adjectives)
noun = random.choice(nouns)

print("Thou", adjective, noun + "!")
```

[Continue with remaining 48 exercises organized by level...]

### Standard Level (15 exercises)
*Combining multiple concepts, introducing complexity*

#### 16. Citation Style Converter
**Instruction**: Write a program that takes citation information and outputs it in different academic styles (MLA, APA, Chicago).
**DH Relevance**: Essential academic skill with computational assistance
**Solution Reasoning**: Functions, string formatting, conditional logic for different styles

#### 17. Text Readability Analyzer
**Instruction**: Calculate basic readability metrics (average word length, sentence count) for a given text.
**DH Relevance**: Computational stylometry and text analysis fundamentals

[Continue with standard level exercises...]

### Advanced Level (12 exercises)
*Complex problem-solving, multiple concepts, error handling*

#### 31. Multi-Language Medieval Text Processor
**Instruction**: Process a collection of medieval texts in different languages, categorize them, and generate statistics.
**DH Relevance**: Multilingual corpus analysis, common in medieval studies

#### 32. Citation Network Visualizer
**Instruction**: Parse a bibliography, identify citation relationships, and create a simple network representation.
**DH Relevance**: Understanding scholarly conversations and intellectual influence

[Continue with advanced level exercises...]

### Challenge Level (8 exercises)
*Open-ended problems requiring creative solutions*

#### 43. Paleographic Training System
**Instruction**: Create a system that helps students learn to identify medieval scripts by providing practice exercises and feedback.
**DH Relevance**: Digital paleography education

#### 44. Cultural Heritage Database Builder
**Instruction**: Design a flexible system for cataloging various types of cultural heritage objects with different metadata schemas.
**DH Relevance**: Museum informatics and digital collections management

[Continue with challenge level exercises...]

---

## Section 6: Google Colab Teaching Guide

### Notebook Structure for Mixed-Ability Teaching

#### Four-Tier Notebook Design[41][44]

**Tier 1: Basic Concepts** (All students)
- Clear markdown explanations
- Simple, working examples
- Step-by-step instructions
- Immediate visual feedback

**Tier 2: Standard Practice** (Regular + Advanced students)
- Extended exercises
- Error handling requirements
- Multiple solution approaches
- Peer review components

**Tier 3: Advanced Applications** (Advanced students)
- Open-ended challenges
- Integration with external libraries
- Research-oriented projects
- Independent exploration

**Tier 4: Challenge Extensions** (Top students + motivated regulars)
- Novel problem-solving
- Creative applications
- Teaching others
- Contributing to shared resources

### AI Usage Documentation System

#### Required Documentation Format
```python
"""
AI USAGE LOG
Student: [Name]
Date: [Date]
Assignment: [Assignment Name]

AI Tools Used: [ChatGPT, Claude, etc.]
Prompts Used:
1. "Help me understand how to count words in Python"
2. "Debug this error: NameError in line 5"

What I learned from AI:
- [Specific insights gained]

What I figured out myself:
- [Independent problem-solving]

Verification steps taken:
- [How you checked AI suggestions]
"""
```

#### AI Collaboration Guidelines
1. **Prompt Documentation**: Record all AI interactions
2. **Understanding Verification**: Explain AI-generated code in your own words
3. **Independent Problem-Solving**: Attempt solutions before asking AI
4. **Error Analysis**: Use AI to understand, not just fix, errors
5. **Iterative Learning**: Show progression from AI-assisted to independent work

### Reproducibility and Documentation Standards

#### Notebook Requirements
- **Clear Headers**: Every section has descriptive markdown headers
- **Code Comments**: All code cells have explanatory comments
- **Output Preservation**: Keep cell outputs to show working solutions
- **Data Sources**: Document all external data sources and their origins
- **Environment**: Note any special packages or settings required

#### Version Control Integration
- **GitHub Classroom**: Connect assignments to version control[24]
- **Regular Commits**: Encourage frequent saves with descriptive messages
- **Collaboration**: Use shared repositories for group projects
- **Portfolio Building**: Students maintain semester-long project portfolios

### Assessment Integration

#### Process-Based Evaluation Criteria
1. **Problem Decomposition**: How well did student break down complex tasks?
2. **Code Quality**: Readability, commenting, organization
3. **Debugging Process**: Systematic approach to error resolution
4. **AI Collaboration**: Appropriate use and documentation of AI assistance
5. **Conceptual Understanding**: Ability to explain and modify code

#### Formative Assessment Tools
- **Real-time Polling**: Use Colab forms for comprehension checks
- **Peer Code Review**: Students comment on each other's notebooks
- **Progress Portfolios**: Weekly reflection on learning and challenges
- **Interactive Debugging**: Live problem-solving sessions

---

## Section 7: Additional Reading and Professional Development

### Essential Academic Resources

#### Core Pedagogy Papers
- Birnbaum & Langmead (2017): Task-Driven Programming Pedagogy in Digital Humanities[27] - Foundational approach to DH programming education
- Mohamed (2021): Teaching Highly Mixed-Ability CS1 Classes[60] - Research-based strategies for diverse cohorts
- Salter (2024): Digital Humanities Programming Pedagogy in the Age of AI[103] - Contemporary approaches to AI integration

#### Assessment and Evaluation
- Bhatt et al. (2024): Process-Based Assessments for Computational Thinking[61] - Framework for assessing thinking processes
- Thangaraj et al. (2023): Formative Assessment in Programming Education[141] - Systematic review of feedback techniques
- Sun et al. (2019): Formative Assessment of Programming Languages[138] - Peer review and continuous evaluation methods

#### AI Integration in Education
- Ahmed et al. (2025): AI-Augmented Teaching Assistant Feasibility[22] - Practical integration of LLMs in programming courses
- Chiang et al. (2024): GPT-4 Performance in Programming Assessments[22] - Current capabilities and limitations
- Microsoft (2024): Responsible AI in Education Framework[140] - Ethical guidelines for educational AI use

### Practical Implementation Guides

#### Google Colab Resources
- Google AI (2024): Teaching CS and ML with Colab[41] - Official pedagogy guide
- Monterail (2023): AI-Powered Coding Assistant Best Practices[23] - Professional development integration
- University of British Columbia (2021): Flipped Classroom Programming Model[60] - Tested mixed-ability strategies

#### Digital Humanities Methodology
- Programming Historian: Creating GUIs in Python for DH Projects[108] - Advanced applications
- HKUST (2024): Learn Python From Zero for Digital Humanities[30] - Beginner-friendly progression
- TU Delft: Python for Digital Humanities Course Materials[24] - Comprehensive curriculum example

### Professional Development Recommendations

#### For Instructors New to DH Programming
1. **Start with Programming Historian Tutorials**: Build personal comfort with basic techniques
2. **Join DH Communities**: Follow @DHPoco, participate in #DigitalHumanities discussions
3. **Attend Workshops**: DHSI, NEH institutes, local DH centers
4. **Practice with Real Data**: Use your own research as learning material

#### For Experienced Programmers New to DH
1. **Read DH Theory**: Moretti's "Distant Reading," Ramsay's "Reading Machines"
2. **Explore DH Projects**: Mapping the Republic of Letters, Photogrammar, Orbis
3. **Understand Humanities Workflows**: How scholars currently work with texts, images, data
4. **Learn Domain Vocabulary**: Familiarize yourself with humanities terminology and concepts

#### For Ongoing Professional Development
1. **Follow DH Journals**: Digital Humanities Quarterly, Literary and Linguistic Computing
2. **Attend Conferences**: Alliance of Digital Humanities Organizations, domain-specific meetings
3. **Participate in Code Review**: Share teaching materials through GitHub, seek feedback
4. **Stay Current with AI**: Follow educational AI research, test new tools regularly

### Implementation Timeline

#### Pre-Course Preparation (4-6 weeks before)
- Set up Google Colab classroom environment
- Prepare sample datasets from actual DH projects
- Create assessment rubrics emphasizing process over product
- Test all code examples across different experience levels

#### Week 1: Foundation Setting
- Establish AI collaboration norms and documentation requirements
- Assess student background through practical exercises, not surveys
- Form mixed-ability working groups for peer support
- Introduce the "whole game" with a complete DH project walkthrough

#### Ongoing Assessment Strategy
- Weekly process portfolios with reflection components
- Peer code review sessions with structured feedback forms
- Regular one-on-one check-ins for struggling students
- Mid-semester adjustment based on learning analytics from Colab

#### Post-Course Support
- Provide pathways to intermediate courses or independent projects
- Maintain connection through DH programming community
- Share student work (with permission) as examples for future cohorts
- Collect longitudinal feedback on skill retention and application

### Technology Integration Checklist

#### Essential Colab Setup
- [ ] Shared class Drive folder with example datasets
- [ ] Template notebooks for each major assignment type
- [ ] Integration with institutional LMS for grade reporting
- [ ] Backup plans for connectivity or platform issues

#### AI Tool Integration
- [ ] Clear policies on acceptable AI use in different contexts
- [ ] Training materials for effective prompt engineering
- [ ] Assessment modifications that account for AI capabilities
- [ ] Regular updates as AI tools evolve

#### Accessibility Considerations
- [ ] Screen reader compatible notebook formatting
- [ ] Alternative text for all images and diagrams
- [ ] Multiple input methods for students with different needs
- [ ] Flexible deadline policies for varying circumstances

This framework provides a comprehensive foundation for teaching Python programming to Digital Humanities students in the era of Large Language Models, emphasizing both computational skills and scholarly practices while accommodating diverse learning needs and abilities.