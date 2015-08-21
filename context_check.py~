import pickle

word_pairs = []
word_pairs.append(['dubai','india'])
word_pairs.append(['namo','modi'])
word_pairs.append(['dubai','speech'])
word_pairs.append(['cricket','stadium'])
word_pairs.append(['nation','country'])
word_pairs.append(['india','pakistan'])
word_pairs.append(['mosque','temple'])
word_pairs.append(['prince','leader'])
word_pairs.append(['crowd','people'])
word_pairs.append(['minister','criket'])
word_pairs.append(['congress','love'])
word_pairs.append(['terrorism','love'])
word_pairs.append(['nation','land'])

def check():
	d = {}
	for pair in word_pairs:
		if not(d.has_key(pair[0])):
			d[pair[0]]=0
		if not(d.has_key(pair[1])):
			d[pair[1]]=0		
	tups = pickle.load(open("tups.pkl","rb"))
	vocab = pickle.load(open("vocab.pkl","rb"))
	for tup in tups:
		if tup[1] in d.keys():
			d[tup[1]]+=1
	scores = []
	for pair in word_pairs:
		delta = abs(d[pair[0]] - d[pair[1]])
		z = d[pair[0]] + d[pair[1]]
		pair.append(1-(float(delta)/z))
	print word_pairs
	pickle.dump(word_pairs,open("results1.pkl","wb"))
	
def new_check():
	tups = pickle.load(open("tups.pkl","rb"))
	vocab = pickle.load(open("vocab.pkl","rb"))
	dd = {}
	for pair in word_pairs:
		if not(dd.has_key(pair[0])):
			dd[pair[0]]=0
		if not(dd.has_key(pair[1])):
			dd[pair[1]]=0
	d = []
	for pair in word_pairs:
		temp = []
		c1=0
		c2=0
		for tup in tups:
			if(tup[1] == pair[0]):
				temp.append(tup[1])
				c1 +=1
		for v in temp:
			v[1] = pair[1]
			if v in tups:
				c2+=1
		delta = abs(c2-c1)
		d.append(delta)
	D = sum(d)
	for pair in word_pairs:
		
	
if __name__=="__main__":
	check()
