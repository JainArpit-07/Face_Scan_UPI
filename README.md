# Face_scan_UPI

make sure you have following python libraries downloaded
pip intall opencv-python
pip install face_recognition
pip install Pillow


Follow the following directory layout:

--- face_recognizer
            ----- output
            ----- training
                      ---- (folder with name - upi_address_person1)
                                                        ----- img_1.jpg (pictures of person1 correspnding to upi address)
                                                        ----- img_2.jpg (pictures of person1 correspnding to upi address)
                                                        |
                                                        |
                                                        ----- img_n.jpg (more pictures will result in better accuracy)
                      ---- (folder wtih name - upi_address_person2)
                                                        ----- img_1.jpg (pictures of person2 correspnding to upi address)
                                                        ----- img_2.jpg (pictures of person2 correspnding to upi address)
                                                        |
                                                        |
                                                        ----- img_n.jpg (more pictures will result in better accuracy)
            ----- validation (to check your model)
                      ---- person1.jpg
                      ---- person2.jpg
            ----- detector.py
            ----- unknown.jpg (image to check - not mandatory as the model takes input from webcam also)


Points to remember
python detector.py --help                  #to check all methods
python detector.py --train                 #to train your model
python detector.py --validate              #to validate your model
python detector.py --test                  #to take input from webcam
python detector.py --test -f file_path     #to check unknown already existing image
