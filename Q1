import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

class Contact {
    private String contactName;
    private String contactPhoneNumber;
    private String contactEmailAddress;

    public Contact(String contactName, String contactPhoneNumber, String contactEmailAddress) {
        this.contactName = contactName;
        this.contactPhoneNumber = contactPhoneNumber;
        this.contactEmailAddress = contactEmailAddress;
    }

    public String getContactName() {
        return contactName;
    }

    public void setContactName(String contactName) {
        this.contactName = contactName;
    }

    public String getContactPhoneNumber() {
        return contactPhoneNumber;
    }

    public void setContactPhoneNumber(String contactPhoneNumber) {
        this.contactPhoneNumber = contactPhoneNumber;
    }

    public String getContactEmailAddress() {
        return contactEmailAddress;
    }

    public void setContactEmailAddress(String contactEmailAddress) {
        this.contactEmailAddress = contactEmailAddress;
    }

    @Override
    public String toString() {
        return "Name: " + contactName + ", Phone: " + contactPhoneNumber + ", Email: " + contactEmailAddress;
    }
}

class AddressBook {
    private List<Contact> contactList;

    public AddressBook() {
        this.contactList = new ArrayList<>();
    }

    public void addNewContact(Contact contact) {
        contactList.add(contact);
        System.out.println("Contact added successfully.");
    }

    public void displayAllContacts() {
        if (contactList.isEmpty()) {
            System.out.println("No contacts found.");
        } else {
            for (Contact contact : contactList) {
                System.out.println(contact);
            }
        }
    }

    public void findContactByName(String contactName) {
        boolean isFound = false;
        for (Contact contact : contactList) {
            if (contact.getContactName().equalsIgnoreCase(contactName)) {
                System.out.println(contact);
                isFound = true;
            }
        }
        if (!isFound) {
            System.out.println("No contact found with the name: " + contactName);
        }
    }
}

public class AddressBookApplication {
    public static void main(String[] args) {
        Scanner inputScanner = new Scanner(System.in);
        AddressBook addressBook = new AddressBook();
        int userChoice;

        do {
            System.out.println("\nMenu:");
            System.out.println("1. Add a new contact");
            System.out.println("2. View all contacts");
            System.out.println("3. Search for a contact by name");
            System.out.println("4. Exit the program");
            System.out.print("Enter your choice: ");
            userChoice = inputScanner.nextInt();
            inputScanner.nextLine(); // Consume newline

            switch (userChoice) {
                case 1:
                    System.out.print("Enter name: ");
                    String newName = inputScanner.nextLine();
                    System.out.print("Enter phone number: ");
                    String newPhoneNumber = inputScanner.nextLine();
                    System.out.print("Enter email address: ");
                    String newEmailAddress = inputScanner.nextLine();

                    Contact newContact = new Contact(newName, newPhoneNumber, newEmailAddress);
                    addressBook.addNewContact(newContact);
                    break;
                case 2:
                    System.out.println("All Contacts:");
                    addressBook.displayAllContacts();
                    break;
                case 3:
                    System.out.print("Enter name to search: ");
                    String searchName = inputScanner.nextLine();
                    addressBook.findContactByName(searchName);
                    break;
                case 4:
                    System.out.println("Exiting the program.");
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        } while (userChoice != 4);

        inputScanner.close();
    }
}
