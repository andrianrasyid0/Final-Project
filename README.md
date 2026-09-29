<center><img src ="Gambar/M. Rasyid Andrian.png"><img></center>

# Final Project
Final Project Data Analyst & Business Intelligent tentang "Analisa performa & resiko pembayaran customer loan" , ingin melihat apa saja faktor - faktor yang menyebabkan customer berhenti membayar angsuran 
## Sumber data
Data diambil dari [kaggel](https://www.kaggle.com/datasets/vivekmali1436/banking-transactions-dataset?select=card_transactions.csv)

## Business Questions
Business Questions : 
1. Bagaimana customer dapat dikelompokkan berdasarkan income?
2. Bagaimana karakteristik customer berdasarkan loan behavior?
3. Bagaimana customer dikelompokkan berdasarkan payment behavior?
4. Bagaimana distribusi customer berdasarkan status dan loan type?
5. Strategi apa yang dapat diterapkan untuk setiap segment?

## Data Preparation
Data Cleaning :
- Cek data duplicated
- Cek missing value
- Mengubah tipe data kolom date_of_birth, join_date dan starat_date dari Object menjadi datetime
  
Data Transformation :
- Merge data  : customers customer_id(pk) on loans customer_id(fk) -> loans loan_id(pk) on loan_payments loan_id(fk)
  
Feature Engineering :
- Create columns : - remaining_balance(sisa pinjaman), age(umur), credit_category(very poor,poor,fair,good,excellent),due_date(jatuh tempo 30 setelah start_date)

Output :
- Dataset final : 18384 customer 
- Clustering income,loan,payment ,city,state dan status+loan type
- Ready to Exmplore
