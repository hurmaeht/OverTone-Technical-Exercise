# OverTone-Technical-Exercise
### README

#### Exercise 1 - Checking for synonyms where a=b and a=c but b != c

This exercise checks if two sentences are equivalent by considering direct synonyms only, without transitive relationships. That means if a word has two different synonyms, these synonyms are not considered synonymous with each other.

##### Code Explanation:

1. **Define Synonym Pairs:**
   - `synonym_pairs` contains pairs of synonyms like ("eat", "consume") and ("coach", "bus").

2. **User Input:**
   - `sentence1` and `sentence2` are taken as input from the user.

3. **Function: are_synonyms:**
   - This function checks if two words are same word.
   - If words are identical, returns True.
   - Looks through `synonym_pairs` to check if the words match any pair.

4. **Function: sentences_are_equivalent:**
   - Splits the sentences into lists of words.
   - Checks if the number of words is the same in both sentences.
   - Compares each word pair using `are_synonyms` function.
   - If all word pairs are synonymous, returns True.

5. **Check Sentence Equivalence:**
   - Uses `sentences_are_equivalent` to determine if the sentences are equivalent and prints the result.

#### Exercise 2 - Checking for synonyms where a=b, b=c hence a=c

This exercise checks if two sentences are equivalent by considering transitive relationship. That means if a word is a synonym of another word, and that word is a synonym of a third word, all three words are considered synonymous.

##### Code Explanation:

1. **Define Synonym Pairs:**
   - `synonym_pairs` contains pairs of synonyms like ("eat", "consume") and ("consume", "devour").

2. **User Input:**
   - `sentence1` and `sentence2` are taken as input from the user.

3. **Function: are_direct_synonyms:**
   - This function checks if two words are same word.
   - If words are identical, returns True.
   - Looks through `synonym_pairs` to check if the words match any pair.

4. **Function: build_synonym_groups:**
   - Groups all synonyms together.
   - Uses sets to combine all related words into synonym groups.

5. **Function: are_transitive_synonyms:**
   - Checks if two words are in the same synonym group, using `build_synonym_groups`.
   - Returns True if they are synonyms, False otherwise.

6. **Function: sentences_are_equivalent:**
   - Splits the sentences into lists of words.
   - Checks if the number of words is the same in both sentences.
   - Builds synonym groups from `synonym_pairs`.
   - Compares each word pair using `are_transitive_synonyms` function.
   - If all word pairs are synonymous, returns True.

7. **Check Sentence Equivalence:**
   - Uses `sentences_are_equivalent` to determine if the sentences are equivalent and prints the result.

### How to Use

- **For Exercise 1:**
  - Run the script.
  - Enter two sentences to compare.
  - The program checks if the sentences are equivalent considering only direct synonyms.

- **For Exercise 2:**
  - Run the script.
  - Enter two sentences to compare.
  - The program checks if the sentences are equivalent considering transitive synonyms.
