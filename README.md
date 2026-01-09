
Band Name Generator — Day 1 practice.

Asks the user for a city and a favorite letter, then prints a suggested band name.
def generate_band_name(city: str, letter: str) -> str:
    """Return a cleaned, nicely formatted band name from inputs."""
    city = city.strip()
    letter = letter.strip()
    if not city:
        city = "UnknownCity"
    if not letter:
        letter = "X"
    # Capitalize city words and ensure single space between parts
    city = " ".join(word.capitalize() for word in city.split())
    letter = letter.upper()
    return f"{city} {letter}"

def main() -> None:
    print("Welcome to the Band Name Generator.")
    city = input("In which city did you grow up?\n")
    letter = input("What is your favorite letter?\n")
    band_name = generate_band_name(city, letter)
    print(f"Your band name is: {band_name}")

