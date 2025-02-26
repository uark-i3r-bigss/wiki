---
title: /launch
---

<style type="text/css">
#mermaid {
    min-width: 600px;
    max-width: 1200px; 
    width: 200%; /* Set this value to whatever is appropriate for your use case, or use the height property instead */
    overflow-x: scroll;
}
</style>

<div id="mermaid">
{{< mermaid >}}
%%{init: { 'flowchart': {'useMaxWidth':false} } }%%
flowchart LR
    %% URWithSnakeHomewoodAll.launch
    subgraph spine_robot_control
    URWithSnakeHomewoodAll.launch --> URWithSnakeController.xml -->URWithSnakeLeadscrewActUnit:::orange
    URWithSnakeHomewoodAll.launch -->|path_to_main_dir:=$find spine_robot_control\n config_dir:=/config/homewood_ur5/| URWithSnakeHomewoodPeriphery.launch
    URWithSnakeHomewoodPeriphery.launch -->|base_marker_name:=LasercutBase1\n origin_to_base_marker_transform_filename:=$arg path_to_main_dir/$arg config_dir/urBaseToPolarisBaseMarker.txt| estimate_tracker_camera_location.launch-->EstimateTrackerCameraLocation:::orange
    URWithSnakeHomewoodPeriphery.launch-->view_UR5_frames_rviz.launch-->load_description_ur5.launch
    end
    view_UR5_frames_rviz.launch-->rviz:::blue
    view_UR5_frames_rviz.launch-->robot_state_publisher:::blue
    subgraph snake
    URWithSnakeHomewoodPeriphery.launch-->StartMaxonVelocityMode.launch-->startMaxon.xml-->startMaxonWithUI:::orange
    end
    subgraph ndi_tracker_ros
    URWithSnakeHomewoodPeriphery.launch -->|-j $arg path_to_main_dir/$arg config_dir/saw_ndi_tracker_config.json\n -s /dev/ttyUSB0| ndi_tracker:::orange
    end

    %% URWithSnakeHomewoodController.launch
    subgraph spine_robot_control
    URWithSnakeHomewoodController.launch-->URWithSnakeController.xml
    end

 classDef orange fill:#FFA500
 classDef blue   fill:#0047AB, color:white
{{< /mermaid >}}
</div>
