# Pairwise Alignment methods
Work in progress.
Use <strong>own node</strong> with high gas limits for calls, or infinite gas limits for calls. 
Or public rpc node with such specification: <pre>https://rpcb.genesisL1.org</pre>
ABI for NeedlemanWunsch <pre>0xa747A43Be45105155F5a0fA2c3890FF17858Ac11</pre>
<pre>
[
    {
      "inputs": [
        {
          "internalType": "contract SubstitutionMatrices",
          "name": "_matricesAddress",
          "type": "address"
        }
      ],
      "stateMutability": "nonpayable",
      "type": "constructor"
    },
    {
      "inputs": [
        {
          "internalType": "string",
          "name": "sequenceA",
          "type": "string"
        },
        {
          "internalType": "string",
          "name": "sequenceB",
          "type": "string"
        },
        {
          "components": [
            {
              "internalType": "int256",
              "name": "gap",
              "type": "int256"
            },
            {
              "internalType": "uint256",
              "name": "limit",
              "type": "uint256"
            },
            {
              "internalType": "string",
              "name": "substitutionMatrix",
              "type": "string"
            }
          ],
          "internalType": "struct NeedlemanWunsch.AlignmentOptions",
          "name": "alignmentOptions",
          "type": "tuple"
        }
      ],
      "name": "_needlemanWunsch",
      "outputs": [
        {
          "components": [
            {
              "internalType": "string",
              "name": "sequenceA",
              "type": "string"
            },
            {
              "internalType": "string",
              "name": "sequenceB",
              "type": "string"
            },
            {
              "components": [
                {
                  "internalType": "string",
                  "name": "alignmentA",
                  "type": "string"
                },
                {
                  "internalType": "string",
                  "name": "alignmentB",
                  "type": "string"
                }
              ],
              "internalType": "struct NeedlemanWunsch.Alignment[]",
              "name": "alignments",
              "type": "tuple[]"
            },
            {
              "internalType": "int256",
              "name": "score",
              "type": "int256"
            },
            {
              "internalType": "uint256",
              "name": "count",
              "type": "uint256"
            }
          ],
          "internalType": "struct NeedlemanWunsch.AlignmentOutput",
          "name": "alignmentOutput",
          "type": "tuple"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_address",
          "type": "address"
        }
      ],
      "name": "addAdmin",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_newOwner",
          "type": "address"
        }
      ],
      "name": "changeOwner",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_address",
          "type": "address"
        }
      ],
      "name": "isAdmin",
      "outputs": [
        {
          "internalType": "bool",
          "name": "",
          "type": "bool"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_address",
          "type": "address"
        }
      ],
      "name": "isOwner",
      "outputs": [
        {
          "internalType": "bool",
          "name": "",
          "type": "bool"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "string",
          "name": "sequenceA",
          "type": "string"
        },
        {
          "internalType": "string",
          "name": "sequenceB",
          "type": "string"
        },
        {
          "internalType": "int256",
          "name": "gap",
          "type": "int256"
        },
        {
          "internalType": "string",
          "name": "substitutionMatrix",
          "type": "string"
        },
        {
          "internalType": "uint256",
          "name": "limit",
          "type": "uint256"
        }
      ],
      "name": "needlemanWunsch",
      "outputs": [
        {
          "components": [
            {
              "internalType": "string",
              "name": "sequenceA",
              "type": "string"
            },
            {
              "internalType": "string",
              "name": "sequenceB",
              "type": "string"
            },
            {
              "components": [
                {
                  "internalType": "string",
                  "name": "alignmentA",
                  "type": "string"
                },
                {
                  "internalType": "string",
                  "name": "alignmentB",
                  "type": "string"
                }
              ],
              "internalType": "struct NeedlemanWunsch.Alignment[]",
              "name": "alignments",
              "type": "tuple[]"
            },
            {
              "internalType": "int256",
              "name": "score",
              "type": "int256"
            },
            {
              "internalType": "uint256",
              "name": "count",
              "type": "uint256"
            }
          ],
          "internalType": "struct NeedlemanWunsch.AlignmentOutput",
          "name": "alignmentOutput",
          "type": "tuple"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_address",
          "type": "address"
        }
      ],
      "name": "removeAdmin",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "updateAlphabetIndices",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "limit",
          "type": "uint256"
        }
      ],
      "name": "updateDefaultLimit",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "contract SubstitutionMatrices",
          "name": "_address",
          "type": "address"
        }
      ],
      "name": "updateMatricesAddress",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    }
  ]
</pre>
