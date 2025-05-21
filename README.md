# Ressources utiles
https://docs.ultralytics.com/fr/guides/yolo-performance-metrics/#class-wise-metrics
Précision : plus c'est élevé plus ça veut dire que quand on detecte alors on sait que c'est bon.  
Rappel : plus c'est élevé plus ça veut dire qu'on a trouvé tous les objets qu'on devait détecté. 
Augmentation de données :
https://docs.ultralytics.com/fr/guides/yolo-data-augmentation/

On baisse la luminosité pour simuler des images nocturnes
model.train(data="/content/Projet-parking/data/dataset.yaml", epochs=50, imgsz=640, batch=16, hsv_v = 0.5)
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100%|██████████| 1/1 [00:00<00:00,  7.01it/s]

                   all          6        558       0.76      0.825      0.833      0.389
           Place_Libre          6        374      0.663      0.898      0.863      0.422
         Place_Occupée          6        184      0.857      0.751      0.802      0.357


model.train(data="/content/Projet-parking/data/dataset.yaml", epochs=50, imgsz=640, batch=16, degrees = 90)

model.train(data="/content/Projet-parking/data/dataset.yaml", epochs=50, imgsz=640, batch=16, hsv_h=0.03,hsv_s = 0.6, hsv_v = 0.5, translate = 0.25, scale = 0.5, bgr = 1, erasing = 0.4)
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100%|██████████| 1/1 [00:00<00:00,  7.18it/s]

                   all          6        558      0.775       0.82      0.832      0.387
           Place_Libre          6        374      0.723      0.885      0.864      0.415
         Place_Occupée          6        184      0.828      0.755      0.799      0.359


