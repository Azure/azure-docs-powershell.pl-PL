---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055398"
---
# Set-AzureAclConfig

## STRESZCZENIe
Modyfikuje obiekt konfiguracji ACL.

## POLECENIA

### AddRule
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### RemoveRule
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Setrule
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureAclConfig** modyfikuje obiekt konfiguracji listy kontroli dostępu (ACL) z istniejącej konfiguracji maszyny wirtualnej platformy Azure.

## Przykłady

### Przykład 1. Dodawanie reguły do nowej konfiguracji ACL
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

Pierwsze polecenie tworzy konfigurację listy ACL, a następnie zapisuje ją w zmiennej $Acl.

Drugie polecenie doda nową regułę do konfiguracji przechowywanej w $Acl.
Polecenie Określa akcję, podsieć, kolejność i opis reguły.

### Przykład 2: modyfikowanie reguły w konfiguracji ACL
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

Pierwsze polecenie pobiera maszynę wirtualną o nazwie VirtualMachine07 w usłudze o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureVM** .
Polecenie przekazuje ten obiekt do polecenia cmdlet **Get-AzureAclConfig** za pomocą operatora potoku.
To polecenie cmdlet pobiera konfigurację ACL dla punktu końcowego o nazwie sieć Web.
Polecenie zapisuje ten obiekt konfiguracji ACL w zmiennej $Acl.

Drugie polecenie modyfikuje regułę o IDENTYFIKATORze 0.
Polecenie zmieni kolejność i opis reguły.

Polecenie ostatnie ustawia obiekt konfiguracji ACL dla tej maszyny wirtualnej za pomocą polecenia cmdlet **Set-AzureEndpoint** .
Polecenie powoduje również zaktualizowanie tej maszyny wirtualnej.

### Przykład 3: Usuwanie reguły z konfiguracji listy ACL
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

Pierwsze polecenie zapisuje obiekt konfiguracji ACL w zmiennej $Acl.
Taki sam jak w poprzednim przykładzie.

Drugie polecenie usuwa regułę o IDENTYFIKATORze 0 z konfiguracji ACL w $Acl.

Polecenie ostatnie ustawia obiekt konfiguracji ACL dla maszyny wirtualnej i aktualizuje tę maszynę wirtualną.
Taki sam jak w poprzednim przykładzie.

## PARAMETRÓW

### -ACL
Określa obiekt konfiguracji ACL, który jest modyfikowany przez to polecenie cmdlet.

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Action
Określa akcję reguły, którą to polecenie cmdlet dodaje lub modyfikuje.
Prawidłowe wartości to: Permit i Deny.

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRule
Wskazuje, że to polecenie cmdlet dodaje regułę do konfiguracji ACL.

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Opis
Określa opis reguły, którą to polecenie cmdlet dodaje lub modyfikuje.

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Order (kolejność)
Określa kolejność przetwarzania dla reguły, którą to polecenie cmdlet dodaje lub modyfikuje.

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteSubnet
Określa podsieć zdalną dla reguły, którą to polecenie cmdlet dodaje lub modyfikuje.
Określa adres w formacie CIDR (Classless międzydomain Routing).

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRule
Wskazuje, że to polecenie cmdlet usuwa regułę z konfiguracji ACL.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleId
Określa identyfikator reguły, która jest usuwana lub modyfikowana przez to polecenie cmdlet dla konfiguracji ACL.

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Setrule
Wskazuje, że to polecenie cmdlet modyfikuje regułę w konfiguracji ACL.

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureAclConfig](./Get-AzureAclConfig.md)

[Get-AzureVM](./Get-AzureVM.md)

[Nowe — AzureAclConfig](./New-AzureAclConfig.md)

[Remove-AzureAclConfig](./Remove-AzureAclConfig.md)

[Set-AzureEndpoint](./Set-AzureEndpoint.md)

[Update-AzureVM](./Update-AzureVM.md)


