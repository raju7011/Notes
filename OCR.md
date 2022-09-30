                                                                  ##PADDLE OCR##
                                                                                        
 ## USE PADDLE OCR
 
 1. create virtual enviroment in django

        pip install paddleocr
        
 2. create the one result.py 
      
        from paddleocr import PaddleOCR
        ocr = PaddleOCR(lang='en') # need to run only once to load model into memory
        img_path = 'PaddleOCR/doc/imgs_words_en/word_10.png'
        result = ocr.ocr(img_path, det=False, cls=False)
        for line in result:
            print(line)
