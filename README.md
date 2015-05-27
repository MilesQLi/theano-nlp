###train.py
	usage: train.py [-h] [--max-epochs MAX_EPOCHS] [--batch-size BATCH_SIZE]
					[--validation-percent VALIDATION_PERCENT]
					[--checkpoint CHECKPOINT]
					[--improvement-threshold IMPROVEMENT_THRESHOLD]
					[--patience PATIENCE] [--embedding-size EMBEDDING_SIZE]
					[--hidden-size HIDDEN_SIZE] [--l2 L2]
					data_file vocab_file output_file

	Train a language model on text file.

	positional arguments:
	  data_file             Text file for training. Each new line will be treated
							as a new sequence
	  vocab_file            Vocabulary file generated by vocab.py.
	  output_file           Output location to write data to.

	optional arguments:
	  -h, --help            show this help message and exit
	  --max-epochs MAX_EPOCHS
							Maximum number of epochs to run through training data.
							(default: 20)
	  --batch-size BATCH_SIZE
							Number of sequences to simultaneously calculate cost.
							(default: 32)
	  --validation-percent VALIDATION_PERCENT
							First validation_percent of data will be used as the
							validation set. (default: 0.01)
	  --checkpoint CHECKPOINT
							Saves to temporary_file every time this number of
							instances are seen. (default: 5000)
	  --improvement-threshold IMPROVEMENT_THRESHOLD
							Improvement over best cost has to be this much or
							incur patience. (default: 0.95)
	  --patience PATIENCE   Number of times improvement_threshold is allowed to be
							crossed since last best cost. (default: 10)
	  --embedding-size EMBEDDING_SIZE
							Size of per character embedding / character
							representation vector. (default: 100)
	  --hidden-size HIDDEN_SIZE
							Size of hidden LSTM layers. (default: 100)
	  --l2 L2               L2 coefficient. (default: 0.0)