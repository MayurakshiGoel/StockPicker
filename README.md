# StockPicker
def stock_picker(picker)
	i=0
	max = 0
	buy = 0
	sell = 0
	while i < picker.size-1
		j=i
		for x in picker[i+1..-1] do 
			j=j+1
 			if x-picker[i] > max
 				max = x-picker[i]
 				buy = i
 				sell = j
 			end
		end
		i=i+1
	end
	p "buy: #{buy} sell: #{sell} profit: #{max}"
end
stock_picker([17,3,6,9,15,8,6,1,10])
stock_picker([4,6,9,34,28,12,2,16,8,44])
stock_picker([8, 5, 3, 6 ,8, 56, 43, 76, 54, 9])
stock_picker([6, 2, 7, 3, 1, 7, 3, 8, 4, 9])
