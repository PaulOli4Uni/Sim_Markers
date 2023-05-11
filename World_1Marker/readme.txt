Follwing Commands used 

Running simulation
gz sim -v 3 Marker3_PoseToFile.sdf 

Start Recording (will place recording in working directory)
gz service -s /boxes_full_2d --timeout 2000 --reqtype gz.msgs.VideoRecord --reptype gz.msgs.Boolean --req 'start:true, save_filename:"name.mp4"'
Stop Recording
gz service -s /boxes_full_2d --timeout 2000 --reqtype gz.msgs.VideoRecord --reptype gz.msgs.Boolean --req 'start:false, save_filename:"name.mp4"'

Running pose_movement file
gz topic -t /file -m gz.msgs.StringMsg -p 'data:"/home/stb21753492/Sim_Markers/World_1Marker/pose_file2.txt"'

Storing Pose information of camera
gz service -s /pose_to_file --timeout 2000 --reqtype gz.msgs.VideoRecord --reptype gz.msgs.Int32 --req 'start:true, save_filename:"name.txt"'

