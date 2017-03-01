# mongodb-query
1. membuat database academic
    use academic

2. Menampilkan semua collection dan data dalam database
    show collections;

3. membuat dan mengaktifkan database
    cara membuat & mengaktifkan database:
      use nama_database;
    cara menampilkan semua database;
      show dbs;

4. membuat collection departement
    db.createCollection("department", {})

5. membuat collection student
    db.createCollection("student", {})

6. melihat struktur student

7. melihat struktur collections

8. menginput 5 data ke dalam collection department
    db.department.insert([
       { code: "001", name: "IT", major: { 1: "sistem informasi", 2: 'sistem jaringan'}  },
       { code: "002", name: "MANAGEMENT", major: { 1: "management informatika", 2: 'management bisns'}  },
       { code: "003", name: "DOCTOR", major: { 1: "doktor anak", 2: 'doktor gigi'}  },
       { code: "004", name: "TEKNIK", major: { 1: "teknik mesin", 2: 'teknik industri'}  },
       { code: "005", name: "AKUNTANSI", major: { 1: "akutansi umum", 2: 'akutansi umum'}  }
    ]);

9. menginput 3 data ke dalam collection student, beserta reference ke department
    db.student.insert([
       { studentId: "001", name: "irsan", address: "jakarta", department: {"$ref": "department", "$id": ObjectId("58b66e78ac5712d33dba8010"), "$db": "academic" }  },
       { studentId: "002", name: "irwin", address: "tangerang", department: {"$ref": "department", "$id": ObjectId("58b66e78ac5712d33dba8013"), "$db": "academic" }  },
       { studentId: "002", name: "daniel", address: "medan", department: {"$ref": "department", "$id": ObjectId("58b66e78ac5712d33dba8014"), "$db": "academic" } }
    ]);
    
