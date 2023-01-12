#prices of newspaper

news = {

    'TOI': [3, 3, 3, 3, 3, 5, 6],
    
    'Hindu': [2.5, 2.5, 2.5, 2.5, 2.5, 4, 4],
    
    'ET': [4, 4, 4, 4, 4, 4, 10],
    
    'BM': [1.5, 1.5, 1.5, 1.5, 1.5, 1.5, 1.5],
    
    'HT': [2, 2, 2, 2, 2, 4, 4],
    
}

#calculate total cost for the week

for key in news:

    news[key] = sum(news[key])

papers = list(news.keys())

amount = int(input())

n = len(news)

ans = []

#check all possible combinations

for i in range(n):

    for j in range(i+1, n):
    
        if news[papers[i]] + news[papers[j]] <= amount:
        
            ans.append({papers[i], papers[j]})
        
print(*ans)
    
