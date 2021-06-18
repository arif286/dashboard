<template>
  <div>
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
        <tr>
          <td>{{ data }}</td>
          <td>{order.email}</td>
          <td>{order.serviceName}</td>
          <td>credit Card</td>
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
      type: Object,
      required: true
      default: ''
    }
  }
}
</script>
<style></style>
