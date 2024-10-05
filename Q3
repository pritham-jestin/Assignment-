import java.util.ArrayList;
import java.util.List;

public class TextJustification {
    public static List<String> fullJustify(String[] words, int maxWidth) {
        List<String> justifiedLines = new ArrayList<>();
        int wordCount = words.length;
        int currentIndex = 0;
        
        while (currentIndex < wordCount) {
            int currentLineLength = words[currentIndex].length();
            int nextIndex = currentIndex + 1;
            
            while (nextIndex < wordCount) {
                if (currentLineLength + 1 + words[nextIndex].length() > maxWidth) break;
                currentLineLength += 1 + words[nextIndex].length();
                nextIndex++;
            }
            
            StringBuilder lineBuilder = new StringBuilder();
            int gapsBetweenWords = nextIndex - currentIndex - 1;
            
            // If it's the last line or only one word in the line
            if (nextIndex == wordCount || gapsBetweenWords == 0) {
                for (int i = currentIndex; i < nextIndex; i++) {
                    lineBuilder.append(words[i]);
                    if (i != nextIndex - 1) lineBuilder.append(" ");
                }
                while (lineBuilder.length() < maxWidth) {
                    lineBuilder.append(" ");
                }
            } else {
                int spacesPerGap = (maxWidth - currentLineLength) / gapsBetweenWords;
                int extraSpaces = (maxWidth - currentLineLength) % gapsBetweenWords;
                
                for (int i = currentIndex; i < nextIndex - 1; i++) {
                    lineBuilder.append(words[i]);
                    lineBuilder.append(" ");
                    for (int j = 0; j < spacesPerGap; j++) {
                        lineBuilder.append(" ");
                    }
                    if (extraSpaces > 0) {
                        lineBuilder.append(" ");
                        extraSpaces--;
                    }
                }
                lineBuilder.append(words[nextIndex - 1]); // Last word in the line
            }
            
            justifiedLines.add(lineBuilder.toString());
            currentIndex = nextIndex;
        }
        
        return justifiedLines;
    }
    
    public static void main(String[] args) {
        String[] words = {"This", "is", "an", "example", "of", "text", "justification."};
        int maxWidth = 16;
        List<String> justifiedText = fullJustify(words, maxWidth);
        
        for (String line : justifiedText) {
            System.out.println("\"" + line + "\"");
        }
    }
}
