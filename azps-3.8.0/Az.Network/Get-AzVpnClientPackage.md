---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: ec91fecd41138238bc4d89fa81d77bae4730c770
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399400"
---
# Get-AzVpnClientPackage

## SYNOPSIS
Pobiera informacje o pakiecie klienta SIECI VPN.

## SKŁADNIA

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzVpnClientPackage** pobiera informacje o pakietach klienckich VPN dostępnych z bramy sieci wirtualnej.
Pakiety klientów zawierają dane konfiguracji, które umożliwiają klientowi nawiązaniu połączenia VPN z siecią wirtualną platformy Azure; komputery klienckie muszą mieć zainstalowany właściwy pakiet konfiguracji, aby można było nawiązaniu połączenia VPN.
Różne pakiety konfiguracji są dostępne w zależności od wersji systemu Windows na komputerze klienckim (na przykład systemu Windows 7 lub Windows 10) i architektury procesora komputera klienckiego (AMD64 lub x86).
Podczas uruchamiania usługi **Get-AzVpnClientPackage** musisz określić typ architektury.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie informacji o pakiecie klienta VPN architektury procesora
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

To polecenie pobiera informacje o pakietach klienckich SIECI VPN AMD64 przechowywanych w wirtualnej bramie sieciowej o nazwie ContosoVirtualNetworkGateway.
Aby uzyskać informacje na temat pakietów klienta x86, ustaw wartość parametru *ProcessorArchitecture* na x86.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProcessorArchitecture
Określa typ architektury procesora, dla których jest przeznaczony pakiet kliencki.
Prawidłowe wartości to Amd64 i X86.

```yaml
Type: System.String
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
Określa nazwę grupy zasobów, do których przypisano bramę sieci wirtualnej.
Grupy zasobów kategoryzowają elementy, aby uprościć zarządzanie zapasami i ogólną administrację azure.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### System.String

## NOTATKI

## LINKI POKREWNE

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)



