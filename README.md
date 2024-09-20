<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Custom Marker-based AR.js</title>
  <!-- A-Frame 라이브러리 -->
  <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
  <!-- AR.js 라이브러리 -->
  <script src="https://raw.githack.com/jeromeetienne/AR.js/1.7.7/aframe/build/aframe-ar.js"></script>
</head>
<body style="margin: 0; overflow: hidden;">

  <!-- A-Frame AR Scene 설정 -->
  <a-scene embedded arjs>
    
    <!-- 커스터마이징된 마커 사용 (pattern-mark.patt) -->
    <a-marker type="pattern" url="pattern-mark.patt">
      <!-- index.html 경로에 있는 GLB 3D 모델 로드 -->
      <a-entity 
        gltf-model="index.html"  <!-- GLB 파일 경로 -->
        scale="0.5 0.5 0.5"       <!-- 모델 크기 조절 -->
        position="0 0 0"          <!-- 모델 위치 -->
        rotation="0 0 0">         <!-- 모델 회전 -->
      </a-entity>
    </a-marker>
    
    <!-- 카메라 설정 -->
    <a-entity camera></a-entity>
  
  </a-scene>
  
</body>
</html>
