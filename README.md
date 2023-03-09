# csc249_

#Module three

#CSC 249 Data Structures
#M3T1_PYT
#Jonathan Purchase
#3/8/2023


DEBUG = False #True 

def selection_sort(numbers):
   # A variable to hold the number of item comparisons
   comparisons = 0

   for i in range(len(numbers)-1):
     
      # Find index of smallest remaining element
      index_smallest = i
      for j in range(i+1, len(numbers)):
        
        
        if numbers[j] < numbers[index_smallest]:  
       
         index_smallest = j
        if DEBUG:
            print ("\t", "smallest:", numbers[j], "0", j) 
         
        
         #comparisons = comparisons + 1
        

      
      # Swap numbers[i] and numbers[index_smallest]
      temp = numbers[i]
      if DEBUG: 
        print("\t\t", "swapping", numbers[i], "and", numbers[index_smallest])
      numbers[i] = numbers[index_smallest]
      numbers[index_smallest] = temp
      if DEBUG:
        print("PART_SORTED:", numbers)    
   #return comparisons


# Main program to test the selection sort algorithm
numbers = [10, 2, 78, 4, 45, 32, 7, 11]

# Display the contents of the list

print('UNSORTED:', numbers)

# Call the selection_sort() function
comparisons = selection_sort(numbers)

# Display the (sorted) contents of the list
print('SORTED:', numbers)

#print('Total comparisons: %d' % comparisons)
