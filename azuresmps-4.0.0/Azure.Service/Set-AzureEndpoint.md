---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055023"
---
# Set-AzureEndpoint

## STRESZCZENIe
Modyfikuje punkt końcowy przypisany do maszyny wirtualnej.

## POLECENIA

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureEndpoint** modyfikuje punkt końcowy przypisany do maszyny wirtualnej platformy Azure.
Możesz określić zmiany w punkcie końcowym, który nie jest zrównoważony względem obciążenia.

## Przykłady

### Przykład 1: modyfikowanie punktu końcowego w celu nasłuchiwania na porcie
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

To polecenie pobiera konfigurację maszyny wirtualnej o nazwie VirtualMachine01 przy użyciu polecenia cmdlet **Get-AzureVM** .
Polecenie przekazuje je do bieżącego polecenia cmdlet za pomocą operatora potoku.
To polecenie cmdlet modyfikuje punkt końcowy o nazwie sieć Web w celu odsłuchiwania na porcie 443.
Polecenie przekazuje obiekt maszyny wirtualnej do polecenia cmdlet **Update-AzureVM** , które implementuje wprowadzone zmiany.

## PARAMETRÓW

### -ACL
Określa obiekt konfiguracji listy kontroli dostępu (ACL), którego to polecenie cmdlet dotyczy punktu końcowego.

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DirectServerReturn
Określa, czy to polecenie cmdlet włącza bezpośrednią zwracanie serwera.
Określ, $True włączyć lub $False do wyłączenia.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
Określa okres czasu bezczynności protokołu TCP (w minutach) dla punktu końcowego.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### -InternalLoadBalancerName
Określa nazwę wewnętrznego modułu równoważenia obciążenia.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerDistribution
Określa algorytm dystrybucji modułu równoważenia obciążenia.
Prawidłowe wartości: 

- sourceIP.
Koligacja dwóch krotek: źródłowy adres IP, docelowy adres IP 
- sourceIPProtocol.
Koligacja trzech krotek: źródłowy adres IP, docelowy adres IP, protokół 
- znaleziono.
Koligacja pięciu krotek: źródłowy adres IP, port źródłowy, docelowy adres IP, port docelowy, protokół 

Wartość domyślna to None.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalPort
Określa lokalny, prywatny, port, którego używa dany punkt końcowy.
Aplikacje w ramach maszyny wirtualnej nasłuchują na tym porcie żądań wejścia usług dla tego punktu końcowego.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę punktu końcowego.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol (protokół)
Określa protokół punktu końcowego.
Prawidłowe wartości: 

- protokoł 
- obsługiwane

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicPort
Określa port publiczny używany przez punkt końcowy.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualIPName
Określa nazwę wirtualnego adresu IP, który jest skojarzony z platformą Azure do punktu końcowego.
Usługa może mieć wiele wirtualnych adresów IP.
Aby utworzyć wirtualne adresy IP, użyj polecenia cmdlet **Add-AzureVirtualIP** .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Umożliwia określenie maszyny wirtualnej, do której należy punkt końcowy.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### System. Object

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureEndpoint](./Add-AzureEndpoint.md)

[Dodaj-AzureVirtualIP](./Add-AzureVirtualIP.md)

[Get-AzureEndpoint](./Get-AzureEndpoint.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureEndpoint](./Remove-AzureEndpoint.md)

[Update-AzureVM](./Update-AzureVM.md)


