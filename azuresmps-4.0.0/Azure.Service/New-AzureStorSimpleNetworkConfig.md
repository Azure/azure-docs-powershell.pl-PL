---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054481"
---
# New-AzureStorSimpleNetworkConfig

## STRESZCZENIe
Przygotowowanie obiektu konfiguracji sieci.

## POLECENIA

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureStorSimpleNetworkConfig** umożliwia przygotowanie obiektu konfiguracji sieci do przechodzenia do polecenia cmdlet **Set-AzureStorSimpleDevice** .
Ustaw parametr *Controller0IPAddress* i parametr *Controller1IPAddress* tylko w interfejsie Data0.
Data0 obsługuje tylko trzy ustawienia: *Controller0IPAddress* , *Controller1IPAdress* i *EnableIscsi*.

## Przykłady

### Przykład 1: Konfigurowanie interfejsu Data0
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

To polecenie umożliwia utworzenie konfiguracji sieci dla interfejsu Data0.
To polecenie określa parametry *Controller0IPv4Address* , *Controller1IPv4Address* i *EnableIscsi* .
To polecenie cmdlet umożliwia skonfigurowanie Data0 tylko dla tych trzech parametrów.

### Przykład 2: Configuren interfejs inny niż Data0
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

To polecenie umożliwia skonfigurowanie interfejsu dane1.

### Przykład 3: modyfikowanie konfiguracji urządzenia
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

Pierwsze polecenie tworzy konfigurację sieci dla interfejsu Data0.
To polecenie określa parametry *Controller0IPv4Address* , *Controller1IPv4Address* i *EnableIscsi* .
Polecenie zapisuje wynik w zmiennej $NetworkConfigData 0.

Drugie polecenie używa polecenia cmdlet **Get-AzureStorSimpleDevice** i podstawowego polecenia **WHERE-Object** w celu uzyskania urządzenia StorSimple online, a następnie zapisuje je w zmiennej $OnlineDevice.

Polecenie ostatnie modyfikuje konfigurację urządzenia o określonym IDENTYFIKATORze urządzenia przy użyciu polecenia cmdlet **Set-AzureStorSimpleDevice** .
W poleceniu jest używany obiekt konfiguracji, który jest tworzony przez bieżące polecenie cmdlet utworzone w pierwszym poleceniu.

## PARAMETRÓW

### -Controller0IPv4Address
Określa adres IPv4 dla kontrolera 0.
Ten parametr można określić tylko dla interfejsu Data0.

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

### -Controller1IPv4Address
Określa adres IPv4 dla kontrolera 1.
Ten parametr można określić tylko dla interfejsu Data0.

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

### -EnableCloud
Wskazuje, czy włączyć interfejs w chmurze.

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

### -EnableIscsi
Wskazuje, czy włączyć funkcję Internet SCSI (ISCSI) dla interfejsu.

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

### -InterfaceAlias
Określa alias interfejsu, dla którego są dostępne ustawienia tego polecenia cmdlet.
Prawidłowe wartości należą do przeData0 do Data5.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Address
Określa adres IPv4 interfejsu.

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

### -IPv4Gateway
Określa adres IPv4 bramy.

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

### -IPv4Netmask
Określa maskę sieci IPv4 dla interfejsu.

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

### -IPv6Gateway
Określa bramę IPv6 dla interfejsu.

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

### -IPv6Prefix
Określa prefiks IPv6 dla interfejsu.

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

### -Profile
Określa Profil platformy Azure.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### NetworkConfig
To polecenie cmdlet zwraca obiekt NetworkConfig, który zawiera następujące właściwości: 

- **IsIscsiEnabled** ( **wartość logiczna** ) 
- **IsCloudEnabled** ( **wartość logiczna** )
- **Controller0IPv4Address** ( **adres_IP** ) 
- **Controller1IPv4Address** ( **adres_IP** ) 
- **IPv6Gateway** ( **adres_IP** ) 
- **IPv4Gateway** ( **adres_IP** ) 
- **IPv4Address** ( **adres_IP** ) 
- **IPv6Prefix** ( **ciąg** )
- **IPv4Netmask** ( **adres_IP** ) 
- **InterfaceAlias** ( **NetInterfaceId** )

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureStorSimpleDevice](./Set-AzureStorSimpleDevice.md)

[Get-AzureStorSimpleDevice](./Get-AzureStorSimpleDevice.md)


