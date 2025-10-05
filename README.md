************ How to run *****************

1. Run floodlight
2. Run a topology on mininet: sudo mn --topo linear,3 --controller=remote,ip=127.0.0.1,port=6653 --switch ovsk,protocols=OpenFlow10
3. Implement the lightpath.py: python3 lightpath.py --src h1 --dst h3 --floodlight http://127.0.0.1:8080 --bidirectional
4. Show installations using floodlight REST API: curl http://127.0.0.1:8080/wm/core/switch/all/flow/json | jq

5. Show individual switches on mininet:
    sh ovs-ofctl dump-flows s1
    sh ovs-ofctl dump-flows s2
    sh ovs-ofctl dump-flows s3

ping test on mininet: h1 ping h3
