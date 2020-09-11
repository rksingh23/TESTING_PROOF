# TESTING_PROOF *TESTING BY CONTRADICTION
Explain: In very simple steps and a basic example expalin how to perform Testing of your design using Testing by Induction and Testing by Contradiction.....


# TESTING_PROOF_1 *TESTING BY CONTRADICTION
Use proof by contradiction to prove that the FindMax function always finds the maximum value in the input vector.

int FindMax(std::vector<int> &inputs) {
   if (inputs.size() == 0) {
       return -1;
   }
   int result = INT32_MIN;
   for (auto n : inputs) {
       if (n > result) {
           result = n;
       }
   }
   return result;
}
  
Answer: The proposition to be proved is that "the FindMax function always finds the maximum value in the input vector." So                                                        
Step 1. Let's assume this to be false. i.e "the FindMax function NEVER finds the maximum value in the input vector."                                                            
Step 2. Begining the proof, Let's pass a vector as an argument to the function.                                                                                         
Step 3. Upon testing it is observed that --> If the vector is empty, the returned valus is -1, whereas if the vector is not empty, then every single element of the vector is ittreated in the loop, and the max value is returned as the result.                                                                                                       
Step 4. Hence we conclude that the CONTRADICTION/NEGATION of our assumption is true.                                                                                   
Step 5. Concluding, we have proved that "the FindMax function always finds the maximum value in the input vector by method of contradiction."                                                        


# TESTING_PROOF_2 *TESTING BY INDUCTION

Use proof by induction to prove that the FindMax function always finds the maximum value in the input vector.

int FindMax(std::vector<int> &inputs) {
   if (inputs.size() == 0) {
       return -1;
   }
   int result = INT32_MIN;
   for (auto n : inputs) {
       if (n > result) {
           result = n;
       }
   }
   return result;
}
  
Answer: The proposition to be proved is that "the FindMax function always finds the maximum value in the input vector." So                                                        
Step 1. Let's assume this to be true. i.e "the FindMax function always finds the maximum value in the input vector."                                                            
Step 2. Begining the proof, Let's not pass a set of values in a vector as an argument to the function, But let's pass one value via vector.                                     
Step 3. We begin our testing by proving that that one value, which is greater that the min integer value is being returnd from the function.                                    
Step 4. Additionally, we pass a an empty vector, and test that the returned valus is -1.                                                                                         
Step 4. Hence we conclude that by the method of induction, we are now safe to say that our assumption is true.                                                                   
Step 5. Concluding, we have proved that "the FindMax function always finds the maximum value in the input vector by method of induction."                                                        
