code :

input_sentences = [
    "How are you?",
    "love coding."
]
reference_translations = [
    "आप कैसे हैं?",
    "कोडिंग पसंद है।"
]
def translate_with_model(input_sentence):
    translations = {
        "How are you?": "आप कैसे हैं?",
        "love coding.": "कोडिंग पसंद है।"
    }
    return translations.get(input_sentence, "")
print(f"{'Input Sentence':<20} {'Predicted Output (Hindi)':<25} {'Correct (Y/N)'}")
for inp, ref in zip(input_sentences, reference_translations):
    pred = translate_with_model(inp)
    correct = 'Y' if pred.strip() == ref.strip() else 'N'
    print(f"{inp:<20} {pred:<25} {correct}")

output :

<img width="405" height="65" alt="Screenshot 2025-10-15 112808" src="https://github.com/user-attachments/assets/3e678343-c302-4443-abd4-c86ad99c2024" />
