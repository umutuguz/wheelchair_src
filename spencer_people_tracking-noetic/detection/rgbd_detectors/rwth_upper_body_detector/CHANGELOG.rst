^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package rwth_upper_body_detector
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.3.1 (2020-08-28)
------------------

1.3.0 (2020-08-26)
------------------
* Merge branch 'melodic' into noetic
* Contributors: Timm Linder

1.2.0 (2020-08-26)
------------------
* Merge branch 'master' into melodic
* Fixes required for ROS Melodic support
* Contributors: Timm Linder

1.0.11 (2020-08-26)
-------------------
* Adapt stability fixes to upper-body detector + config changes from LCAS (provided by Manuel in pull request `#59 <https://github.com/spencer-project/spencer_people_tracking/issues/59>`_, commit e5ca86b28c99) to the SPENCER version.
* Merge branch 'master' of https://github.com/MFernandezCarmona/spencer_people_tracking into master
* Merge pull request `#52 <https://github.com/spencer-project/spencer_people_tracking/issues/52>`_ from Sangheli/patch-1
  In upper-body detector, use correct dimensions of depth image (important when not using VGA resolution; otherwise part of image might not be used for detection)
* Fixed depth image converting to matrix when resolution!=640x480
* Contributors: Manuel Fernandez-Carmona, Timm Linder, Андрей Савельев

1.0.10 (2018-09-22)
-------------------
* Merge pull request `#47 <https://github.com/LCAS/spencer_people_tracking/issues/47>`_ from LCAS/master
  1.0.8
* Contributors: Timm Linder

1.0.9 (2018-01-17)
------------------

1.0.8 (2017-09-22)
------------------
* Merge pull request `#41 <https://github.com/LCAS/spencer_people_tracking/issues/41>`_ from LCAS/master
  1.0.7
* Contributors: Timm Linder

1.0.7 (2017-06-09)
------------------
* Add missing install targets
* Contributors: Timm Linder

1.0.6 (2017-06-09)
------------------

1.0.5 (2017-05-12)
------------------

1.0.4 (2017-05-12)
------------------

1.0.3 (2017-05-11)
------------------

1.0.2 (2017-05-09)
------------------
* added missing roslib deps
* Contributors: Marc Hanheide

1.0.1 (2017-05-09)
------------------
* homogenised all version strings to 1.0.0
* various install targets added that were missing
* Fix crash on startup of upper_body_detector
  If the upper_body_detector is initialized before the rgbd sensor and the
  depth image is received before the rgb image (as is the case with a
  kinect v1 using openni1 driver), color_image is an empty smart pointer
  and thus trying to access a member causes a segfault.
* check for if position is out of range
* Remap upper-body detector topics correctly for tracking_single_rgbd_sensor.launch to work with OpenNi1, `#20 <https://github.com/LCAS/spencer_people_tracking/issues/20>`_
* Fix license of upper-body detector
* Fix license of upper-body detector
* adjusted KConnectedComponentLabeler to drop depency to CPoint (due to license issues)
* In upper_body_detector, ensure that input depth image has proper encoding
* Minor optimization in upper_body_detector visualization
  Instead of using synchronizer for color and depth image, only subscribe to color image if visualization is enabled. This also reduces network traffic and RGB-D driver CPU load. Color image is not used by detector itself.
* Synching topic names with internal repo, changes from integration week III
* Update README.md
* Update package.xml
* Adding upper-body and groundHOG detectors
* Contributors: Kota Weaver, Marc Hanheide, Stefan Breuers, Timm Linder
