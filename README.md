# RailsConsoleCommands
CREATE RAILS APP/DATABASE
rails new application_name -TBd postgresql
cd application_name
subl .
#Open the gem file (command p)
#Manually add "pry-rails" to the file and save
bundle
rake db:create
rails g model Student first_name:text last_name:text age:integer
rake db:migrate

TASKS
1) madeline = Student.new(first_name:"Madeline", last_name:"Bagby", age:20)
2) madeline.save
3) madeline.update(first_name:"Myles") or student = Student.find_by_first_name("Madeline"), student.first_name= "Myles"
4) student = Student.find_by_first_name("Myles"), student.destroy
5) validates_uniqueness_of :last_name WRONG
6) validates :first_name :last_name, length: {minimum: 4}
7) validates :first_name :last_name, presence: true
8) rails g migration addFavoriteColorToStudents favorite_color:text
9) student = Student.create(first_name:"John", last_name:"Doe", age:23, favorite_color: "purple")
10) student.valid?
11) student.errors.full_messages.size
12) student= Student.find_by_first_name("John"), student.update(first_name: "Martin", last_name: "Fowler")
13) student.save
14) Student.asll
15) Student.find(128) or Student.fin_by_id(128)
16) Student.first
17) Student.last
18) Student.find_bu_last_name("Fowler")
19) Student.find_by(first_name:"Martin", favorite_color:"red")
20) Student.all.limit(5).offset(2).order(first_name: :asc)
21) Student.find_by_first_name("Martin").destroy
22) Student.destroy.all
