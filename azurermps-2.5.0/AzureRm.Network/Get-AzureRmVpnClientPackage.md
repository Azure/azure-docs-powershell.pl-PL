---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientpackage
schema: 2.0.0
ms.openlocfilehash: 193353a3e578ec0f644be605498214d5bf4944c6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898329"
---
# Get-AzureRmVpnClientPackage

## STRESZCZENIe
Pobiera informacje o pakiecie klienta sieci VPN.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmVpnClientPackage** pobiera informacje o pakietach klienckich sieci VPN dostępnych w wirtualnej bramie sieci.
Pakiety klienta zawierają dane konfiguracji umożliwiające komputerowi klienckiemu nawiązywania połączenia VPN z siecią wirtualną Azure. Aby nawiązać połączenie z siecią VPN, na komputerach klienckich musi być zainstalowany prawidłowy pakiet konfiguracji.
Różne pakiety konfiguracyjne są dostępne na podstawie wersji systemu Windows komputera klienckiego (na przykład system Windows 7 lub Windows 10) oraz w architekturze procesora komputera klienckiego (AMD64 lub x86).
Typ architektury należy określić podczas uruchamiania **Get-AzureRmVpnClientPackage**.

## Przykłady

### Przykład 1: uzyskiwanie informacji o pakiecie klienta sieci VPN architektura procesora
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

To polecenie pobiera informacje o pakietach klienckich sieci VPN AMD64 przechowywanych w bramy sieci wirtualnej o nazwie ContosoVirtualNetworkGateway.
Aby uzyskać informacje o pakietach klienta x86, ustaw wartość parametru *processorArchitecture* na wartość x86.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProcessorArchitecture
Określa typ architektury procesora, dla którego jest przeznaczony pakiet klienta.
Prawidłowe wartości to amd64 i x86.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.

Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Określa nazwę bramy sieci wirtualnej, w której są przechowywane informacje o pakiecie klienta.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Ciąg
Parametr "ResourceGroupName" akceptuje wartość typu "String" z procesu

### Ciąg
Parametr "VirtualNetworkGatewayName" akceptuje wartość typu "String" z procesu

## WYSYŁA

###  
Funkcja **Get-AzureRmVpnClientPackage** zwraca wystąpienia obiektu System. String.

## INFORMACYJN

## LINKI POKREWNE

[Zmienianie rozmiaru — AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


