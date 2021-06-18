<template>
  <div>
    <div>{{ data }}</div>
    <table className="table table-borderless">
      <thead>
        <tr>
          <th className="text-secondary" scope="col">
            Name
          </th>
          <th className="text-secondary" scope="col">
            Email Id
          </th>
          <th className="text-secondary" scope="col">
            Service
          </th>
          <th className="text-secondary" scope="col">
            pay with
          </th>
          <th className="text-secondary" scope="col">
            status
          </th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in data" :key="item.case">
          <td>{{ item.equipmentTag }}</td>
          <td>{{item.component}}</td>
          <td>{{item.assessmentDate}}</td>
          <td>{item.}</td>
          <!-- <td>
            <select
              onBlur="{()"
              =
            >
              {
              handleUpdate(order._id);
              }}
              onChange={handleChange}
              className="form-select"
              aria-label="Default select example"
              >
              <option value="{order.status}">
                Pending
              </option>
              <option value="On going">
                On going
              </option>
              <option value="Done">
                Done
              </option>
            </select>
          </td> -->
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  props: {
    data: {
      type: Array,
      required: true
    }
  }
}
</script>
<style></style>
