# code-alpha---project-name-task-2
Chatbot for FAQS
<br>
#include <iostream>
#include <map>
using namespace std;

int main() {
    map<string, string> faq;

    faq["what is ai"] = "AI stands for Artificial Intelligence.";
    faq["what is your name"] = "I am a chatbot.";
    faq["how are you"] = "I am fine!";
    faq["what is programming"] = "Programming is writing instructions for computers.";

    string question;

    cout << "FAQ Chatbot (type 'exit' to quit)\n";

    while (true) {
        cout << "\nYou: ";
        getline(cin, question);

        if (question == "exit") break;

        if (faq.find(question) != faq.end()) {
            cout << "Bot: " << faq[question] << endl;
        } else {
            cout << "Bot: Sorry, I don't understand.\n";
        }
    }

    return 0;
}
