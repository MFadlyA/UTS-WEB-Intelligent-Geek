<template>
    <div>
        <div class="container">
            <div class="row">
                <div class="mr40 mt20">
                    <router-link to="/list-voucher">
                        <img src="../../assets/icons/back.svg">
                    </router-link>
                </div>
                <div>
                    <h1 class="m0">UpdateVoucher</h1>
                    <p class="mt5 mb20 tc-green">Make your customers shop using vouchers</p>
                </div>
            </div>
            <hr class="uline-grey">
            <div class="mt50 row">
                <div class="w20">
                    <label class="form-label">Voucher Image</label>
                </div>
                <div class="w80">
                    <input
                        class="form-text"
                        type="image"
                        placeholder="Masukkan Kode Voucher"
                    >
                </div>
            </div>
            <div class="mt50 row">
                <div class="w20">
                    <label class="form-label">Voucher Code</label>
                </div>
                <div class="w80">
                    <input
                        class="form-text"
                        type="text"
                        placeholder="Masukkan Kode Voucher"
                        maxlength="6"

                    >
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Voucher Name</label>
                </div>
                <div class="w80">
                    <input
                        class="form-text"
                        type="text"
                        placeholder="Masukkan Voucher Name"
                        minlength="5"
                        maxlength="20"
                    >
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Description</label>
                </div>
                <div class="w80">
                    <input
                        class="form-text"
                        type="text"
                        placeholder="Masukkan Voucher Description"
                        maxlength="5000"
                    >
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Type</label>
                </div>
                <div class="w80">
                    <select class="form-select">
                        <option disabled selected>Pilih Type</option>
                        <option value="1">Total</option>
                        <option value="2">Grand Total</option>
                        <option value="3">Ongkos</option>
                    </select>
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Min. Transaction</label>
                </div>
                <div class="w80">
                    <input
                        class="form-text"
                        type="text"
                        placeholder="Masukkan Minimal Transaction"
                    >
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Amount</label>
                </div>
                <div class="w80">
                    <input
                        class="form-text"
                        type="text"
                        placeholder="Masukkan Amount"
                    >
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Valid From</label>
                </div>
                <div class="w80">
                    <input
                        class="form-text"
                        type="text"
                        placeholder="Masukkan Tanggal"
                    >
                </div>
            </div>
            <div class="mt30 row">
                <div class="w20">
                    <label class="form-label">Valid Untill</label>
                </div>
                <div class="w80">
                    <input
                        class="form-text"
                        type="text"
                        placeholder="Masukkan Tanggal"
                    >
                </div>
            </div>
            <div class="flex mt30">
                <router-link to="/list-voucher">
                    <button class="bt-submit-green">Update Voucher</button>
                </router-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
	name: 'edit-voucher'
}
</script>