#!/usr/bin/python

# calc, a command-line calculator with arguments; version 1

# import libraries
import optparse


# function calc
def calc(num1, num2, op):
    # match the operator to the total
    if op == "+":
        total = num1 + num2
    elif op == "-":
        total = num1 - num2
    elif op == "x":
        total = num1 * num2
    elif (op == "%") or (op == "/"):
        total = num1 / num2
    # otherwise exit
    else:
        print "[!]Invalid operator, exiting. "
        exit(0)
    # print result
    print total


# function main
def main():
    # create parser
    parser = optparse.OptionParser("usage%prog -1 <number> -2 <number> -o <+, -, x, %(or /)>")
    
    # add options
    parser.add_option("-1", dest="number1", type="int",\
            help="specify first number")
    parser.add_option("-2", dest="number2", type="int",\
            help="specify second number")
    parser.add_option("-o", dest="operator", type="string",\
            help="specify operator of +, -, x, %(or /)")
    (options, args) = parser.parse_args()

    # if any of the options are empty, print usage and exit
    if ((options.number1 == None) or (options.number2 == None) or (options.operator == None)):
        print parser.usage
        exit(0)
    
    # if options.operator has none of the below, print usage and exit
    if (        (options.operator != "+") 
            and (options.operator != "-") 
            and (options.operator != "x") 
            and (options.operator != "%") 
            and (options.operator != "/")):
        print parser.usage
        exit(0)
    
    # create variables with value of options
    num1 = options.number1
    num2 = options.number2
    op   = options.operator

    # call calc function with variables
    calc(num1, num2, op)


# kick off main
if __name__ == "__main__":
    main()
