## Use the right words

The proper use of words is reflected in two aspects: correct use of words and uniform use of words. This section introduces the corresponding specifications in terms of stop words and common words.

### Stop words

Correct use of words means not using offensive stop words. For the forbidden words in technical documents, please refer to ["Forbidden Words in News Reports of Xinhua News Agency (First Batch)" published by Xinhua News Agency in November 2015](https://www.digitaling.com/articles/22975.html) . Although technical documents are not news reports, as mass media in the field of technical communication, the impact of document communication should also be considered. Avoiding offensive words can save an individual or company unnecessary trouble.

The following are some points that are more suitable for technical documents in "Forbidden Words in Xinhua News Reports (First Batch)":

- Do not use words with strong evaluation color such as "best", "best", "famous", "latest technology", "highest level", "state-of-the-art" when reporting various facts, especially products and commodities .
- People with physical disabilities should not use "handicapped", "one-eyed dragon", "blind", "deaf", "fool", "nerd", "mentally handicapped" and other derogatory terms, but should use "disabled", " "Blind", "Deaf", "Intellectually Disabled" and other terms.
- Medical reports must not contain words such as "best curative effect", "radical cure", "safety prevention", "safe and no side effects", and drug reports must not contain "medicine to cure", "invalid refund", "insurance company" "Insurance", "latest technology", "highest technology", "most advanced manufacturing method", "king of medicine", "national new medicine" and other words.
- If the product copy involves multiple regions or availability zones, words involving Chinese territory, sovereignty, Hong Kong, Macao and Taiwan need to be used correctly. for example:
  - Do not mention Taiwan, Hong Kong, Macau and China side by side. For example, "China-Hong Kong", "China-Taiwan" and "China-Australia" should not be used, but "Mainland and Hong Kong", "Mainland and Taiwan" or "Beijing-Hong Kong", "Shanghai-Hong Kong", "Fujian-Taiwan", etc. can be used.
  - It is not recommended to mention a region of China alongside other countries.
- As a national news agency, Xinhua News Agency should not use slang words such as "wow" and "damn", swear words, slang words, etc. in the press release. If such words cannot but be used in quotations, they should be placed in brackets to indicate their connotations. In recent years, the newly created "SB", "TMD", "NB", etc. after abbreviating profanity in Internet language, shall not be used in the report.

### Common words

Common words refer to words that are often used when writing one or a series of technical documents, such as personal pronouns, demonstrative pronouns, modal particles, operational verbs, technical terms, etc.

Various common words must be used correctly in technical documentation. The specific requirements are:

1. Must use the correct "的", "地", "得" and cannot use it indiscriminately.

    - [Correct example 1] The scheduling system will migrate data to other storage nodes. (adjective + + noun)
    - [Correct example 2] The database can use transactions explicitly. (adverb + ground + verb)
    - [Correct example 3] This value should not be adjusted too large. (verb + get + adverb)

2. The content referred to by pronouns such as "it", "the", "this", and "this" must be clearly defined to ensure no ambiguity.

    - [Error example] If you want to build an image of PD, TiKV or TiDB from a locally compiled binary file, you need to leave the `image` field blank.
    - [Correct example] If you want to build an image of PD, TiKV or TiDB from a locally compiled binary file, you need to leave the `image` field of the corresponding image blank.

3. It is not recommended to use words expressing degree and emphasizing tone, because the meaning of such words is usually vague or subjective and absolute, and it is recommended to use specific data or examples instead. For example, the following types of words are recommended to be avoided.

    - Words of degree: more, better, completely, basically, decisive, last, only, fact, noteworthy

        - [Error example] Greatly improved performance.
        - [Analysis] Words such as "very well" have vague and subjective meanings, and are recommended to be replaced with specific data. In addition, the meaning of performance is also relatively broad and can be explained in detail.
        - [Modification suggestion] The performance has been improved by 50% or the delay has been reduced from 10ms to 1ms.

    - Words of quantity: some, very, a lot, some, a little, part, almost, several times, etc.

        - [Error example]... The execution time of the table creation statement will be several times as long as the variable is closed.
        - [Analysis] For users, the meaning of "several times" is very vague, and the difference between three times and eight times is huge. In this case, you can explain the factors that affect the execution time of the table building statement, and give one or two specific examples to illustrate.
        - [Modification suggestion]… The execution time of the table creation statement will be several times as long as when the variable is turned off. The exact number of times depends on the configuration of hardware and PD parameters. For example, when the hardware is … and the PD parameter is configured as …, the execution time of the table creation statement will be … times as long as closing the variable.

4. It is not recommended to use unfamiliar, original or classical Chinese words, and common expressions in modern Chinese should be used.

    - [Error example] This is the only quick start method.
    - [Correct example] These are the only two ways to quickly start.

5. It is forbidden to use too many adjectives to modify nouns.

    - [Error example] To restore the deleted table according to the table name, the first one in the recent historical DDL JOB is a DDL of the DROP TABLE type and the table name of the DROP TABLE is equal to the table name specified in the RECOVER TABLE statement for recovery. .
    - [Analysis] There are too many modified phrases in this sentence, which makes it difficult to read and incomprehensible. In this case, appropriate sentence segmentation is recommended to clarify semantics.
    - [Correct example] The process of restoring a deleted table according to the table name is: first find the latest DDL statement of the DROP TABLE type in the historical DDL JOB, and the table name specified in the DROP TABLE statement is equal to the table name specified in the RECOVER TABLE statement , and then restore the table.

In addition, in the same technical document or in the same series of technical documents, the same words should be used as much as possible to reduce the difficulty of reading comprehension. The specific requirements are:

1. It must be ensured that the personal pronouns are consistent throughout the text, and the personal pronoun cannot be changed repeatedly.

   - It is recommended to use "you" or "you" to refer to the document reader or user, both are acceptable, no mixing is allowed
   - It is recommended to use third-person forms such as "author" and "document author" to refer to the author of the document. It is not recommended to use "I" to refer to the author of the document. This is easy to be subjective and will cause unnecessary doubts in the minds of readers.
   - "We" can be used to refer to the entire company, but it is recommended to use less

2. It is recommended to use the active voice as much as possible instead of the passive voice.

   - [Error example] If this software has not been installed,
   - [Correct example] If this software has not been installed,

[Note] The meaning of **passive sentence** in Chinese is different from that of **passive** in English. In English, the purpose of using the passive is to avoid mentioning the agent, but in Chinese, the quilt often has a passive negative connotation. In addition, the use of active voice in Chinese documents can help to clarify the subject and object of a sentence, which is extremely important for subsequent technical translation work.
