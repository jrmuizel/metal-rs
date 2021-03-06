# Debugging in Xcode

Let's walk through an example of debugging the [`texture` example](/examples/texture).

---

Create a new project using the "External Build System" template.

![New project](./new-project.png)

---


Set the build command to be `cargo` and set the working directory to be the `metal-rs` repository.

Set the arguments to `build --package texture`

![Build settings](./build-settings.png)

---

Click `build` once in order to generate the executable.

> If you get any shader compilation errors edit your `Build Settings` with `LIBCLANG_PATH=/usr/local/opt/llvm/lib` after running `brew install llvm`.

`Product > Scheme > Edit Scheme` and choose the `metal-rs/target/texture` executable.

![Set run target](./set-run-target.png)

---

Now when you click `run` you should see the textured quad example in a window.

![Running window](./running-window.png)

---

From here you'll be able to use XCode's Metal debugging tools on your running application, such as capturing a GPU frame.

![Capture GPU frame](./capture-gpu-frame.png)

---

See [Developing and debugging shaders](https://developer.apple.com/documentation/metal/shader_authoring/developing_and_debugging_metal_shaders) for more infromation on
debugging Metal applications in XCode.

# Capture GPU Command Data to a File

TODO: Show an example of capturing data without using XCode by using the capture descriptor.

https://developer.apple.com/documentation/metal/frame_capture_debugging_tools/capturing_gpu_command_data_programmatically
