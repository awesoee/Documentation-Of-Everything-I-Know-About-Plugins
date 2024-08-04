## Functions

| Function Name | Description |
| --------------------- | --------------------------------- |
| polar(**len**:number, **angle**:number) |    Platform-independent polar function for calculating the position of a point relative to 0,0 given a length and angle. <br/> <br/> **@param len** Distance from the origin. <br/> **@param angle** Angle around the origin to calculate the position in radians. |
| calculateAbsolutePivotPosition(**origin**:{ x:number; y:number}, **pivot**:{ x:number; y:number}, **rotationOffset**:number) | Calculates the absolute position of a pivot point provide an origin position, the pivot point position to the origin, and amount of rotation. This assumes a normal cartesian coordinate space, and rotation in the counter-clockwise direction is positive. <br/> <br/> **@param origin** The origin position with no rotation.  <br/> **@param pivot** The pivot position relative to the origin point. <br/>  **@param rotationOffset** Rotation to offset the pivot point in degrees (positive values are counter-clockwise). |
| rotatePointAroundPivot(**origin**:{ x:number; y:number}, **pivot**:{ x:number; y:number}, **fromRotation**:number, **toRotation**:number) | Rotates a point around a pivot anchor and returns the new position. This assumes a normal cartesian coordinate space, and rotation in the counter-clockwise direction is positive. <br/> <br/>  **@param origin** The origin position before rotation. <br/>  **@param pivot** The pivot position relative to the point given an initial rotation of 0 degrees. <br/>  **@param fromRotation** The current rotation of the origin (positive values are counter-clockwise). <br/>  **@param toRotation** The target rotation of the origin (positive values are counter-clockwise). |