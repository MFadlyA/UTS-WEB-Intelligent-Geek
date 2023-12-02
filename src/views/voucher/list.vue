<template>
    <div>
        <Menu/>
        <div class="container">
            <h1 class="m0">Voucher</h1>
            <div class="row">
                <div class="col">
                    <p class="mt5 mb20 tc-green">Manage your voucher promotion</p>
                </div>
                <div class="col flex">
                    <router-link to="/add-voucher">
                        <button class="bt-green">+ Add</button>
                    </router-link>
                </div>
            </div>
            <div class="row bg-blue mt10 p10">
                <div class="col">
                    <input
                        class="search-field"
                        type="text"
                        id="deskripsi"
                        placeholder="Tambah deskripsi..."
                    />
                </div>
                <div class="col flex">
                    <button class="bt-blue">Filter</button>
                </div>
            </div>
            <div class="mt50">
                <table>
                    <thead>
                        <tr>
                            <th>CODE VOUCHER</th>
                            <th>VOUCHER NAME</th>
                            <th>VALID FROM</th>
                            <th>VALID UNTILL</th>
                            <th>VOUCHER STATUS</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="item of list_voucher" :key="item.id">
                            <td class="center">{{ item.voucher_code }}</td>
                            <td class="center">{{ item.voucher_name }}</td>
                            <td class="center"><label class="label-green">{{ item.valid_from }}</label></td> 
                            <td class="center"><label class="label-green">{{ item.valid_until }}</label></td> 
                            <td class="center">
                                <div v-if="item.status === 1">
                                    <label class="label-green">Active</label>
                                </div>
                                <div v-else>
                                    <label class="label-red">Inactive</label>
                                </div>
                            </td>
                            <td class="center">
                                <div class="mt5">
                                    <router-link to="/edit-voucher">
                                        <img src="../../assets/icons/edit.svg">
                                    </router-link>
                                </div>
                                <div class="mt5">
                                    <router-link to="/detail-voucher">
                                        <img src="../../assets/icons/detail.svg">
                                    </router-link>
                                </div>
                                <div class="mt5">
                                    <img src="../../assets/icons/delete.svg">
                                </div>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>

<script>
import Menu from "../../components/menu.vue"

export default {
	name: 'list-voucher',
	components: {
		Menu
	},
    data(){
        return {
            // current_date:
            list_voucher: [
                {
                    id: "1",
                    voucher_code: "ABC123",
                    voucher_name: "November Ceria",
                    valid_from: "20-11-2023",
                    valid_until: "25-11-2023",
                    status: 1
                },
                {
                    id: "2",
                    voucher_code: "ABC123",
                    voucher_name: "November Ceria",
                    valid_from: "20-11-2023",
                    valid_until: "25-11-2023",
                    status: 1
                },
                {
                    id: "3",
                    voucher_code: "ABC123",
                    voucher_name: "November Ceria",
                    valid_from: "20-11-2023",
                    valid_until: "25-11-2023",
                    status: 2
                },
            ]
        }
    }
}
</script>