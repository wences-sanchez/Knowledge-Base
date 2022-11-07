# Quantum Computing for Everyone

deck:: [[Science::Quantum Computing for Everyone]]\
author:: [[Chris Bernhardt]]\
full-title:: "Quantum Computing for Everyone"\
category:: #books\
\
tags:: Science  

![](https://images-na.ssl-images-amazon.com/images/I/41yGAGsO8TL._SL200_.jpg)
## Highlights
- id:: 6363992e-a138-4636-82bb-d22efbd6e610
   The Quantum Clock #flashcard 
    Imagine that you have a clock with a dial marked with hours in the standard positions. It also has a hand. You are, however, forbidden to look at the face of the clock. You can only ask it questions. You want to know in which direction the hand is pointing, so you would like to ask the clock this seemingly simple question. But it is not allowed. You are only allowed to ask whether the hand is pointing at a particular number on the face. So, for example, you can ask if the hand is pointing to twelve, or you can ask if it is pointing to four. Now, if this were a regular clock you would have to be extremely lucky to get a yes answer. Most of the time the hand would be pointing in a completely different direction. But the quantum clock is not like a regular clock. It either answers yes or it tells you that the hand is pointing in the direction exactly opposite the one you asked about. If we ask if the hand is pointing in the direction of twelve, it will tell us either that it is or that it is pointing in the direction of six. If we ask if the hand is pointing in the direction of four, it will either tell us it is, or that it is pointing in the direction of ten. This is a very curious state of affairs, but it is exactly analogous to electron spin.
  
     (Page 6)
-
- id:: 6363992e-5eff-406a-99fc-29e90b56d5e0
   The first measure is whatever. But the second has to be random when we compare it with the first (exactly 1/2).
   But if we measure once, the result is definite. #flashcard 
    The analogous questions for our clock are asking about whether the hand is pointing in the direction of twelve and then asking if it is pointing in the direction of three. If we have a large number of clocks and ask them these two questions, the answers to the second questions will be random.
     Half of the clocks will say the hand is pointing in the direction of three. The other half will say in the direction of nine. The answers to the first question have no bearing on the answers to the second question.
  
     (Page 8)
-
- id:: 6363992e-c10d-4144-a04f-4cd9eb497e5d
  
  What conclusions can we draw from these results? There are three. And they are all important.
     First, if we keep repeating exactly the same question we get exactly the same answer. This tells us that sometimes there are definite answers. We are not getting random answers to every question.
     Second, randomness does seem to occur. If we ask a sequence of questions, the final results can be random.
     Third, measurements affect outcomes. We saw that if we ask the same question three times, we get the exactly the same answer three times. But if the first and third questions are identical and the second is different, the answers to the first and third questions need not be the same. For example, if we ask three times in a row if the hand is pointing toward twelve, we will get exactly the same answer each time, but if we ask first if it is pointing toward twelve, then whether it is pointing to three, and finally again whether it is pointing toward twelve, the answers to the first and third question need not be the same. The only difference between the two scenarios is the second question, so that question must be affecting the outcome of the following question. #flashcard 
  
  
     (Page 8)
-
- id:: 6363992e-abff-405c-acb3-b7f9d1c09027
  
  Each time a measurement is made, we will see that the system is changed in certain prescribed ways; these prescribed ways depend on the type of measurement being made but not on the strength of the measurement.
     Incorporating measurements into the theory is one on the differences between classical and quantum mechanics. #flashcard 
  
  
     (Page 10)
-
- id:: 6363992e-076e-438e-8c1b-a9fd5ada9fcf
  
  These three things-superposition, measurement, and entanglement are the key quantum mechanical ideas. Once we know what they mean, we can see how they may be used in computations. It is here that human ingenuity enters the picture. #flashcard  #quantum 
  
  
     (Page 11)
-
- id:: 6363992e-ac84-4641-bc45-5c278afe6b47
  
  The basic unit of quantum computing is the qubit. We will see what qubits are and what happens when we measure them. A classical bit is either 0 or 1. If it's 0 and we measure it, we get 0. If it's 1 and we measure 1, we get 1. 
     In both cases the bit remains unchanged. The situation is totally different for qubits. A qubit can be in one of an infinite number of states-a superposition of both 0 and 1-but when we measure it, as in the classical case, we just get one of two values, either 0 or 1. The act of measurement changes the qubit. A simple mathematical model describes all of this precisely. #flashcard 
  
  
     (Page 14)
-
- id:: 6363992e-5904-43b2-b270-79ded7bcc06d
   How Quantum and traditional computing are related #flashcard 
    You will also come to realize that quantum computing and classical computing are not two distinct disciplines, but that quantum computing is the more fundamental form of computing anything that can be computed classically can be computed on a quantum computer. 
     The qubit is the basic unit of computation, not the bit. Computation, in its essence, really means quantum computation.
  
     (Page 14)
-
- id:: 6363992e-7823-47f6-a1fa-8e70451ee50c
   Qubits are random but unique. #flashcard 
    To measure spin, you first have to choose a direction and then measure it in that direction. Spin is quantized: When measured, it gives just two possible answers-not a continuous range of answers. We can assign classical bits to these results. For example, if we obtain an N we can consider it to be the binary digit 0, and if we obtain an S we can consider it to be the binary digit 1. This is exactly how we get answers from a quantum computation.
     The last stage of the computation is to take a measurement. The result will be one of two things, which will be interpreted as either 0 or 1. Although the actual computation will involve qubits, the final answer will be in terms of classical bits.
  
     (Page 15)
-
- id:: 6363992e-910b-4add-9c75-0a60fe73e6cd
   About being sure of (specific) Quantum measurements #flashcard 
    If we measure the spin first in the vertical direction and then once more in the same direction, we obtain exactly the same result for both measurements. If the first measurement shows that the electron has its north pole upward, then so will the second measurement.
  
     (Page 37)
-
- id:: 6363992e-c8bf-45a7-80f5-3e0d206abba0
   What is a qubit? #flashcard 
    We define a qubit to be any unit ket in R. Usually, given a qubit, we will want to measure it. If we are going to measure it, we also need to include direction of measurement. This is done by introducing an ordered ortho normal basis (|bo),|bi)). The qubit can be written as a linear combination often called a linear superposition-of the basis vectors. In general, it will have the form d0|b0)+d1|b1). After we measure, its state will jump to either |b0) or |b1). The probability of its being |b0) is d0^2; the probability of |b1) is d1^2. This is exactly the same model we have been using, but now we connect the classical bits 0 and 1 to the basis vectors. We will associate the |b0) basis vector with the bit 0 and the |b1) basis vector with the bit 1. So when we measure the qubit d0|b0)+ d1|b1) we will obtain 0 with probability d and 1 with probability d .
     Since a qubit can be any unit ket and there are infinitely many unit kets, there are infinitely many possible values for a qubit. This is quite unlike classical computation, where we just have two bits. It is important, however, to notice that to get information out of a qubit we have to measure it.
     When we measure it we will get either 0 or 1, so the result is a classical bit.
  
     (Page 50)
-
- id:: 6363992e-708c-48e9-9f2c-c8bbe84ed8a1
   Quantum Computing for everyone #flashcard 
    A qubit can be in one of an infinite number of states-a superposition of both 0 and 1-but when we measure it, as in the classical case, we just get one of two values, either 0 or 1.
     The act of measurement changes the qubit. A simple mathematical model describes all of this precisely.
     Qubits can also be entangled. When we make a measurement of one of them, it affects the state of the other. Again, this is something that we don't experience in our daily lives, but it is described perfectly by our mathematical model.
     These three things-superposition, measurement, and entanglementare the key quantum mechanical ideas.
-
- id:: 6363992e-8089-4c54-9729-ba2efc07cb35
  
  Superposición, medida y entrelazado cuántico.
     Son los tres conceptos principales de la computación cuántica.
     1. Puede estar el qubit en un número infinito de estados desde 0 hasta 1
     2. Si medimos un qubit, al hacerlo lo cambiamos 
     3. Cuando medimos un qubit, también afectamos al otro. #flashcard  #note
-
- id:: 6363992e-e09f-4d48-8165-4b7541d7b486
  
  You will also come to realize that quantum computing and classical computing are not two distinct disciplines, but that quantum computing is the more fundamental form of computing. Anything that can be computed classically can be computed on a quantum computer. #flashcard
-
- id:: 6363992e-4182-4fe9-acf9-651b71dd06a1
  
  Quantum computing is based on an area of mathematics called linear algebra. Fortunately, we only need a few concepts. #flashcard
-
- id:: 6363992e-8bab-4b9c-8e97-0167aaebdcd5
  
  A classical bit is either 0 or 1. If it's 0 and we measure it, we get 0. If it's 1 and we measure 1, we get 1. In both cases the bit remains unchanged. The situation is totally different for qubits. A qubit can be in one of an infinite number of states-a superposition of both 0 and 1-but when we measure it, as in the classical case, we just get one of two values, either 0 or 1. The act of measurement changes the qubit. A simple mathematical model describes all of this precisely.
     Qubits can also be entangled. When we make a measurement of one of them, it affects the state of the other. Again, this is something that we don't experience in our daily lives, but it is described perfectly by our mathematical model.
     These three things-superposition, measurement, and entanglementare the key quantum mechanical ideas. Once we know what they mean, we can see how they may be used in computations. It is here that human ingenuity enters the picture. #flashcard
-