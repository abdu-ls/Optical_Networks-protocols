************ How to run C1 Project 16*****************

1. Run floodlight
2. Run a topology on mininet: sudo mn --topo linear,3 --controller=remote,ip=127.0.0.1,port=6653 --switch ovsk,protocols=OpenFlow10
3. Implement the lightpath.py: python3 lightpath.py --src h1 --dst h3 --floodlight http://127.0.0.1:8080 --bidirectional
4. Show installations using floodlight REST API: curl http://127.0.0.1:8080/wm/core/switch/all/flow/json | jq

5. Show individual switches on mininet:
    sh ovs-ofctl dump-flows s1
    sh ovs-ofctl dump-flows s2
    sh ovs-ofctl dump-flows s3

ping test on mininet: h1 ping h3


************ How to run C3 Project 3*****************

1. Open Jupyter Notebook: https://jupyter.org/try-jupyter/lab/
2. Select the first tile; Python (Pyodide)
3. Copy the code from pulse_broadening-fiberlenght.py and paste a cell.
4. Click on the RUN button to see the results.

