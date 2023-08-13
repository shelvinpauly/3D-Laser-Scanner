# 3D-Laser-Scanner

## Abstract:

This project involved developing a low-cost 3D laser scanner using basic components like a laser pointer, plastic pen body as a cylindrical lens, stepper motor for rotation, webcam for image capture, and MATLAB for scan processing. The use of a pen body as the lens helped reduce the component costs significantly.

## Introduction:

3D scanning is used to digitize real-world objects into 3D mesh models. It has applications in design, manufacturing, quality inspection and reverse engineering. Commercial 3D scanners cost thousands of dollars. This project explored creating a DIY 3D scanner with basic components to provide hands-on experience in 3D scanning principles and techniques.

The goal was to build a rotating laser scanner that uses a line laser and camera to capture multiple views of an object which can then be processed to generate a 3D reconstruction. The main components identified were a laser, focusing optics, stepper motor for rotation, webcam for image capture, and MATLAB for scan processing.

## Methodology: 

The 3D scanner was designed as a rotating platform that spins the object while keeping the optics stationary. A 5mW 650nm laser pointer was used to generate a vertical laser line on the object surface. Instead of using a plano-convex lens, the transparent body of a plastic ballpoint pen was used as an inexpensive cylindrical lens. The transparent cylindrical tube served to focus the laser into a vertical line projection.

The object was placed on a 12 cm diameter rotating platform driven by a stepper motor and controlled via an Arduino Uno. A standard 1080p webcam captured images of the object with the laser line striking it at various angles during the rotation. 

The images were imported into MATLAB and processed to detect the laser line contours using Canny edge detection and Hough transforms. The x-y coordinates of the laser line were extracted from each frame and compiled into a 3D point cloud. Filtering and spatial transforms were applied to generate a closed 3D mesh model.

Results:

The 3D scanner successfully produced mesh models of objects with simple geometric shapes. A 6 inch tall vase was scanned by rotating it 360 degrees with 600 captured frames. The reconstructed model contained approximately 5000 vertices with 1 mm resolution. Some artifacts were noticed at the base due to occlusion. The use of a simple plastic pen body as the lens reduced the component cost significantly while providing the required light focusing.

The total cost of components was under $200, making it an affordable option for hobbyists. The use of a simple laser and webcam provided flexibility although resulted in lower resolution compared to commercial scanners. The MATLAB image processing pipeline provided a way to experiment with various 3D reconstruction algorithms. 

Conclusion:

The project achieved the goal of developing a low-cost rotating laser scanner capable of digitizing small objects. Key outcomes include:

- Designed and built scanner prototype with laser pointer, plastic pen body as lens, webcam, motor and microcontroller 

- Developed image processing pipeline in MATLAB to extract 3D point cloud from images

- Reconstructed multiple 3D mesh models from real objects scanned by the system

- Demonstrated an inexpensive method for getting started with 3D scanning techniques

Future work could explore using higher resolution cameras and multiple laser lines to improve model accuracy and speed. More advanced shape fitting and point cloud algorithms may help clean up the meshes. Overall, the project provided valuable insights into optical digitization and 3D reconstruction approaches.