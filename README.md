# Binary-Search-Using-Swift
A binary search function using Swift 


# code starts here

//: Playground - noun: a place where people can play
//created by tianhaulee 23/2/2018

import UIKit

//let numbers = [1, 2, 4, 6, 8, 9, 11, 13, 16, 17, 28]

var hundred = [Int]()
for i in 1...100 {
    hundred.append(i) //append 1-100
}
func binarySearchForSearchValue(searchValue: Int, array:[Int]) -> Bool {
    
    var leftIndex = 0
    var rightIndex = array.count - 1
    
    while leftIndex <= rightIndex {
        
        let middleIndex = (leftIndex + rightIndex) / 2
        let middleValue = array[middleIndex]
        print("middleValue: \(middleValue), leftIndex: \(leftIndex), rightIndex: \(rightIndex), [\(array[leftIndex]), \(array[rightIndex])]" )
        if middleValue == searchValue {
            return true
        }
        if searchValue < middleValue {
            rightIndex = middleIndex - 1
        }
        if searchValue > middleValue {
            leftIndex = middleIndex + 1
        }
    }
    return false
}
print(binarySearchForSearchValue(searchValue: 53, array: hundred))


//func linearSearchforSearchValue(searchValue: Int, array: [Int]) -> Bool {
//    for num in array {
//        if num == searchValue {
//            return true
//        }
//    }
//    return false
//}
//print(linearSearchforSearchValue(searchValue: 2, array: numbers))

