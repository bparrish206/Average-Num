Average-Num
===========
# main function asks user for a number then calculates the average of all the numbers given.
def main():
   #set counter for total values enters
   total = 0
   #set counter for number of entries
   count = 0
   #ask user for a number
   value = input('Enter a number (\'end\' to exit): ')
   #create a loop to go over value
   while(value != 'end'):
       #test value to see if its a int if it is add it to total variable and add one to count
      if value.isdigit():
         total += int(value)
         count += 1
      #include negative numbers
      elif value[1:].isdigit():
         total += int(value)
         count += 1
      #if not print error message
      else:
         print('Non-numeric input ignored.')
      #ask user again for input
      value = input('Enter a number (\'end\' to exit): ')
      #let the user know how many values they've entered
      print('You entered', count, 'values')
    # if average is not divisable print error message
   if count == 0:
      print('The average cannot be calculated.')
    #let the user know what the average is of thier entries
   else:
      print('The average value is', total/count)

main()
