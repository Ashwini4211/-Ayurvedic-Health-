# ayurvedic_diagnosis.py

# Dictionary of common symptoms and Ayurvedic remedies
ayurveda_remedies = {
    "headache": {
        "cause": "Pitta imbalance",
        "remedy": "Apply sandalwood paste or drink coriander tea"
    },
    "cold": {
        "cause": "Kapha imbalance",
        "remedy": "Take ginger tea with honey, avoid dairy"
    },
    "acidity": {
        "cause": "Pitta excess",
        "remedy": "Drink aloe vera juice, avoid spicy food"
    },
    "constipation": {
        "cause": "Vata imbalance",
        "remedy": "Drink warm water, eat soaked raisins, use Triphala"
    },
    "fatigue": {
        "cause": "Vata-Pitta imbalance",
        "remedy": "Ashwagandha supplements, oil massage"
    },
    "skin rash": {
        "cause": "Pitta excess",
        "remedy": "Apply neem paste, drink turmeric milk"
    }
}

# Function to check symptoms
def suggest_ayurvedic_remedy(symptom):
    symptom = symptom.lower().strip()
    if symptom in ayurveda_remedies:
        info = ayurveda_remedies[symptom]
        return f"""
Symptom: {symptom.title()}
Possible Cause (Dosha Imbalance): {info['cause']}
Suggested Remedy: {info['remedy']}
"""
    else:
        return "Symptom not found in the database. Please consult an Ayurvedic doctor."

# Demo: Simulated user input (can be replaced with real input in GUI or web app)
if __name__ == "__main__":
    print("🧘‍♀️ Welcome to the Ayurvedic Symptom Checker 🩺\n")
    symptoms = ["headache", "fatigue", "back pain"]  # Simulated inputs
    for s in symptoms:
        print(suggest_ayurvedic_remedy(s))
