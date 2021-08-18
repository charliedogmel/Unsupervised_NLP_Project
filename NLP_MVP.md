# Song Recommendation System

## Using NMF Text Recommendation

#### Melissa Cooper

Starting with 54356 documents (lyrics of songs) that contain many unique words (or features), I completed a baseline song recommender.

The following are summaries of the first 15 (out of 20) topics:

- Component 1 (topic 1) seems to be about nothing & includes a Spanish word
- Component 2 (topic 2) seems to be about mr world family
- Component 3 (topic 3) seems to be about years and months
- Component 4 (topic 4) seems to be about parents
- Component 5 (topic 5) seems to be about king, allah, thee/thy/thou
- Component 6 (topic 6) seems to be about numbers
- Component 7 (topic 7) seems to be about big guys: denzel, curry, vince
- Component 8 (topic 8) seems to be about ?
- Component 9 (topic 9) seems to be about Spanish names
- Component 10 (topic 10) seems to be about power, men, world, nature
- Component 11 (topic 11) seems to be about industry/capitalism
- Component 12 (topic 12) seems to be about love and French names
- Component 13 (topic 13) seems to be about ? ends of contractions
- Component 14 (topic 14) seems to be about police and law
- Component 15 (topic 15) seems to be about duke/duchess, mme?

So there is a bit more processing to do, including names and non-english words. Also, I need to look into why the preprocessor did not remove numbers or do anything to the 3rd recommendation shown below.


**Here is a song lyric and the first three recommendations:**

  ["We spotted the ocean At the head of the trail Where are we going So far away And somebody told me \
    This is the place Where every thing's better And every thing's safe Walk on the ocean \
    Step on the stones Flesh becomes water Wood becomes bone And half an hour later We packed up our things \
    We said we'd send letters And all those little things They knew we were lying They smiled just the same \
    And it seemed they'd already Forgotten we'd came Walk on the ocean Step on the stones \
    Flesh becomes water Wood becomes bone Walk on the ocean Step on the stones Flesh becomes water \
    Wood becomes bone Back at the homestead Where the air makes you choke People don't know you \
    And trust is a joke Don't even have pictures Just memories to hold Grow sweeter each season \
    As we slowly grow old"]

**1st Recommendation:** 

"It's haunting This hold that you have over me I grow so weak   I see you And everything around you fades And I can't speak  But you can never know what it is you do to me   I can't take what you're doin' to me! I can't take it!  I can't take what you're doin' to me! I can't take it!   No matter what I say or what I do I know how this will end So I'm turning away now before we begin And no matter what you say or what you do I know how this will end So I'm turning away now I'm dangerous for you I'm dangerous for you  You touch me And I can barely make a move And I can't breathe    You can never know what it is you do to me   I can't take what you're doin' to me! I can't take it!  I can't take what you're doin' to me! I can't take it!   No matter what I say or what I do I know how this will end So I'm turning away now before we begin And no matter what you say or what you do I know how this will end So I'm turning away now I'm dangerous  Maria: The only promise I could make you Adrian: Is that my promise is a lie! Maria: The only promise I could make you! Adrian: Is that my promise is a lie!  No matter what I say or what I do I know how this will end So I'm turning away now before we begin And no matter what you say or what you do I know how this will end So I'm turning away now I'm dangerous for you  Maria: I'm dangerous for you! Adrian: I'm dangerous for you Maria: I'm dangerous for you! Adrian: I'm dangerous for you Maria: I'm dangerous for you! Adrian: I'm dangerous for you Maria: I'm dangerous, I'm dangerous for you!  Adrian: My promise is I will hurt you Maria: My promise is I will hurt you Adrian: My promise is I will hurt you Adrian & Maria: My promise is I will hurt you"

**2nd Recommendation:**  

Oh Im getting over being proven wrong And the stories getting so dry And Ill go next if you say you dont mind Well Ill get it right in my own time And I guess youll forgive me Off where the day goes and the nights are Entangled in grievance that nobody sees   Do you feel it better when its your way Do you treat it better when its your move Do you think you need it for your minds sake If I never say a word its all good if I dont   Though youre searching for a motive All the pieces match Out of nowhere But w can get it Hell, I know you It will please you to know   Though the signs I wont see And your words move through me I can give you the melody Never said it was easy But Ill think up a reason To rely on the melody  Do you feel it better when its your way Do you treat it better when its your move Do you think you need it for your minds sake If I never say a word its all good if I dont   Not like you to give in Take one on the chin I want to be somebody like you True, no shit Hey if I never say a word its all good if I dont   We can get it Hell I know you All the pieces match We can get it Out of nowhere Itll please you to know   Never said it was easy But Ill think up a reason Up a motive  Not like you to give in Take one on the chin I want to be somebody like you True, no shit Hey if I never say a word its all good if I dont   Do you feel it better when its your way Do you treat it better when its your move Do you think you need it for your minds sake If I never say a word its all good if I dont

**3rd Recommendation:** 

[Intro]  [Verse 1] You could be happy and I won't know But you weren't happy the day I watched you go And all of the things that I wish I had not said Are played in loops 'til it's madness in my head Is it too late to remind you how we were? Not our last days of silent screamin' blur Most of what I remember makes me sure I should have stopped you from walkin' out the door  [Verse 2] You could be happy, I hope you are You made me happier than I'd been by far Somehow everything I own smells of you And for the tiniest moment it's all not true Do the things that you always wanted to Without me there to hold you back, don't think, just do More than anything I want to see you, girl Take a glorious bite out of the whole world  [Outro]10EmbedShare URLCopyEmbedCopy


```python

```
