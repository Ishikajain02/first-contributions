# गिट से एक फाइल को हटाना
कभी-कभी, आप किसी फ़ाइल को Git से हटाना चाहते हैं, लेकिन उसे अपने कंप्यूटर से हटाना नहीं चाहते हैं। आप निम्न आदेश का उपयोग करके इसे प्राप्त कर सकते हैं:

``git rm <file> --cached``

## तो क्या हुआ?
Git अब हटाए गए फ़ाइल में परिवर्तनों का ट्रैक नहीं रखेगा। जहां तक Git को पता है, ऐसा लगता है कि आपने फाइल को डिलीट कर दिया है। यदि आप अपने फाइल सिस्टम में फाइल का पता लगाने वाले थे, तो आप देखेंगे कि यह अभी भी वहीं है।

ध्यान दें कि ऊपर के उदाहरण में, ``--cached`` फ्लैग का प्रयोग किया गया है। यदि हमने इस ध्वज को नहीं जोड़ा है, तो Git न केवल रेपो से, बल्कि आपके फ़ाइल सिस्टम से भी फ़ाइल को हटा देगा।

यदि आप git commit ``-m "Remove file1.js"`` के साथ परिवर्तन करते हैं और इसे ``git push origin master`` का उपयोग करके दूरस्थ रिपॉजिटरी में धकेलते हैं, तो दूरस्थ रिपॉजिटरी फ़ाइल को हटा देगी।

## अतिरिक्त सुविधाये
- यदि आप एक से अधिक फ़ाइलों को हटाना चाहते हैं, तो आप उन सभी को एक ही कमांड में शामिल कर सकते हैं:

``git rm file1.js file2.js file3.js --cached``

- आप समान फ़ाइलों को निकालने के लिए वाइल्डकार्ड (*) का उपयोग कर सकते हैं। उदाहरण के लिए, यदि आप अपने स्थानीय भंडार से सभी .txt फ़ाइलों को हटाना चाहते हैं:

``git rm *.txt --cached``