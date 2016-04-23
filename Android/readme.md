
#��׿�ͻ���
* ����

* ����

* �ܽ�

  * �ӿ�

    1. �ӿ�����

    * `[class]`CustomLineChart.java

      public �ӿ�����:

      * **������**

        ����˵����

        * `chartName` ,`String`����ͼ����
        * `lineName`,`String` ��������
        * `limitVal `,`float`������ֵ
        * `data` ,`int[]`����Դ����
        * `xAxislabel `,`ArrayList<String>`����������

        ```java
        CustomLineChart(String chartName,
                                   String limitName,
                                   String lineName,
                                   float limitVal,
                                   int[]data,
                                   ArrayList<String> xAxislabel);
        ```

      * **����ͼ���ɷ���**

        ����˵����

        * `chart`,`LineChart`����ͼ����

        ����ֵ˵����

        * void

        ```java
        void generateChart (LineChart chart);
        ```

      * ��������ͼ���Ʒ���

        ����˵����

        - `lineName`,`String`����ͼ����

        ����ֵ˵����

        - `void`

        ```java
        void setLineName(String lineName);
        ```

      * **��������ͼ���ݷ���**

        ����˵����

        - `data`,`int[]`����ͼ����

        ����ֵ˵����

        - `void`

        ```java
        void setData(int[] data);
        ```


      * **��������ͼ���������Ʒ���**

        ����˵����

        - `limitName`,`String`����������

        ����ֵ˵����

        - `void`

        ```java
        void setLimitName(String limitName);
        ```

      * **��������ͼ��������ֵ����**

        ����˵����

        - `limitVal`,`float`����ͼ����

        ����ֵ˵����

        - `void`

        ```java
        void setLimitVal(float limitVal);
        ```

      * **�������߽�ע**

        ����˵����

        - `lineName`,`String`����ͼ����

        ����ֵ˵����

        - `void`

        ```java
        void setLineName(String lineName);
        ```

      * **���ú���������**

        * ����˵����

          - `xAxislabel`,`ArrayList<String>`����ͼ����

          ����ֵ˵����

          - `void`

          ```java
          void setxAxislabel(ArrayList<String> xAxislabel);
          ```

    2.�ӿ�ʹ��Demo

    �6�7        

    * ```java
      public class FirstFrag extends Fragment {
          private int[] mDataYs = new int[]{21, 23, 25, 30, 29, 26, 25, 27, 24, 22, 21, 22, 23, 20};
          @Nullable
          @Override
          public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
              View view = inflater.inflate(R.layout.fragment_chart_fragmemt, container, false);
              LineChart chart = (LineChart)view.findViewById(R.id.chart);
              CustomLineChart customLineChart = new CustomLineChart();
              customLineChart.setChartName("Temprature");
              customLineChart.setData(mDataYs);
              customLineChart.setLimitName("Great");
              customLineChart.setLimitVal(25f);
              customLineChart.setLineName("line");
              customLineChart.setxAxislabel(getXAxisShowLable());
              customLineChart.generateChart(chart);

              return view;
          }


          private ArrayList<String> getXAxisShowLable() {
              ArrayList<String> m = new ArrayList<String>();
              m.add("00:00");
              m.add("02:00");
              m.add("04:00");
              m.add("06:00");
              m.add("08:00");
              m.add("10:00");
              m.add("12:00");
              m.add("14:00");
              m.add("16:00");
              m.add("18:00");
              m.add("20:00");
              m.add("22:00");
              m.add("55");
              m.add("66");

              return m;
          }

      ```

