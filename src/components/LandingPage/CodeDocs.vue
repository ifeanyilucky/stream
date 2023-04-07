

<template>
    <div class="wrapper">



        <code>


                            <table>
                                <tr>
                                    <td>
                                        1
                                    </td>
                                    <td>{{ `query` }} <span class="title">getIsUserCurrentlyStreaming</span>{{ `($receiver:` }}<span
                                            class="type">String</span> {{ ` = "",` }}
                                    </td>
                                </tr>
                                <tr>
                                    <td>
                                        2
                                    </td>
                                    <td>{{ `$sender:` }}<span class="type">String</span> {{ `= "", $token:${' '}` }} <span
                                            class="type">String</span>{{ ` = "")` }} </td>
                                </tr>
                                <tr>
                                    <td>
                                        3
                                    </td>
                                    <td>{{ `{` }} </td>
                                </tr>
                                <tr>
                                    <td>
                                        4
                                    </td>
                                    <td><span class="title">{{ `streamPeriods` }} {{ `(` }}</span> </td>
                                </tr>
                                <tr>
                                    <td>
                                        5
                                    </td>
                                    <td>{{ ` where: {sender: $sender, receiver: $receiver, token: $token}` }} </td>
                                </tr>
                                <tr>
                                    <td>
                                        6
                                    </td>
                                    <td>{{ ` first:1` }} </td>
                                </tr>
                                <tr>
                                    <td>
                                        7
                                    </td>
                                    <td>{{ ` orderBy:startedAtTimestamp` }} </td>
                                </tr>
                                <tr>
                                    <td>
                                        8
                                    </td>
                                    <td>{{ ` orderDirection:desc` }} </td>
                                </tr>
                                <tr>
                                    <td>
                                        9
                                    </td>
                                    <td>{{ ` 	)  {` }} </td>
                                </tr>
                                <tr>
                                    <td>
                                        10
                                    </td>
                                    <td>{{ ` flowRate` }} </td>
                                </tr>
                                <tr>
                                    <td>
                                        11
                                    </td>
                                    <td>{{ ` stoppedAtTimestamp` }} </td>
                                </tr>
                                <tr>
                                    <td>
                                        12
                                    </td>
                                    <td>{{ ` }` }} </td>
                                </tr>
                                <tr>
                                    <td>
                                        13
                                    </td>
                                    <td>{{ ` }` }} </td>
                                </tr>
                            </table>
                        </code>

    </div>
</template>

<script lang="ts">
export default {
    name: 'CodeDocs',
}
</script>

<style scoped lang="scss">
.wrapper {
    border: 1px solid cadetblue;
    padding: 3rem 1rem;
    border-radius: 15px;

    tr {
        td:first-child {
            color: #929090
        }

        .type {
            color: rgb(227, 98, 9);
        }

        .title {
            color: #6542c1
        }
    }
}
</style>