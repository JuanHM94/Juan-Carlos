# Juan-Carlos
<context>
  <input pattern="(Hola|Buen dia) *">
    <output value="Hola $UserName!" if="full($UserName)"/>

    <context if="empty($UserName)">
      <output value="Hola! Cual es tu nombre?"/>

      <input pattern="$Text">
        <var name="UserName" value="$Text" scope="user"/>
        <output value="Hasta luego $UserName!"/>
      </input>

    </context>
  </input>
</context>
