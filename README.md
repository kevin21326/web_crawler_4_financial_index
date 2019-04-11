# web_crawler_4_financial_index
A web crawling tutorial using Anaconda as coding environment

如果要增加zh-NER-TF自己的訓練集，要在其main.py的程式加入下面mode，這樣它會用內建在data.py的vocab_build方法幫你新增的文字建立id在word2id.pkl檔案中，

elif args.mode == 'update_training_set':
	print('update training set')
	print(train_path)
	vocab_path = os.path.join('.', args.train_data, 'word2id.pkl')
	vocab_build(vocab_path,train_path,2)

並在執行訓練前先輸入以下指令:

python main.py --mode=update_training_set
