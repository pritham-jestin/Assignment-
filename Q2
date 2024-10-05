public class ContainerWithMostWater {
    public static int findMaxWaterArea(int[] heights) {
        int maximumArea = 0;
        int start = 0;
        int end = heights.length - 1; 
        while (start < end) {
            int area = Math.min(heights[start], heights[end]) * (end - start);
            maximumArea = Math.max(maximumArea, area);
            if (heights[start] < heights[end]) {
                start++;
            } else {
                end--;
            }
        }
        return maximumArea;
    }

    public static void main(String[] args) {
        int[] heights1 = {1, 8, 6, 2, 5, 4, 8, 3, 7};
        System.out.println("Maximum water area: " + findMaxWaterArea(heights1));
        int[] heights2 = {1, 1};
        System.out.println("Maximum water area: " + findMaxWaterArea(heights2));
    }
}
