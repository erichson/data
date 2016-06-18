R data-sets:

#'kaggle faces
#'
#' @description Grayscaled faces (8 bit [0-255]), 96x96 size. A few images of several different people
#' and 1500 total images. Each face image is flattened and stored as a column vector.
#'
#' @note This data-set is only a subset of the original kaggle face data-set,
#'  which includes about 7000 faces.
#'
#' @references Donated by Dr. Yoshua Bengio for the kaggle facial keypoints detection competion.
#'
#' @source \href{https://www.kaggle.com/c/facial-keypoints-detection}{kaggle}
#'
#' @examples
#' library(rsvd)
#' data(faces)
#'
#' #Display 10th face image
#' img <- matrix(rev(faces[,10]), nrow=96, ncol=96)
#' image(img, col=gray((0:255)/255))
#'


#'Highway
#'
#' @description 176x144 grayscaled (8 bit [0-255]) surveillance video with 200 frames.
#' Each frame is flattened, and stored as a column vector.
#'
#' @references N. Goyette, P.-M. Jodoin, F. Porikli, J. Konrad, and P. Ishwar,
#'            changedetection.net: A new change detection benchmark dataset,
#'            in Proc. IEEE Workshop on Change Detection (CDW-2012) at CVPR-2012,
#'            Providence, RI, 16-21 Jun., 2012.
#'
#' @source \href{http://changedetection.net/}{changedetection.net}
#'
#' @examples
#' library(rsvd)
#' data(highway)
#'
#' # Reshape and display the 100th frame:
#' frame <- matrix(highway[,100], ncol=144, nrow=176)
#' image(frame, col = gray((0:255)/255))
