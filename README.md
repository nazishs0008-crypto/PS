# PS
PS-1
GATE-1
Q.1 A digital image is made up of pixels. There are different types of digital images.
Pixel is the smallest unit of digital image. And each pixel, at any location of image, stores a numerical value representing the colour and brightness of the image at that location.
Image Resolution shows the number of pixels in an image. The more will be the image resolution, the finer will be the details of the image.
A digital grayscale image can be represented mathematically as a two-dimensional matrix, in which each matrix element represents the intensity value of one pixel. Each number represents the intensity of the corresponding pixel. O represents black, 255 represents white, and intermediate values represent shades of gray.

Q.2 Basically RGB represents colourful images. In these images each pixel contains three primary colours, red, blue and green. And these combine to give different colours.
Grayscale images are those in which each pixel represents a shade of grey, depending on the intensity. 0 corresponding to black whereas 255 corresponding to white.
An autonomous vehicle may process RGB images to recognize traffic-light colours and road signs, while grayscale images may be used for tasks such as edge and lane detection. This is because RGB images gives us information about colour and brightness, whereas grayscale images gives us information about brightness only.

GATE-2
Q.1 Gaussian blur is an image-processing technique used to smooth an image by replacing each pixel's value with a weighted average of the surrounding pixels. The value of weight is calculated by using a gaussian function and in this process the image gets slightly blurry, that's why we call it gaussian blur.
It is useful because it smoothens the images, and makes it easier to detect the features.

Q.2 HSV stands for:
- H — Hue: Represents the actual colour, such as red, yellow, green, or blue.
- S — Saturation: Represents the intensity of the colour. High saturation means a vivid colour, while low saturation means a faded or grayish colour.
- V — Value: Represents the brightness of the colour. A low value is dark, while a high value is bright.
Autonomous vehicles use cameras to detect lane markings, which are often white or yellow. HSV can make it easier to identify these colours because unlike RGB, which represents colours using Red, Green, and Blue components, HSV separates colour information from brightness.

Q.3 Canny edge detection is an image-processing algorithm used to identify the boundaries of objects in an image by detecting significant changes in pixel intensity. It converts an image into an edge map, where the edges of objects appear as thin lines. It uses Gaussian smoothing, gradient calculation, non-maximum suppression, double thresholding, and edge tracking by hysteresis. And it is mainly used for detecting road lanes.

Q.4 A Region of Interest (ROI) is a specific area of an image selected for processing because it contains information relevant to the task. Instead of focusing on an entire image, we focus on a particular area of image.
In autonomous vehicles, ROI can restrict lane detection to the road area. It reduces false detections by excluding irrelevant regions, such as the sky and buildings, and can also reduce computational requirements by limiting the number of pixels processed.

GATE-3
Q.1 A contour represents the outline or shape of an object in a digital image.
It provides information about the object's shape, area, perimeter, position, bounding box, and orientation. In autonomous vehicles, contours can help analyze vehicle outlines, road regions, and lane markings, supporting object detection and scene understanding.

Q.2 The Hough Transform is an another computer vision technique used to detect geometric shapes, especially straight lines, in an image**.** It works by taking edge points from an image and determining which points are likely to belong to the same line.
It is useful for finding lane lines as it recognizes the edges from the images of the road.

GATE-4
Q.1 Lane/path detection is useful for an autonomous ground vehicle because it identifies road boundaries and lane markings, enabling the vehicle to determine a safe driving path. It supports lane keeping, steering control, path planning, navigation, and collision avoidance. By continuously estimating the vehicle's position relative to the road, it helps improve driving accuracy and safety.

Q.2  Shadows, road texture, poor lighting, missing markings, or clutter create false detections because these are unexpected or we can say undetermined events. They result in altering the colour, brightness, shapes and other prominent features of the images. This could lead these features to resemble actual lane markings or object boundaries. Consequently, computer vision algorithms may detect incorrect lanes, miss real lanes, or estimate the wrong path. All these leading to false detections.

Q.3 Lane detection alone is insufficient for a fully autonomous vehicle because it can only tell vehicle where the lane is and the region where it can move. But the other factors like detecting obstacles, recognizing traffic signs and signals, predicting the movements of other road users, planning safe paths are not covered under this. Therefore, lane detection must be combined with other perception, planning, and control systems to achieve safe autonomous driving.

GATE-5
Q.1 Perspective distortion is the apparent change in the size, shape, or relative position of objects when a three-dimensional scene is projected onto a two-dimensional image. Like the objects that are farther away from the side mirror often appear smaller, while objects closer to the side mirror appear larger.

Q.2 A Bird’s-Eye View (BEV) as the name suggests, is a representation of the environment as if it were being viewed from a bird's eye, like looking down at a road from an overhead drone. In autonomous vehicles, BEV can be generated by transforming camera images or combining data from multiple sensors, such as cameras, radar, and LiDAR, into a top-down representation.
A top-down representation make navigation-related perception easier as it simplifies navigation-related perception by making lane geometry, relative object positions, road boundaries, and drivable space easier to interpret. This helps autonomous vehicles with obstacle avoidance, path planning, and sensor fusion.

PS-2
GATE-1
Q.1 The basic difference between a path and a trajectory, lies in its mathematical representation. A path, is where the object moves, so it can be represented as a curve. Whereas, trajectory is represented as a function of time, it tells us the position of the object with time.

Q.2 A waypoint is an intermediate point that a robot or vehicle must pass through, or is instructed to visit, while moving toward its destination.
An obstacle is an object or region that prevents or restricts the robot from moving through a particular area.
Free space is the region in which the robot can move without colliding with obstacles, subject to its size and motion constraints.
The start state is the robot's initial condition from which planning or movement begins. It may include position, orientation, and velocity.
The goal is the desired final state or destination that the robot must reach.

GATE-2
Q.1 A 2D grid map is a representation of an environment divided into small square cells arranged in rows and columns. It helps a robot navigate from a start point to a goal while avoiding obstacles.

Q.2 An occupancy grid is a map used in robotics that divides an environment into small cells and assigns each cell a value representing the probability that it is occupied by an obstacle.

It helps a robot understand where obstacles are, where free space exists, and where it can safely move.

Q.3 In an occupancy grid map, every cell represents a small area of the environment. Based on sensor data, each cell is classified as free, occupied, or unknown.
A free cell represents an area believed to contain no obstacle. The robot can generally plan to move through it.
An occupied cell represents an area believed to contain an obstacle. The robot should avoid moving through it.
An unknown cell represents an area whose occupancy has not yet been determined. The robot does not know whether the area is free or occupied.

GATE-3 
Q.1 Breadth-First Search (BFS) is a graph-search algorithm that explores nodes level by level, starting from a source node. In robotics, it is used to find a shortest path on a 2D grid map when all allowed moves have equal cost.
In short we can say, it is used to  explore all nearby locations first, then locations farther away.

Q.2 Dijkstra’s algorithm finds the minimum-cost path from a start node to a goal node when movement costs are non-negative. In robotics, it is used on a 2D grid map where different cells or movements have different costs. Unlike BFS, which treats every move as having equal cost, Dijkstra considers the cost of the entire route.

Main difference between the both in terms of working principle is, use BFS when every move has the same cost. Use Dijkstra when movements have different non-negative costs and you want the minimum-total-cost route.

Q.3 A is a path-planning algorithm that finds a minimum-cost path by combining the cost already traveled with an estimate of the cost remaining to the goal.
A heuristic is an estimate of how much cost remains between the current node and the goal. It helps A* decide which direction is promising, without needing to explore every possible route first.

GATE-4
Q.1 The main difference is that a global path tells the robot where to go overall, while a local motion decision determines how to move right now based on nearby obstacles and current conditions. The common algorithms used by both are A*, Dijkstra and DWA, potential fields, model predictive control respectively.

Q.2 Autonomous vehicles re-plan because the real world changes dynamically. Re-planning helps them adapt to new obstacles, avoid collisions, and continue toward their destination safely. If no safe maneuver is available, the vehicle should slow down or stop.
