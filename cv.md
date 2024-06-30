# **KSENIYA** PASEKA 
## Contact information:
- Location: Minsk, Belarus
- Phone: +375295045380  
- Email: eseniya.wi@gmail.com
- Discord: cюнечка (@wilamia)
- GitHub: [Kseniya](https://github.com/wilamia)
## Summary
Hardworking programmer ready to start an internship as a Front-End
Developer at a technological corporation. I’m quickly learn new 
information and use this in the future.
## Hard skills
- Python
- C++
- HTML/CSS
- UI/UX design
- Photoshop | Word | Excel | Sony Vegas Pro | Figma | Canva | PowerPoint | AutoCAD | InDesign
## Code examples
- Python
  
```python
import pandas as pd
import numpy as np
data = pd.Series({
    'artist': ['Tayeong', 'Taylor Swift', 'Mr. Bist', 'Lana Del Ray'],
    'dateOfBirth': ['30.12.1995', '13.12.1989', '7.05.1998', '21.06.1985'],
    'country': ['South Korea', 'USA', 'USA', 'USA']})
arrays = [
    np.array(['South Korea', 'USA', 'USA', 'USA']),
    np.array(['Tayeong', 'Taylor Swift', 'Mr. Bist', 'Lana Del Ray']),
    np.array(['30.12.1995', '13.12.1989', '7.05.1998', '21.06.1985']),
]
s = pd.Series(np.random.randn(4), index=arrays)
print(s)
```
- C++

``` C++
System::Void Kursach::Registration::button1_Click(System::Object^ sender, System::EventArgs^ e){
	Admin^ form = gcnew Admin;
	String^ login = maskedTextBox1->Text;
	String^ password = maskedTextBox2->Text;
	Mennu^ form2 = gcnew Mennu;
	SelectLevel^ form3 = gcnew SelectLevel;
	array<Byte>^ dataBytes = Encoding::UTF8->GetBytes(password);
	// Хэширование данных
	SHA512Managed^ sha512 = gcnew SHA512Managed();
	array<Byte>^ hashedData = sha512->ComputeHash(dataBytes);
	// Конвертация хэша в строку
	String^ hashedString = BitConverter::ToString(hashedData)->Replace("-", String::Empty);
	System::String^ connectionString = "Provider=Microsoft.ACE.OLEDB.12.0;Data Source=C:\\Users\\eseni\\OneDrive\\Документы\\MathUsers.accdb";
	OleDbConnection^ dbConnection = gcnew OleDbConnection(connectionString);
	dbConnection->Open();
	if (dbConnection->State != ConnectionState::Open){
		MessageBox::Show("Ошибка открытия соединения с базой данных!", "Ошибка!");
		return System::Void();
	}
	String^ query = "SELECT COUNT(*) FROM [Users] WHERE [Логин] = ?";
	OleDbCommand^ checkCommand = gcnew OleDbCommand(query, dbConnection);
	checkCommand->Parameters->Add("Логин", OleDbType::LongVarWChar)->Value = login;
	checkCommand->Parameters->Add("Пароль", OleDbType::LongVarWChar)->Value = hashedString;
	int count = Convert::ToInt32(checkCommand->ExecuteScalar());
	if (count == 0) {
		MessageBox::Show("Логина не существует или неправильно введён пароль.
Пожалуйста, введите другие значения.", "Ошибка!", MessageBoxButtons::OK, MessageBoxIcon::Error);
		dbConnection->Close();
		return System::Void();
	}
	else if (login == "admin") {
		form->Show();
		Registration::Hide();
		dbConnection->Close();
		return System::Void();
	}
	else {
		form2->loginOfPeople = maskedTextBox1->Text;
		form2->Show();
		Registration::Hide();
		dbConnection->Close();
		return System::Void();
	}
}
```
## Education
**Diploma in Computer Science  
09/2022 – nowadays**  
Minsk Radioengineering College, Belarus
- Specialized in computer programming and digital technologies
- Learned C++, Python, HTML/CSS
- Got skills in drawing different diagrams
- Got qualification of 5th category as operator of electronic computing machine
## Expirience
**Rolling Scopes  
06/2024**  
- Learned how to work with Markdown & Git
- Did a [CV](https://github.com/wilamia/rsschool-cv/blob/gh-pages/cv.md)
## Languages
- Russian - native speaker
- English - B1+
 

