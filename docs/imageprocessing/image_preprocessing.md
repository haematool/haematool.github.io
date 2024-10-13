# Image Processing Filters

## Median Blur

The **median blur** filter is useful for removing salt and pepper noise from an image. It works by replacing each pixel with the median value of its neighboring pixels. This can help smooth out isolated noisy pixels while preserving edges.

\begin{equation}
\hat{f}(x, y) = \text{median} \left\{ g(r, c) \right\}_{(r, c) \in S_{xy}}
\end{equation}

## Gaussian Blur

The **Gaussian blur** filter reduces detail and noise in an image. It “blurs” the image by applying a Gaussian function to each pixel and its surrounding pixels. This helps smooth edges and details in preparation for edge detection or other processing techniques. The amount of smoothing is controlled by the parameter \(\sigma\), which determines how much the image will be blurred.

\begin{equation}
h(u, v) = \frac{1}{2\pi\sigma^2} e^{-\frac{u^2 + v^2}{2\sigma^2}}
\end{equation}

## Laplacian Filter

The **Laplacian filter** highlights regions of rapid intensity change. Any feature with a sharp discontinuity is enhanced by a Laplacian operator. This filter is a second-order filter used in image processing for edge detection and feature extraction. Unlike first-order derivative filters (like Sobel), which detect edges in specific directions (horizontal and vertical), the Laplacian detects all edges regardless of direction.

To detect edges in noisy images, we typically smooth the image first using a Gaussian filter, and then apply the Laplacian filter. This combination is known as the **Laplacian of Gaussian (LoG)** filter, and its mathematical representation is:

\begin{equation}
LoG(x, y) = -\frac{1}{\pi \sigma^4} \left[ 1 - \frac{x^2 + y^2}{2\sigma^2} \right] e^{-\frac{x^2 + y^2}{2\sigma^2}}
\end{equation}

!!! tip

    The **LoG operator** calculates the second spatial derivative of an image. This means that in areas where the image has constant intensity (i.e., where the intensity gradient is zero), the LoG response will be zero. Near intensity changes, however, the LoG response will be:

    - Positive on one side of the edge,
    - Negative on the other side,
    - Zero at some point in between, exactly at the edge itself.

This behavior makes the **LoG** an effective method for edge detection.

## Canny Filter

The **Canny filter** is a more advanced method for edge detection in images. It combines several steps to ensure precise edge detection while reducing false positives. The algorithm follows four main steps:

1. **Gaussian Smoothing**: Similar to the LoG filter, the Canny filter starts by smoothing the image with a Gaussian blur to reduce noise and improve edge detection accuracy.
2. **Gradient Calculation**: Next, the algorithm computes the gradient of the image, usually using a Sobel filter or another derivative-based filter, to estimate the direction and magnitude of intensity changes.
3. **Non-Maximum Suppression**: After calculating the gradient, non-maximum suppression is applied, which keeps only the points where the gradient is strongest and discards others, eliminating spurious edges.
4. **Double Threshold and Hysteresis**: Finally, a double threshold technique is used to identify strong and weak edges. Pixels with values above the high threshold are marked as edges, while pixels between the high and low thresholds are considered edges only if they are connected to strong edges (hysteresis).

The Canny filter is highly effective for applications requiring precise edge detection, such as object recognition or computer vision systems.

## Sobel Filter

The **Sobel filter** is another derivative-based filter used for edge detection. Unlike the LoG, it is a **first-order derivative** filter, which detects edges by calculating the first derivative of the image's intensity. The Sobel filter is simple and effective at detecting edges in specific directions.

The Sobel filter uses two convolution matrices to compute the **gradient** of the image's intensity in the x and y directions:

\begin{equation}
G_x = 
\begin{bmatrix}
-1 & 0 & +1 \\
-2 & 0 & +2 \\
-1 & 0 & +1
\end{bmatrix}, \quad
G_y = 
\begin{bmatrix}
-1 & -2 & -1 \\
 0 &  0 &  0 \\
+1 & +2 & +1
\end{bmatrix}
\end{equation}

These matrices detect gradients in the horizontal and vertical directions, respectively. By combining the two gradients, we can obtain the overall gradient magnitude \( G \) using the formula:

\begin{equation}
G = \sqrt{G_x^2 + G_y^2}
\end{equation}

The Sobel filter is particularly useful for detecting edges in horizontal and vertical directions but may be less sensitive compared to more advanced methods like the **Canny filter**.

## Bilateral Filter

The bilateral filter is a non-linear filter that smooths images while preserving edges. Unlike other filters like Gaussian blur, which only consider spatial distance when smoothing, the bilateral filter takes into account both the spatial distance and the intensity difference between pixels. This dual consideration makes it highly effective in preserving edges while reducing noise.

This filter worksby applying a spatial Gaussian filter $G_{\sigma_s}$ to measure the proximity between pixels and a range Gaussian filter $G_{\sigma_r}$ to account for the intensity difference. Pixels that are close spatially and have similar intensity values will be smoothed together, while pixels with significant intensity differences, such as those at edges, are preserved.

\begin{equation}
BF[I]_p = \frac{1}{W_p} \sum_{q \in S} G_{\sigma_s}(\|\mathbf{p} - \mathbf{q}\|) G_{\sigma_r}(I_p - I_q) I_q
\end{equation}
    
    



## Comparison of Filters (LoG, Canny, Sobel and Bilateral)

- **Sobel**: Used for fast and simple edge detection. It is sensitive to intensity changes along the x and y directions but doesn't handle noise well.
- **LoG**: More robust than Sobel, the Laplacian of Gaussian combines smoothing and edge detection. It's effective when the image contains noise.
- **Canny**: The Canny filter is one of the most effective edge detection methods, combining smoothing, gradient calculation, non-maximum suppression, and double thresholding. It's ideal for complex images that require precise edge detection.
- **Bilateral**: Unique in its ability to smooth images while preserving edges, the bilateral filter is ideal for reducing noise without sacrificing important image details such as in medical imaging, photography, and image segmentation tasks.
