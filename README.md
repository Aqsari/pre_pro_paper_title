Berikut merupakan hasil pengambilan data judul penelitan pada google scholar.

Pengambilan data ini menggunakan query : '("Generative" OR "Conversational") OR ("Emotional" OR "Emotion") AND ("Chatbot" OR "Chat" OR "Agent")'

Data yang simpan dalam file CSV hanya yang dipublikasi pada tahun 2020-2025.

Data yang di simpan sejumlah 415 data judul paper.

Text Cleaning yang dilakukan
        
        Beberapa tahap text cleaning yang dilakukan:

        Lowercasing: Mengubah teks menjadi huruf kecil.

        Removing Punctuation & Special Characters: Menghapus tanda baca.

        Removing Numbers: Menghapus angka dari teks.

        Tokenization: Memisahkan teks menjadi kata-kata.

        Stopword Removal: Menghapus kata-kata umum yang tidak memiliki makna penting.

        Lemmatization: Mengubah kata menjadi bentuk dasarnya.


Dari data yang sudah dilakukan proses Cleaning diperoleh hasil:

        📊 20 Kata Paling Sering Muncul:

                conversational: 283

                agent: 226

                generative: 96

                chatbot: 70

                ai: 59

                using: 38

                chat: 32

                learning: 31

                model: 31

                artificial: 30

                intelligence: 28

                health: 27

                emotion: 25

                study: 25

                chatgpt: 25

                emotional: 24

                system: 23

                interaction: 23

                user: 23

                support: 22


Named Entity Recognition

Named Entity Recognition (NER) adalah teknik dalam pemrosesan bahasa alami (NLP) yang bertujuan untuk mengidentifikasi dan mengklasifikasikan entitas bernama dalam teks ke dalam kategori yang telah ditentukan, seperti nama orang, organisasi, lokasi, tanggal, dan lainnya. Dalam penelitian ini, kami menggunakan **NLTK’s ne_chunk** untuk melakukan identifikasi entitas dalam dataset judul penelitian yang telah dibersihkan.

✅ Named Entity Recognition selesai! Hasil disimpan di 'ner_output_nltk.csv'.

                                               Title Named_Entities

0  enjoy writing playing personalized emotion gro...             []

1  teaching student conversational ai using convo...             []

2    towards online empathetic chatbot emotion cause             []

3  compeer generative conversational agent proact...             []

4  conversational aichatbot architecture evaluati...             []



TF-IDF

TF-IDF (Term Frequency-Inverse Document Frequency) adalah salah satu teknik yang digunakan untuk mengukur pentingnya sebuah kata dalam dokumen relatif terhadap koleksi dokumen (korpus). Dalam konteks teks, TF-IDF membantu menilai kata-kata yang paling relevan dengan konteks tertentu berdasarkan frekuensinya di dalam dokumen serta distribusinya dalam seluruh korpus. `TfidfVectorizer` dari library `sklearn.feature_extraction.text` menyediakan cara yang efisien untuk menghitung nilai TF-IDF. Metode ini bekerja dengan dua langkah utama: pertama, menghitung frekuensi kata dalam dokumen (TF), dan kedua, menghitung invers frekuensi kata tersebut di seluruh koleksi dokumen (IDF). Dengan demikian, kata-kata yang sering muncul dalam dokumen namun jarang di seluruh koleksi dokumen diberi bobot lebih tinggi, yang menunjukkan relevansinya. Penggunaan `TfidfVectorizer` memungkinkan representasi teks numerik, sehingga dapat digunakan dalam model pembelajaran mesin seperti klasifikasi dan clustering teks. Teknik ini banyak digunakan dalam pemrosesan bahasa alami (NLP) untuk ekstraksi fitur teks.


✅ Proses TF-IDF selesai! Hasil disimpan di 'tfidf_output.csv'.
                                               Title  ability  abstract  \
0  enjoy writing playing personalized emotion gro...      0.0       0.0   
1  teaching student conversational ai using convo...      0.0       0.0   
2    towards online empathetic chatbot emotion cause      0.0       0.0   
3  compeer generative conversational agent proact...      0.0       0.0   
4  conversational aichatbot architecture evaluati...      0.0       0.0   

   abuse  academic  acceleration  acceptability  acceptance  accounting  \
0    0.0       0.0           0.0            0.0         0.0         0.0   
1    0.0       0.0           0.0            0.0         0.0         0.0   
2    0.0       0.0           0.0            0.0         0.0         0.0   
3    0.0       0.0           0.0            0.0         0.0         0.0   
4    0.0       0.0           0.0            0.0         0.0         0.0   

   accuracy  ...  worker  workplace  write   writing  writingtolearn  written  \
0       0.0  ...     0.0        0.0    0.0  0.374895             0.0      0.0   
1       0.0  ...     0.0        0.0    0.0  0.000000             0.0      0.0   
2       0.0  ...     0.0        0.0    0.0  0.000000             0.0      0.0   
3       0.0  ...     0.0        0.0    0.0  0.000000             0.0      0.0   
4       0.0  ...     0.0        0.0    0.0  0.000000             0.0      0.0   

   wysa  young  youobservers  zhorai  
0   0.0    0.0           0.0     0.0  
1   0.0    0.0           0.0     0.0  
2   0.0    0.0           0.0     0.0  
3   0.0    0.0           0.0     0.0  
4   0.0    0.0           0.0     0.0  

[5 rows x 1264 columns]

