---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054789"
---
# Set-AzureRoute

## STRESZCZENIe
Tworzy trasę w tabeli tras.

## POLECENIA

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRoute** tworzy trasę w tabeli tras.
Nowa trasa zacznie obowiązywać prawie natychmiast na maszynach wirtualnych skojarzonych z tabelą tras.

## Przykłady

### Przykład 1: Dodawanie urządzenia wirtualnego — Następna przeskokowa trasa
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

To polecenie tworzy tabelę tras o nazwie ApplianceRouteTable w określonej lokalizacji.
Polecenie przekazuje tę tabelę routingu do bieżącego polecenia cmdlet.
Bieżące polecenie cmdlet umożliwia dodanie trasy o nazwie ApplianceRoute03, która jest typu VirtualAppliance następnego przeskoku.
Polecenie określa adres IP następnego przeskoku oraz prefiks adresu dla tej trasy.

### Przykład 2: Dodawanie internetowego trasy przeskoków internetowych
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

To polecenie pobiera tabelę tras o nazwie ApplianceRouteTable.
Polecenie przekazuje tę tabelę routingu do bieżącego polecenia cmdlet.
Bieżące polecenie cmdlet umożliwia dodanie trasy o nazwie InternetRoute, która jest internetowym typem następnego przeskoku.
Polecenie Określa prefiks adresu dla trasy.

## PARAMETRÓW

### -AddressPrefix
Określa prefiks adresu dla nowej trasy.

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

### -NextHopIpAddress
Określa adres IP urządzenia, które jest następnym skokiem dla ruchu sieciowego korzystającego z tej trasy.
Tę wartość należy określić tylko wtedy, gdy dla parametru *NextHopType* określono wartość VirtualAppliance.

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

### -NextHopType
Określa typ następnego przeskoku dla ruchu, który używa tej trasy.
Prawidłowe wartości: 

- VPNGateway
- VNETLocal
- Internetowe
- VirtualAppliance
- Puste

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

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet. Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### -RouteName
Określa nazwę nowej trasy, którą dodaje polecenie cmdlet.

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

### -Routeing
Określa tabelę tras, z którą to polecenie cmdlet dodaje nową trasę.

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

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

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzureRoute](./Remove-AzureRoute.md)


