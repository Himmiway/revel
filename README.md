# revel
from fpdf import FPDF

# Create the PDF scene sheet and song layout
class PDF(FPDF):
    def header(self):
        self.set_font("Arial", "B", 14)
        self.cell(0, 10, "Scene 6 – Comedic Remix: 'Like Rabbits'", ln=True, align="C")
        self.ln(5)

    def chapter_title(self, title):
        self.set_font("Arial", "B", 12)
        self.set_text_color(30, 30, 120)
        self.cell(0, 10, title, ln=True)
        self.set_text_color(0, 0, 0)
        self.ln(2)

    def chapter_body(self, text):
        self.set_font("Arial", "", 11)
        self.multi_cell(0, 8, text)
        self.ln()

# Scene and beat layout content
scene_text = """
[Scene Begins – Malcolm at the grave]

MALCOLM:
Charity, my sweet. I’ll miss you always…
(Spots a woman walking past)
Oop—hold up, Jesus done sent me an upgrade. (Snatches flowers off grave)
Say there, beautiful! I just promised myself—if I saw a fine woman today,
I’d give her these flowers… so here ya go!

NANCY (side-eyeing):
You stole those off a grave, didn’t you?

MALCOLM:
Grave? Nah, I’m just recycling memories. I’m Malcolm, by the way.

NANCY:
Nancy. Revels.

MALCOLM:
A Revels? Girl, we ‘bout to break the census.
"""

song_text = """
[Song: "Like Rabbits (Comedic Remix)"]

CHORUS:
🎵 Did you hear about Malcolm down that dusty lane?
Got one baby, then two—Lord, here comes twins again!
They multiplying like a math test from hell—
Whole town looking like his personnel! 🎵

CHORUS WOMAN 1:
That boy Malcolm? Chile please… he done turned his house into a daycare!

CHORUS MAN:
Last time I went over there, a baby opened the door talkin’ bout, “He busy!”

CHORUS:
🎵 And growing… AND GROWING! AND GROWING!
They spreading like rabbits, we ain't joking! 🎵

[Call & Response, dancing and clapping]

CHORUS:
🎵 That boy Malcolm, son of Owen…
Definitely knew what he was sowin'.
Had so many Revels, even he stopped knowin’
Names, birthdays—he started just throwin… 🎵

MALCOLM:
Girl, I got love and a crib with twenty beds…
Might not be rich, but I got strong meds!
These kids runnin’ wild like they on Red Bull—
One more baby, we gon’ need a school!

[Song Ends with all Chorus in unison, laughing]
CHORUS:
MALCOLM REVELS—KING OF THE CRIBS!
"""

beat_layout = """
[Beat Layout – "Like Rabbits (Comedic Remix)"]

Intro: Light theatrical piano with upright bass & snare taps (comedic jazz energy)
Verse 1 (Chorus): New Orleans-style bounce rhythm, snare-driven with quirky horns
Spoken Dialogue: Minimal underscore with upright bass walking line
Verse 2 (Malcolm): Funk rhythm kicks in with synth bass, layered handclaps, humorous strings
Call & Response: Tempo picks up, gospel harmonies enter (children’s choir feel)
Bridge: Swing-breakbeat fusion, tempo slows down slightly for punchline delivery
Final Chorus: Full band – brass, drums, organ, vocal stack – energy peaking
Outro: Big band-style comedic stinger with a cartoon “BOING” sound effect

Optional FX:
- Baby giggles
- Rattles or bottle sound for transitions
- Whispered “Dada” for comedic punctuation
"""

# Create PDF
pdf = PDF()
pdf.add_page()
pdf.chapter_title("Comedic Scene Rewrite")
pdf.chapter_body(scene_text)
pdf.chapter_title("Song: 'Like Rabbits (Comedic Remix)'")
pdf.chapter_body(song_text)
pdf.chapter_title("Beat Layout & Song Transitions")
pdf.chapter_body(beat_layout)

# Output PDF
output_path = "/mnt/data/Like_Rabbits_Comedic_Remix_Scene.pdf"
pdf.output(output_path)
output_path
