public class WordEncryption {

    public static String encryptString(String inputText, int shiftAmount) {
        StringBuilder encryptedText = new StringBuilder();

        for (char currentChar : inputText.toCharArray()) {
            if (Character.isLetter(currentChar)) {
                int baseValue = Character.isLowerCase(currentChar) ? currentChar - 'a' : currentChar - 'A';
                int shiftedValue = (baseValue + shiftAmount) % 26;
                char shiftedChar = (char) ((Character.isLowerCase(currentChar) ? 'a' : 'A') + shiftedValue);
                
                // Inverting the case
                if (Character.isLowerCase(currentChar)) {
                    shiftedChar = Character.toUpperCase(shiftedChar);
                } else {
                    shiftedChar = Character.toLowerCase(shiftedChar);
                }

                encryptedText.append(shiftedChar);
            } else {
                encryptedText.append(currentChar);
            }
        }

        return encryptedText.toString();
    }

    public static void main(String[] args) {
        String inputText = "Wipro Tech";
        int shiftAmount = 20;
        String encryptedResult = encryptString(inputText, shiftAmount);
        System.out.println("Encrypted words: " + encryptedResult);
    }
}
