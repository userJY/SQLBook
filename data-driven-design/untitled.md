# Untitled

## ACID really just AID

<table>
  <thead>
    <tr>
      <th style="text-align:left">Title</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Atomic</td>
      <td style="text-align:left">If transaction breaks half-way, partial changes is reverted.</td>
    </tr>
    <tr>
      <td style="text-align:left">Consistency</td>
      <td style="text-align:left">
        <p>Shouldn&apos;t really belong; It is property of transaction design.
          <br
          />AID the rest are properties of the database.</p>
        <p>Basically same as program(transaction) invariant is maintained before
          and after if the program(transaction) is written correctly.</p>
        <p>Best example: Validation of datatypes</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Isolation</td>
      <td style="text-align:left">
        <p>Client never see an dirty state with partial transaction.</p>
        <p>Concurrent access to same resource doesn&apos;t create race condition.</p>
        <p>Serialization is ideal isolation but rarely used due to performance.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Durability</td>
      <td style="text-align:left">
        <p>Literally means data that is committed doesn&apos;t get wiped out by physical
          electronic failure.</p>
        <p>Replication provides best durability , database must wait until replication
          completes before transaction is successful.</p>
      </td>
    </tr>
  </tbody>
</table>

### Isolation

* Snapshot Isolation
  * Called "Repeatable read" in Postgres and MySQL

