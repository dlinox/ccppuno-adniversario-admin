<template>
  <v-card class="mx-auto" style="max-width: 600px">
    <v-toolbar theme="dark" density="compact" title="Validar participantes" />
    <v-card-item>
      <v-text-field class="pa-5" label="Buscar"></v-text-field>
    </v-card-item>
    <v-divider></v-divider>
    <v-toolbar
      color="primary"
      density="compact"
      title="654654654654 - JUAN PERES"
    />

    <v-list-item
      class="py-3"
      title="HABIL S/. 20"
      subtitle="El boleto aun no fue usado"
    >
      <template v-slot:append>
        <v-btn color="primary" variant="tonal"> Ingreso </v-btn>
      </template>
    </v-list-item>

    <v-list-item
      class="py-3"
      title="INHABIL / OTROS S/. 50"
      subtitle="El boleto aun no fue usado"
    >
      <template v-slot:append>
        <v-btn color="primary" variant="tonal"> Ingreso </v-btn>
      </template>
    </v-list-item>

    <v-list-item
      class="py-3"
      title="INHABIL / OTROS S/. 50"
      subtitle="El boleto ya fue usado"
    >
      <template v-slot:append>
        <v-btn disabled color="red" variant="flat"> usado </v-btn>
      </template>
    </v-list-item>
  </v-card>
</template>
