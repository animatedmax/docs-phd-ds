---
title: Creating an External Service Plan
owner: Pivotal HD
---

To create an External Service Plan:

<ol>
            <li>Use a Web browser to open the Pivotal Ops Manager application. (This application is part of your <a href="https://network.pivotal.io/products/pivotal-cf">Pivotal Cloud Foundry&reg;</a> (PCF) installation.) </li>
            <li>Click the <strong>Pivotal HD for PCF</strong> tile. </li>
            <li>Select <strong>External Service Plans</strong>. <p>The External Service Plans screen displays.</p></li>
            <li>Click <strong>Add</strong> to create a new Service Plan. </li>
            <li>Configure the following options for your Service Plan. This information displays in the Apps Manager and command line interface:<table rules="all"
                    frame="void">
                    <caption>Informational Display</caption>
                    <col
                        width="33%" />
                    <col
                        width="33%" />
                    <col
                        width="33%" />
                    <thead>
                        <tr>
                            <th>Parameter</th>
                            <th>Description</th>
                            <th>Values</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Service Plan Name</td>
                            <td>(Required) The name you want PCF users to see in the CLI and Apps Manager. </td>
                            <td>String</td>
                        </tr>
                        <tr>
                            <td>Service Plan Feature Bullet 1 </td>
                            <td
                                rowspan="3"> The details of the service plan you want PCF users to see. The values in these fields display to users in the Marketplace section of the Apps Manager. </td>
                            <td
                                rowspan="3">String</td>
                        </tr>
                        <tr>
                            <td>Service Plan Feature Bullet 2</td>
                        </tr>
                        <tr>
                            <td>Service Plan Feature Bullet 3</td>
                        </tr>
                    </tbody>
                </table></li>
            <li> Enter the following values regarding the cost of Pivotal HD clusters. These fields are for display only. The values in these fields display to users in the Marketplace section of the Apps Manager:<table rules="all"
                    frame="void">
                    <caption>Cost Information</caption>
                    <col
                        width="33%" />
                    <col
                        width="33%" />
                    <col
                        width="33%" />
                    <thead>
                        <tr>
                            <th>Parameter</th>
                            <th>Description</th>
                            <th>VAlues</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Amount</td>
                            <td> (Required) The cost, if any, in US dollars to create an instance of this Service Plan.  For example: inputting 1000 will display $1000 </td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Unit of Measurement</td>
                            <td> (Required) Unit of measurement used for billing.  For example: Monthly, or weekly. </td>
                            <td>String</td>
                        </tr>
                    </tbody>
                </table></li>
            <li>Select the Pivotal HD Components whose information you want to include in the Service Plan. If you do not select a component, the related input fields on the page for that component are ignored. You can select any of the following components: <table rules="all"
                    frame="void">
                    <caption>Pivotal HD Components</caption>
                    <col
                        width="50%" />
                    <col
                        width="50%" />
                    <thead>
                        <tr>
                            <th>Parameter</th>
                            <th>Description</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>HDFS</td>
                            <td> Controls whether to include information about the NameNode host and HDFS port, and the Web UI port. </td>
                        </tr>
                        <tr>
                            <td> Yarn/MapReduce2 </td>
                            <td> Controls whether to include information about the ResourceManager’s host and port, scheduler port, the Web UI port, and the JobHistoryServer’s UI port. </td>
                        </tr>
                        <tr>
                            <td>HAWQ</td>
                            <td> Controls whether to include information about the HAWQ Master’s host and port as well as the database name. </td>
                        </tr>
                        <tr>
                            <td>GemFire XD</td>
                            <td> Controls whether to include information about the GemFire XD Locator’s host and port. </td>
                        </tr>
                    </tbody>
                </table></li>
            <li> Enter the following values for all relevant fields of the Pivotal HD software where you want the Service Plan to broker access. These values you enter in these fields are displayed in the Service Instance Dashboard that PCF users can access when they create a Service Instance and/or in the <code>VCAP_SERVICES</code> environment variable that Applications can access when they are bound to the Service Instance. <table rules="all"
                    frame="void"
                    width="540">
                    <caption>Pivotal HD Configuration</caption>
                    <col
                        width="33%" />
                    <col
                        width="33%" />
                    <col
                        width="33%" />
                    <thead>
                        <tr>
                            <th>Parameter</th>
                            <th>Description</th>
                            <th>Values</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td> NameNode Host Address </td>
                            <td>The hostname or IP address of the NameNode.  For example:<ul>
                                    <li><code>namenode.pivotal.io</code></li>
                                    <li><code>10.1.1.1</code></li>
                                </ul>
                            </td>
                            <td>String</td>
                        </tr>
                        <tr>
                            <td> NameNode Port </td>
                            <td>The port number where the NameNode runs the HDFS protocol.  Typically this value is <code>8020</code>
                            </td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>NameNode UI Port</td>
                            <td> The port number where the NameNode Web interface runs. </td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Resource Manager Host Address</td>
                            <td> The hostname or IP address of the ResourceManager.  For example:<ul>
                                    <li><code>resourcemanager.pivotal.io</code></li>
                                    <li><code>10.2.2.2</code></li>
                                </ul>
                            </td>
                            <td>String</td>
                        </tr>
                        <tr>
                            <td>Resource Manager Port</td>
                            <td> The port number where the ResourceManager is running for application submissions.  Typically this is 8032 </td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Resource Manager Scheduler Port</td>
                            <td> The port where the ResourceManager runs the resource scheduler.  Typically this value is <code>8030</code>. </td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Resource Manger UI Port</td>
                            <td> The port where the Resource Manager Web interface runs.  Typically this value is <code>8088</code>. </td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>JobHistoryServer UI Port</td>
                            <td>The port that the the JobHistoryServer UI is listening.  Typically this value is <code>19888</code>. </td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>HAWQ Host Address</td>
                            <td> The hostname or IP address where the HAWQ Master is running. For example: <ul>
                                    <li><code>hawq.pivotal.io</code></li>
                                    <li><code>10.3.3.3</code></li>
                                </ul>
                            </td>
                            <td>String</td>
                        </tr>
                        <tr>
                            <td>HAWQ Host Port</td>
                            <td> The port where HAWQ is running for client connections.  Typically this value is <code>5432</code>. </td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>HAWQ Database</td>
                            <td> The HAWQ database that users can access. </td>
                            <td>String</td>
                        </tr>
                        <tr>
                            <td>GemFire XD Locator Host</td>
                            <td> The hostname or IP address where the GemFire XD Locator is running.  For example: <ul>
                                    <li><code>gemxd.pivotal.io</code></li>
                                    <li><code>10.4.4.4</code></li>
                                </ul></td>
                            <td>String</td>
                        </tr>
                        <tr>
                            <td>GemFire XD Locator Port</td>
                            <td> The port where the GemFire XD Locator is running for client connections.  Typically this value is <code>1527</code>. </td>
                            <td>Integer</td>
                        </tr>
                    </tbody>
                </table></li>
            <li>(Optional) Repeat the steps above to create additional <strong>External Service Plans</strong>.</li>
            <li>Click <strong>Save</strong> to save the service plan(s).</li>
        </ol>
