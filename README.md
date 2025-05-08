# EX-NO-10-Diffie-Hellman-Key-Exchange-Algorithm

## AIM:
To Implement Diffie Hellman Key Exchange Algorithm 

## Algorithm:

1. Diffie-Hellman Key Exchange is used for securely sharing a secret key between two parties over an insecure channel.

2. Initialization: Agree on a large prime number \( p \) and a primitive root \( g \) modulo \( p \) (both are public values).

3. Key Exchange Process: 
   - Each party selects a private key and calculates their public key using the formula \( g^{\text{private key}} \mod p \).
   - Each party then shares their public key with the other.

4. Secret Key Computation: 
   - Each party computes the shared secret key using the received public key and their own private key.

5. Security: The difficulty of computing discrete logarithms ensures that the shared key remains secure even if public values are intercepted.

## Program:
### Name : PAVITHRAN S
### Reg no : 212223240113
```
def power(a, b, P):
    # Efficient modular exponentiation
    return pow(a, b, P)

def main():
    print("\n***** Diffie-Hellman Key Exchange Algorithm *****\n")

    # Input prime P and primitive root G
    P = int(input("Enter the value of P (a prime number): "))
    print(f"The value of P: {P}")

    G = int(input("Enter the value of G (a primitive root of P): "))
    print(f"The value of G: {G}\n")

    # Alice's private key
    a = 4
    print(f"The private key a for Alice: {a}")
    x = power(G, a, P)  # Alice's public key

    # Bob's private key
    b = 3
    print(f"The private key b for Bob: {b}\n")
    y = power(G, b, P)  # Bob's public key

    # Secret key computation
    ka = power(y, a, P)  # Secret key for Alice
    kb = power(x, b, P)  # Secret key for Bob

    print(f"Secret key for Alice: {ka}")
    print(f"Secret key for Bob: {kb}")

if __name__ == "__main__":
    main()
```



## Output:

![image](https://github.com/user-attachments/assets/21753579-c839-448c-a736-e420d241cf41)



## Result:
  The program is executed successfully

