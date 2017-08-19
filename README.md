# Exercism

def hello_world():
	print('Hello, world!')

def leap_year(x):
	try:
		x = int(x)
	except:
		print("Put numbers.")
	if x % 4 == 0:
		if x % 100 == 0:
			if x % 400 == 0:
				return True
			else:
				return False
		else:
			return True
	else:
		return False

def isogram(x):
	lst = []
	indicate = False
	for i in x:
		if i not in x:
			lst.append(i)
		else:
			indicate = True
	if not indicate:
		print('%s is an isogram.' % (x))
	else:
		print('%s is not an isogram' % (x))

def pangram(x):
	lst = []
	lst2 = []
	alph = 'abcdefghijklmnopqrstuvwxyz'
	for i in alph:
		if i not in lst2:
			lst2.append(i.lower())
	for i in x:
		if i not in lst:
			if i in alph:
				lst.append(i.lower())
	if len(lst2) == len(lst):
		print('It is a pangram.')
	else:
		print('It is not a pangram.')

def rna_trans(x):
	new = ''
	for i in x:
		if i == 'G':
			new += 'C'
		elif i == 'C:
			new += 'G'
		elif i == 'A':
			new += 'U'
		elif i == 'T':
			new += 'A'
	print('%s\n%s' % (x,new))







