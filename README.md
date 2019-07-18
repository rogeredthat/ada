# Estilo

Currently in development as a face recognition and clustering engine for linux desktops

### Proposed experience:

<HR SIZE=1></HR>

#### 1. Add folders to photo library

  * Clusters are created and added automatically in the background
  * Served as integration with third-party photo organization apps
  
#### 2. Open any photo-organization app and label, split or join clusters
  
  * Labels are dumped into database
  * Correction of false-positives and false-negatives leads to automatic splits and joins

<BR/>

### Proposed design:

<HR SIZE=1></HR>

#### 1. Face Encoding

  * Resize into usable resolution
  * [Dlib HOG detector for face detection](http://dlib.net/python/index.html#dlib.get_frontal_face_detector)
  * [Dlib Landmark detection](http://dlib.net/python/index.html#dlib.shape_predictor)
  * [Dlib face recognition](http://dlib.net/python/index.html#dlib.face_recognition_model_v1)

#### 2. Clustering 

  * [Sklearn's DBSCAN clustering implementation](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.DBSCAN.html)

#### 3. Cluster Maintenance

  * Extended file attributes (ext* as of now)
  * Database
  
#### 4. Expose training methods

  * CLI based
  * Library based

