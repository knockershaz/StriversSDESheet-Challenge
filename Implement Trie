class TrieNode {
public:
    char data;
    TrieNode* childNode[26];
    bool isTerminal;

    TrieNode(char val)
    {
        this->data = val;
        this->isTerminal = false;
        for (int i = 0; i < 26; i++)
        {
            childNode[i] = NULL;
        }
    }
};

class Trie {
    TrieNode* root;

public:
    Trie() {
        root = new TrieNode('\0');
    }

    void insert_key(TrieNode* root, string key) {
        TrieNode* currentNode = root;
        int length = key.size();
        for (int i = 0; i < length; i++)
        {
            if (currentNode->childNode[key[i] - 'a'] == NULL)
            {
                TrieNode* newNode = new TrieNode(key[i]);
                currentNode->childNode[key[i] - 'a'] = newNode;
            }
            currentNode = currentNode->childNode[key[i] - 'a'];
        }
        currentNode->isTerminal = true; // Mark the last node as terminal
    }

    void insert(string word) {
        insert_key(root, word);
    }

    bool search_key(TrieNode* root, string& queryString) {
        TrieNode* currentNode = root;
        int length = queryString.size();
        for (int i = 0; i < length; i++)
        {
            if (currentNode->childNode[queryString[i] - 'a'] == NULL)
            {
                return false;
            }
            currentNode = currentNode->childNode[queryString[i] - 'a'];
        }
        return currentNode != NULL && currentNode->isTerminal == true;
    }

    bool search(string word) {
        return search_key(root, word);
    }

    bool startsWithCheck(TrieNode* root, string prefix) {
        TrieNode* currentNode = root;
        for (int i = 0; i < prefix.size(); i++)
        {
            if (currentNode->childNode[prefix[i] - 'a'] == NULL)
            {
                return false;
            }
            currentNode = currentNode->childNode[prefix[i] - 'a'];
        }
        return currentNode != NULL ||currentNode->isTerminal == true;
    }

    bool startsWith(string prefix) {
        return startsWithCheck(root, prefix);
    }
};
