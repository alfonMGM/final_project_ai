import unittest
from EmotionDetection.emotion_detection import emotion_detector

class TestEmotionDetection(unittest.TestCase):
    def test_emotion_detector(self):
        # 1. Prueba para "joy" (alegría)
        result_1 = emotion_detector('I am glad this happened')
        self.assertEqual(result_1['dominant_emotion'], 'joy')

        # 2. Prueba para "anger" (ira)
        result_2 = emotion_detector('I am really angry about this')
        self.assertEqual(result_2['dominant_emotion'], 'anger')

        # 3. Prueba para "disgust" (desagrado)
        result_3 = emotion_detector('I feel disgusted just hearing about this')
        self.assertEqual(result_3['dominant_emotion'], 'disgust')

        # 4. Prueba para "sadness" (tristeza)
        result_4 = emotion_detector('I am so sad about this')
        self.assertEqual(result_4['dominant_emotion'], 'sadness')

        # 5. Prueba para "fear" (miedo)
        result_5 = emotion_detector('I am really afraid that this will happen')
        self.assertEqual(result_5['dominant_emotion'], 'fear')

if __name__ == '__main__':
    unittest.main()