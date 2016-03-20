Part 1. Run the search engine
step 1. cd code
step 2. ./compile
step 3. ./BuildInvFile
	./DocLen
	./Retrieval
step 4. Choose model:
The program will ask:
-----------------------
|Load Document Lengths|
|Select Model: 	      |
|[1].VSM	      |
|[2].BM25	      |
-----------------------
input 1 or 2 and press ENTER

step 5. 
The program will ask:
------------------------------------------------------
| Type the name of the query file or "_quit" to exit |
------------------------------------------------------
Type in: queryTDN and press ENTER

step 6. After program terminates, there will be result.txt under /code folder. Rename it, for example: VSM_queryTDN.txt

step 7. Choose another model and run step 4-6 again
Rename as BM25_queryTDN.txt

step 8. 
Drag 2 result files:
	VSM_queryTDN.txt
	BM25_queryTDN.txt
to folder ../trec_eval/test
and make sure there is test/judgerobust file

step 9. Run evaluation under ./trec_eval folder:
./trec_eval -a test/judgerobust test/BM25_queryTDN.txt > test/eval_BM25_queryTDN.txt
./trec_eval -a test/judgerobust test/VSM_queryTDN.txt > test/eval_VSM_queryTDN.txt

step 10. Compare between 2 files..








