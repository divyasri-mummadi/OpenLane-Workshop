# Commands Sheet

This file contains some of the commonly used commands from the VSD OpenLane Workshop.

---

# Linux Commands

### Show current directory

```bash
pwd
```

Displays the current working directory.

---

### List files and folders

```bash
ls
```

Lists all files and folders in the current directory.

---

### Change directory

```bash
cd <directory_name>
```

Moves into the specified directory.

Example:

```bash
cd designs/picorv32a
```

---

### Go back one directory

```bash
cd ..
```

Moves to the parent directory.

---

# Starting OpenLane

Move to the OpenLane directory.

```bash
cd ~/Desktop/work/tools/openlane_working_dir/openlane
```

Start Docker.

```bash
docker
```

Launch OpenLane in interactive mode.

```bash
./flow.tcl -interactive
```

---

# OpenLane Commands

Load the OpenLane package.

```tcl
package require openlane 0.9
```

Prepare the design.

```tcl
prep -design picorv32a
```

Run synthesis.

```tcl
run_synthesis
```

Run floorplanning.

```tcl
run_floorplan
```

Run placement.

```tcl
run_placement
```

Run Clock Tree Synthesis.

```tcl
run_cts
```

Run routing.

```tcl
run_routing
```

---

# Viewing Layouts in Magic

Open the generated floorplan.

```bash
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def
```

---

# Magic DRC

Open Magic using the workshop technology file.

```bash
magic -d XR
```

---

# Useful Navigation

Exit OpenLane interactive mode.

```tcl
exit
```

or

```tcl
quit
```

---

