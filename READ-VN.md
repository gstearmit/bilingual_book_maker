# Windows PowerShell
$Env:folder_path='/d/EBOOK_BILINGO-2024/Book/bytebytego' # $folder_path="C:\Users\user\mybook\"
$Env:book_name='System Design Interview - An Insiders Guide (Alex Xu, Sahn Lam) (Z-Library).epub' # $book_name="animal_farm.epub"
$Env:gemini_key='AIzxxxxxxx' # $openai_key="sk-xxx"
$Env:language='vi' # see utils.py



$Env:folder_path='/d/EBOOK_BILINGO-2024/Book/bytebytego'  
$Env:book_name='System Design Interview - An Insiders Guide (Alex Xu, Sahn Lam) (Z-Library).epub'  
$Env:gemini_key='AIzxxxxxxx'  
$Env:language='vi'  

docker run --rm --name bilingual_book_maker --mount type=bind,source=$folder_path,target='/app/test_books' bilingual_book_maker --book_name "/app/test_books/$book_name" --gemini_key $gemini_key --language $language

python make_book.py --book_name  'test_books/System_Design_Interview.epub'  --language 'vi' --gemini_key 'AIzxxxxxxx' --model gemini

python make_book.py --book_name  'test_books/Designing_Data_Intensive.epub'  --language 'vi' --gemini_key 'AIzxxxxxxx' --model gemini

# --- D:\EBOOK_BILINGO-2024\bilingual_book_maker\test_books\ebook-english
## gs : 'AIzxxxxxxx'


python make_book.py --book_name  'test_books/ebook-english/Check_Your_English_Vocabulary_for_TOEIC.epub'  --language 'vi' --gemini_key 'AIzxxxxxxx'  --model gemini

python make_book.py --book_name  'test_books/ebook-english/Skill_for_the_TOEIC_Test_Listening_and_Reading.epub'  --language 'vi' --gemini_key 'AIzxxxxxxx' --model gemini

python make_book.py --book_name  'test_books/System_Design_Interview.epub'  --language 'vi' --gemini_key 'AIzxxxxxxx' --model gemini
