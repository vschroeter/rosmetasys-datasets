# Rosmetasys Datasets
Datasets gathered with [rosmetasys](https://github.com/vschroeter/rosmetasys) and used for [RosComGraph](https://vschroeter.github.io/RosComGraph/#/) and [VisCom](https://github.com/vschroeter/viscom) (WiP).

# Contribute Datasets

**By Issue:**
Create an Issue with the [Providing a new Dataset](https://github.com/vschroeter/rosmetasys-datasets/issues/new?assignees=vschroeter&labels=dataset&projects=&template=providing-a-new-dataset-.md&title=%5BDATASET%5D+New+dataset) template and attach your .json or .zip file created with [rosmetasys](https://github.com/vschroeter/rosmetasys).

**By Pull Request:**
You also submit your dataset by creating a pull request. 
Fork the repository and make sure to add your dataset .json to the `datasets` folder.

**By Email:**
If you want to anonymously submit your dataset without creating a pull request and have it uploaded to the repository, you can zip your dataset and send it to me via email (valentin.schroeter@hpi.uni-potsdam.de). 

# Usage of the datasets

The objective of the data gathering is to create an open-source, accessible dataset in accordance with the [FAIR-Principles](https://www.go-fair.org/fair-principles/). 
Snapshots of the dataset may be published as a collection on [Zenodo](https://zenodo.org/).

# Format of the datasets

```json
{
    "version": "1.0.0",
    "created_at": "2024-01-01T10:40:40.000000",
    "name": "...",
    "description": "...",
    "nodeCount": 20,
    "author": "...",
    "cc_by_sa_consent": true,
    "nodes": [
        {
            "name": "first_node",
            "namespace": "/",
            "localhost_only": true,
            "publishers": [
                {
                    "name": "/parameter_events",
                    "type": "rcl_interfaces/msg/ParameterEvent"
                },
                {
                    "name": "/my/topic/1",
                    "type": "std_msgs/msg/Empty"
                },
                {
                    "name": "/rosout",
                    "type": "rcl_interfaces/msg/Log"
                }
            ],
            "subscribers": [
                {
                    "name": "/my/topic/1",
                    "type": "std_msgs/msg/Empty"
                },
                {
                    "name": "/my/topic/2",
                    "type": "custom_type"
                }
            ],
            "services": [
                ...
            ],
            "clients": [
                ...
            ]
        },
        {
            "name": "second_node",
            "namespace": "/",
            "localhost_only": false,
            ...
        }
    ]
}

```

See [rosmetasys](https://github.com/vschroeter/rosmetasys) for more information on exporting datasets.
