# [1] FINANCE

(A) According to the bitcoin white paper published by Satoshi Nakamoto(2008), Bitcoin is the first scarce digital object the world has ever seen. Its scarcity can be compared to precious metals like silver & gold, and can be sent over the internet, radio, satellite. It's almost safe to say every scarcity has value. But how much? That's where stock-to-flow valuation model became an important interest.

STOCK-TO-FLOW (SF) MODEL:

The Stock to Flow model measures the relationship between the currently available stock of a resource and its production rate. It’s typically applied to precious metals and other commodities, but over the years advocates of SF have argue this same logic applies to bitcoin. 

BLOCKCHAIN STOCK-TO-FLOW (SF) MODEL:

Bitcoin Stock-to-Flow (SF) Model is a metric used to quantify the abundance of bitcoin, that is, the ratio between current supply(amount of bitcoin held in reserve) and new supply(amount of Bitcoin produced annually). 

Gold is often regarded as store of value resource because it tends to retain its value over the long term due to its relative scarcity and low flow, also it’s very difficult to significantly increase its supply within a short period of time. Bitcoin features like its scarcity, relatively high cost of production,  its maximum supply capped at 21 million coins, and Bitcoin’s supply issuance which is defined on the protocol level which makes its flow(annual production) completely predictable as led to the conclusion that SF model can be considered in actualizing Bitcoin scarcity valuation. Also roughly every four years, Bitcoin halvings is implemented where the amount of new supply entering the system is halved at every 210,000 blocks. 

With minimal flow introduced and higher SF, it was concluded that scarcity is a driven factor in determining the value of priced resources.
     SF = Stock / Flow
     Where Stock = size of the existing stockpiles or reserves, 
     Flow = annual production rate.

ARGUMENT FOR WHY STOCK-TO-FLOW IS A BAD MODEL:

The SF hypothesis, “…that scarcity, as measured by SF, directly drives value” cannot be relied on according to critics of Stock to Flow, this model fails if Bitcoin doesn’t have any other useful qualities other than supply scarcity. For example, gold’s scarcity, its predictable flow, and global liquidity have made it a relatively stable store of value compared to Bitcoin's value which has been historically characterized as being quite volatile. 

And since the Bitcoin Stock-to-Flow model tries to predict the value of Bitcoin based on historical data, historical data can’t account for unknown events. The unknown events that triggers Bitcoin volatility feature which hurts its adoption rate includes (I) Bad News: news events that scare bitcoin users include, geopolitical events and statements by governments that Bitcoin is likely to be regulated., (II) Uncertainty of Future Bitcoin's Value: varying perceptions of the intrinsic value of the cryptocurrency as a store of value(store of value is the function by which an asset can be useful in the future with some predictability) and method of value transfer., (III) Security Breaches., to mention a few.

(B) From the question,
Stock Price (Po) = $40
Strike Price (X) = $45
Maturity time (t) = 4months = 4/12 = 0.333yr
Volatility (Standard deviation Ó) = 40% = 0.4
Risk Free (Krf) = 3% = 0.03

Black-Schole call price is given as;

VC = Po * N(d1) -  X/e^Krft * N(d2)

Where d1 = [ln (Po/X) + (Krf + 0.5*Ó^2) t] / Ó√t

d2 = d1 - Ó√t

We first need to find d1 and d2:
Finding the value of d1;

d1 =  [ln (40/45) + (0.03 + 0.5*0.4^2) 0.333] / 0.4√0.333

d1 =  [ -0.117783 + (0.03+ 0.08) 0.333] / 0.44 * 0.57735

d1 = -0.081153/0.23094
d1 = -0.35140

Finding the value of d2;

d2 = d1 - Ó√t

d2 = -0.35140 - (0.4√0.333)
d2 = -0.35140 - 0.23094
d2 = -0.58234

Therefore d1 = -0.35140,  d2 = -0.58234

Checking these value under Standard Normal Distribution Table;

N(d1) = 0.3632,  N(d2) = 0.2810

Once we have N(d1) and N(d2), we can plug-in the relevant numbers in the Black-Scholes formula

Finding the Black-Scholes call price;

VC = Po * N(d1) -  X/e^Krft * N(d2)

VC = 40(0.3632) -  45/(e^0.03*0.333) * (0.2810)

VC = 14.528 -  45/1.0100 * (0.2810)

VC = 14.528 - 12.5193053

VC = 2.0086747

Black-Scholes call price is $2



# [2] COMPUTER SCIENCE

(A) The Recursion, Instead of executing a specific process within the function, the function calls itself repeatedly until a certain condition is met (this condition being the base case). Because the function has to add to the stack with each recursive call and keep the values there until the call is finished, hence it requires a higher memory allocation. Also its requirement of a new stack frame allocation with each call increases its tendency of it being slow.

(B) A Proth number is a positive integer of the form n = k * 2n + 1. Where k is an odd positive integer and n is a positive integer such that 2n > k .

Steps;

Step 1: Deduct 1 from the number. This would give a number in the form k*2n, if the given number is a proth number.

Step 2: Now, loop through all odd number starting form k=1 to n/k and check if k can divide n in such a way that ( n/k ) is a power of 2 or not.

Step 3: If found, print ‘NUMBER IS PROTH’

Step 4: If no such value of k is found then Print ‘NUMBER IS NOT PROTH’

// C++ program to check Proth number 
#include <iostream> 
using namespace std; 
  
// method to check power of two 

bool isPowerOfTwo(int n) 

{ 
    
    return (n && !(n & (n - 1))); 
} 

  
// Function to check if the 
// Given number is Proth number or not 

bool isProthNumber(int n) 
{ 

    int k = 1; 

    while (k < (n / k)) { 

        // check if k divides n or not 

        if (n % k == 0) { 

            // Check if n/k is power of 2 or not 

            if (isPowerOfTwo(n / k)) 

                return true; 

        } 

        // update k to next odd number 

        k = k + 2; 
    } 

    // IF there exists no value of K 

    // Such that k is odd number 

    // and n/k is a power of 2 greater than k 

    return false; 
}
  
// Main code 
int main() 
{ 

    // Get n 
    int n = 25; 

  
    // Check n for Proth Number 
    if (isProthNumber(n - 1)) 

        cout << "NUMBER IS PROTH"; 

    else

        cout << "NUMBER IS NOT PROTH"; 


    return 0; 
} 


# [3] MATHEMATICS
