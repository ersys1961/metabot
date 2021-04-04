# Синтаксис JavaScript с условием

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x424;&#x443;&#x43D;&#x43A;&#x446;&#x438;&#x44F; / &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x430;&#x44F;</th>
      <th
      style="text-align:left">&#x41E;&#x43F;&#x438;&#x441;&#x430;&#x43D;&#x438;&#x435;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#x414;&#x430;&#x43D;&#x43D;&#x44B;&#x435; &#x43F;&#x43E; &#x431;&#x43E;&#x442;&#x443;</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">bot.getData(&apos;leadsCount&apos;)</td>
      <td style="text-align:left">
        <p>&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; &#x43A;&#x43E;&#x43B;&#x438;&#x447;&#x435;&#x441;&#x442;&#x432;&#x43E;
          &#x43B;&#x438;&#x434;&#x43E;&#x432; &#x442;&#x435;&#x43A;&#x443;&#x449;&#x435;&#x433;&#x43E;
          &#x431;&#x43E;&#x442;&#x430;.
          <br />
        </p>
        <p>&#x41D;&#x430;&#x43F;&#x440;&#x438;&#x43C;&#x435;&#x440;</p>
        <p>if (bot.getData(&apos;leadsCount&apos;) &gt; 0) {... &#x412;&#x43C;&#x435;&#x441;&#x442;&#x43E;
          leadsCount &#x43C;&#x43E;&#x436;&#x43D;&#x43E; &#x443;&#x43A;&#x430;&#x437;&#x430;&#x442;&#x44C;
          &#x43B;&#x44E;&#x431;&#x43E;&#x435; &#x43F;&#x43E;&#x43B;&#x435; &#x431;&#x43E;&#x442;&#x430;
          &#x438;&#x437; &#x442;&#x430;&#x431;&#x43B;&#x438;&#x446;&#x44B; &#x411;&#x414;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&#x410;&#x442;&#x440;&#x438;&#x431;&#x443;&#x442;&#x44B;-&#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x44B;&#x435; &#x431;&#x43E;&#x442;&#x430;</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">bot.setAttr(string $key, string $value)</td>
      <td style="text-align:left">&#x423;&#x441;&#x442;&#x430;&#x43D;&#x43E;&#x432;&#x438;&#x442;&#x44C;
        &#x437;&#x43D;&#x430;&#x447;&#x435;&#x43D;&#x438;&#x435; &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x43E;&#x439;
        &#x431;&#x43E;&#x442;&#x430;, &#x434;&#x430;&#x43D;&#x43D;&#x44B;&#x435;
        &#x431;&#x443;&#x434;&#x443;&#x442; &#x441;&#x43E;&#x445;&#x440;&#x430;&#x43D;&#x435;&#x43D;&#x44B;
        &#x432; &#x411;&#x414;</td>
    </tr>
    <tr>
      <td style="text-align:left">bot.getAttr(string $key)</td>
      <td style="text-align:left">&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; &#x437;&#x43D;&#x430;&#x447;&#x435;&#x43D;&#x438;&#x435;
        &#x441;&#x43E;&#x445;&#x440;&#x430;&#x43D;&#x435;&#x43D;&#x43D;&#x43E;&#x439;
        (&#x432; &#x431;&#x43E;&#x442;&#x435;) &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x43E;&#x439;
        &#x43F;&#x43E; &#x43A;&#x43B;&#x44E;&#x447;&#x443;</td>
    </tr>
    <tr>
      <td style="text-align:left">bot.getAllAttr(): array</td>
      <td style="text-align:left">&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; &#x43C;&#x430;&#x441;&#x441;&#x438;&#x432;
        &#x432;&#x441;&#x435;&#x445; &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x44B;&#x445;
        &#x431;&#x43E;&#x442;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left">bot.isAttrExist(string $key): bool</td>
      <td style="text-align:left">&#x41F;&#x440;&#x43E;&#x432;&#x435;&#x440;&#x438;&#x442;&#x44C; &#x43D;&#x430;&#x43B;&#x438;&#x447;&#x438;&#x435;
        &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x43E;&#x439;
        &#x432; &#x431;&#x43E;&#x442;&#x435;</td>
    </tr>
    <tr>
      <td style="text-align:left">bot.issetAttr(string $key): bool</td>
      <td style="text-align:left">&#x41F;&#x440;&#x43E;&#x432;&#x435;&#x440;&#x438;&#x442;&#x44C; &#x43D;&#x430;&#x43B;&#x438;&#x447;&#x438;&#x435;
        &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x43E;&#x439;
        &#x432; &#x431;&#x43E;&#x442;&#x435; (&#x430;&#x43B;&#x438;&#x430;&#x441;
        &#x444;&#x443;&#x43D;&#x43A;&#x446;&#x438;&#x438; bot.isAttrExist)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&#x414;&#x430;&#x43D;&#x43D;&#x44B;&#x435; &#x43F;&#x43E; &#x41B;&#x438;&#x434;&#x443;</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getData(string $key)): mixed|null</td>
      <td style="text-align:left">
        <p>&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; &#x437;&#x43D;&#x430;&#x447;&#x435;&#x43D;&#x438;&#x435;
          &#x434;&#x430;&#x43D;&#x43D;&#x44B;&#x445; &#x43F;&#x43E; &#x441;&#x443;&#x449;&#x43D;&#x43E;&#x441;&#x442;&#x438;
          &#x43B;&#x438;&#x434; &#x43F;&#x43E; &#x43A;&#x43B;&#x44E;&#x447;&#x443;.
          <br
          />
        </p>
        <p>&#x412; &#x43A;&#x430;&#x447;&#x435;&#x441;&#x442;&#x432;&#x435; &#x43A;&#x43B;&#x44E;&#x447;&#x430;
          &#x43C;&#x43E;&#x436;&#x43D;&#x43E; &#x443;&#x43A;&#x430;&#x437;&#x430;&#x442;&#x44C;
          <br
          />
        </p>
        <p>id</p>
        <p>identification</p>
        <p>manager_id</p>
        <p>bot_id</p>
        <p>channel_id</p>
        <p>status_id</p>
        <p>extra</p>
        <p>is_mute</p>
        <p>+ &#x432;&#x441;&#x435; &#x441;&#x438;&#x441;&#x442;&#x435;&#x43C;&#x43D;&#x44B;&#x435;
          &#x43F;&#x43E;&#x43B;&#x44F; &#x43B;&#x438;&#x434;&#x430; (&#x43F;&#x43E;
          &#x430;&#x43D;&#x433;&#x43B;&#x438;&#x439;&#x441;&#x43A;&#x438;)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">lead.isDataExist(string $key): bool</td>
      <td style="text-align:left">&#x41F;&#x440;&#x43E;&#x432;&#x435;&#x440;&#x438;&#x442;&#x44C; &#x43D;&#x430;&#x43B;&#x438;&#x447;&#x438;&#x435;
        &#x434;&#x430;&#x43D;&#x43D;&#x44B;&#x445; &#x43F;&#x43E; &#x43B;&#x438;&#x434;&#x443;</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.isDataExist(string $key): bool</td>
      <td style="text-align:left">&#x421;&#x438;&#x43D;&#x43E;&#x43D;&#x438;&#x43C; &#x43C;&#x435;&#x442;&#x43E;&#x434;&#x430;
        lead.issetData()</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getSerialNumber(): int|null</td>
      <td style="text-align:left">&#x41F;&#x43E;&#x440;&#x44F;&#x434;&#x43A;&#x43E;&#x432;&#x44B;&#x439;
        &#x43D;&#x43E;&#x43C;&#x435;&#x440; &#x43B;&#x438;&#x434;&#x430; &#x432;
        &#x442;&#x435;&#x43A;&#x443;&#x449;&#x435;&#x43C; &#x431;&#x43E;&#x442;&#x435;
        (&#x43D;&#x430;&#x447;&#x438;&#x43D;&#x430;&#x44F; &#x441; 1)</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getChannelCode(): string</td>
      <td style="text-align:left">&#x41A;&#x43E;&#x434; &#x43A;&#x430;&#x43D;&#x430;&#x43B;&#x430; &#x43B;&#x438;&#x434;&#x430;
        (telegram, umnico, bitrix, &#x438; &#x43F;&#x440;.)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&#x410;&#x442;&#x440;&#x438;&#x431;&#x443;&#x442;&#x44B;-&#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x44B;&#x435; &#x43B;&#x438;&#x434;&#x430;</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">lead.setAttr(string $key, string $value): self</td>
      <td style="text-align:left">&#x423;&#x441;&#x442;&#x430;&#x43D;&#x43E;&#x432;&#x438;&#x442;&#x44C;
        &#x437;&#x43D;&#x430;&#x447;&#x435;&#x43D;&#x438;&#x435; &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x43E;&#x439;
        &#x43B;&#x438;&#x434;&#x430;, &#x434;&#x430;&#x43D;&#x43D;&#x44B;&#x435;
        &#x431;&#x443;&#x434;&#x443;&#x442; &#x441;&#x43E;&#x445;&#x440;&#x430;&#x43D;&#x435;&#x43D;&#x44B;
        &#x432; &#x411;&#x414;</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getAttr(string $key): string|null</td>
      <td style="text-align:left">&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; &#x43F;&#x43E;
        &#x43A;&#x43B;&#x44E;&#x447;&#x443; &#x437;&#x43D;&#x430;&#x447;&#x435;&#x43D;&#x438;&#x435;
        &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x43E;&#x439;
        &#x43B;&#x438;&#x434;&#x430; (&#x441;&#x43E;&#x445;&#x440;&#x430;&#x43D;&#x435;&#x43D;&#x43D;&#x43E;&#x439;
        &#x432; &#x411;&#x414;)</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getAllAttr(): array</td>
      <td style="text-align:left">&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; &#x43C;&#x430;&#x441;&#x441;&#x438;&#x432;
        &#x432;&#x441;&#x435;&#x445; &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x44B;&#x445;
        &#x43B;&#x438;&#x434;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left">bot.isAttrExist(string $key): bool</td>
      <td style="text-align:left">&#x41F;&#x440;&#x43E;&#x432;&#x435;&#x440;&#x438;&#x442;&#x44C; &#x43D;&#x430;&#x43B;&#x438;&#x447;&#x438;&#x435;
        &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x43E;&#x439;
        &#x43B;&#x438;&#x434;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left">bot.issetAttr(string $key): bool</td>
      <td style="text-align:left">&#x41F;&#x440;&#x43E;&#x432;&#x435;&#x440;&#x438;&#x442;&#x44C; &#x43D;&#x430;&#x43B;&#x438;&#x447;&#x438;&#x435;
        &#x43F;&#x435;&#x440;&#x435;&#x43C;&#x435;&#x43D;&#x43D;&#x43E;&#x439;
        &#x43B;&#x438;&#x434;&#x430; (&#x430;&#x43B;&#x438;&#x430;&#x441; &#x444;&#x443;&#x43D;&#x43A;&#x446;&#x438;&#x438;
        lead.isAttrExist)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&#x422;&#x44D;&#x433;&#x438; &#x43B;&#x438;&#x434;&#x430;</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">lead.isTagExist(&apos;some_tag&apos;)</td>
      <td style="text-align:left">&#x41F;&#x440;&#x43E;&#x432;&#x435;&#x440;&#x438;&#x442;&#x44C; &#x43D;&#x430;&#x43B;&#x438;&#x447;&#x438;&#x435;
        &#x442;&#x44D;&#x433;&#x430; &#x43B;&#x438;&#x434;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getTag(string $key): string|null</td>
      <td style="text-align:left">&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; &#x43D;&#x430;&#x437;&#x432;&#x430;&#x43D;&#x438;&#x435;
        &#x442;&#x44D;&#x433;&#x430; &#x43B;&#x438;&#x434;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getAllTags(): array</td>
      <td style="text-align:left">&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; &#x43C;&#x430;&#x441;&#x441;&#x438;&#x432;
        &#x432;&#x441;&#x435;&#x445; &#x43B;&#x438;&#x434;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&#x41A;&#x43E;&#x43D;&#x442;&#x435;&#x43A;&#x441;&#x442; &#x43B;&#x438;&#x434;&#x430;</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">lead.isContextExist(string $key): bool</td>
      <td style="text-align:left">&#x41F;&#x440;&#x43E;&#x432;&#x435;&#x440;&#x438;&#x442;&#x44C; &#x43D;&#x430;&#x43B;&#x438;&#x447;&#x438;&#x435;
        &#x43A;&#x43E;&#x43D;&#x442;&#x435;&#x43A;&#x441;&#x442;&#x430; &#x43B;&#x438;&#x434;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getContext(string $key): string|null</td>
      <td style="text-align:left">&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; &#x43D;&#x430;&#x437;&#x432;&#x430;&#x43D;&#x438;&#x435;
        &#x43A;&#x43E;&#x43D;&#x442;&#x435;&#x43A;&#x441;&#x442;&#x430; &#x43B;&#x438;&#x434;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getAllContexts(): array</td>
      <td style="text-align:left">&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; &#x43C;&#x430;&#x441;&#x441;&#x438;&#x432;
        &#x432;&#x441;&#x435;&#x445; &#x43A;&#x43E;&#x43D;&#x442;&#x435;&#x43A;&#x441;&#x442;&#x43E;&#x432;
        &#x43B;&#x438;&#x434;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&#x421;&#x442;&#x430;&#x442;&#x443;&#x441; &#x43B;&#x438;&#x434;&#x430;</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">lead.isInStatus(string $statusName): bool</td>
      <td style="text-align:left">&#x41F;&#x440;&#x43E;&#x432;&#x435;&#x440;&#x438;&#x442;&#x44C;, &#x447;&#x442;&#x43E;
        &#x43B;&#x438;&#x434; &#x43D;&#x430;&#x445;&#x43E;&#x434;&#x438;&#x442;&#x441;&#x44F;
        &#x432; &#x441;&#x442;&#x430;&#x442;&#x443;&#x441;&#x435; &#x441; &#x438;&#x43C;&#x435;&#x43D;&#x435;&#x43C;
        $statusName</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getStatusId(): int|null</td>
      <td style="text-align:left">&#x412;&#x43E;&#x437;&#x432;&#x440;&#x430;&#x449;&#x430;&#x435;&#x442;
        &#x437;&#x43D;&#x430;&#x447;&#x435;&#x43D;&#x438;&#x435; &#x43F;&#x43E;&#x43B;&#x44F;
        status_id &#x43B;&#x438;&#x434;&#x430; (&#x442;&#x43E; &#x436;&#x435; &#x441;&#x430;&#x43C;&#x43E;&#x435;,
        lead.getAttr(&quot;status_id&quot;)</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>&#x41C;&#x435;&#x442;&#x43E;&#x434;&#x44B; &#x43B;&#x438;&#x434;&#x430;</b>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">lead.getPersonId(): ?int</td>
      <td style="text-align:left">&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x438;&#x442;&#x44C; id &#x43F;&#x435;&#x440;&#x441;&#x43E;&#x43D;&#x44B;
        &#x43F;&#x440;&#x438;&#x432;&#x44F;&#x437;&#x430;&#x43D;&#x43D;&#x43E;&#x439;
        &#x43A; &#x43B;&#x438;&#x434;&#x443;</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.setPersonId(?int $personId): bool</td>
      <td style="text-align:left">&#x41F;&#x440;&#x438;&#x432;&#x44F;&#x437;&#x430;&#x442;&#x44C; &#x43F;&#x435;&#x440;&#x441;&#x43E;&#x43D;&#x443;
        &#x43A; &#x43B;&#x438;&#x434;&#x443; (&#x43F;&#x43E; id &#x43F;&#x435;&#x440;&#x441;&#x43E;&#x43D;&#x44B;)</td>
    </tr>
    <tr>
      <td style="text-align:left">lead.createPersonForCurrentLead($data): ?int</td>
      <td style="text-align:left">
        <p>&#x421;&#x43E;&#x437;&#x434;&#x430;&#x442;&#x44C; &#x43F;&#x435;&#x440;&#x441;&#x43E;&#x43D;&#x443;
          &#x434;&#x43B;&#x44F; &#x442;&#x435;&#x43A;&#x443;&#x449;&#x435;&#x433;&#x43E;
          &#x43B;&#x438;&#x434;&#x430; (&#x432; &#x43A;&#x43E;&#x43D;&#x442;&#x435;&#x43A;&#x441;&#x442;&#x435;
          &#x43A;&#x43E;&#x442;&#x43E;&#x440;&#x43E;&#x433;&#x43E; &#x437;&#x430;&#x43F;&#x443;&#x449;&#x435;&#x43D;
          v8-&#x441;&#x43A;&#x440;&#x438;&#x43F;&#x442;)</p>
        <p>&#x41F;&#x43E;&#x43B;&#x44F; &#x43F;&#x435;&#x440;&#x435;&#x434;&#x430;&#x432;&#x430;&#x435;&#x43C;&#x44B;&#x435;
          &#x432; &#x43E;&#x431;&#x44A;&#x435;&#x43A;&#x442; $data &#x441;&#x43C;&#x43E;&#x442;&#x440;&#x438;&#x442;&#x435;
          &#x432; &#x43E;&#x43F;&#x438;&#x441;&#x430;&#x43D;&#x438;&#x438; bot.createPerson(...)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">lead.setForwarded(bool|int $state): self</td>
      <td style="text-align:left">&#x423;&#x441;&#x442;&#x430;&#x43D;&#x43E;&#x432;&#x43A;&#x430; ($state
        == true) &#x438;&#x43B;&#x438; &#x441;&#x431;&#x440;&#x43E;&#x441; ($state
        == false) &#x443; &#x43B;&#x438;&#x434;&#x430; &#x43F;&#x440;&#x438;&#x437;&#x43D;&#x430;&#x43A;&#x430;
        &#x201C;&#x41F;&#x435;&#x440;&#x435;&#x432;&#x435;&#x434;&#x451;&#x43D;
        &#x43D;&#x430; &#x43E;&#x43F;&#x435;&#x440;&#x430;&#x442;&#x43E;&#x440;&#x430;&#x201D;</td>
    </tr>
  </tbody>
</table>

