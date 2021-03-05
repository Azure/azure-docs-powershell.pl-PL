---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: e5dd9da25bfa2c27bd605dc80b04f8e47fb7f95b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964122"
---
# New-AzVpnClientConfiguration

## SYNOPSIS
To polecenie umożliwia użytkownikom utworzenie pakietu profilu vpn na podstawie wstępnie skonfigurowanych ustawień sieci VPN w bramie VPN, a także niektórych dodatkowych ustawień, które użytkownicy mogą konfigurować na przykład na niektórych certyfikatach głównych.

## SKŁADNIA

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
umożliwia to użytkownikom utworzenie pakietu profilu VPN na podstawie wstępnie skonfigurowanych ustawień sieci VPN w bramie VPN, a także niektórych dodatkowych ustawień, które użytkownicy mogą konfigurować na przykład na niektórych certyfikatach głównych.

## PRZYKŁADY

### Przykład 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

To polecenie cmdlet służy do tworzenia pliku zip profilu klienta VPN dla pliku "ContosoVirtualNetworkGateway" w grupie zasobów "ContosoResourceGroup". Profil jest generowany dla wstępnie skonfigurowanego serwera promieni, który jest skonfigurowany do używania metody uwierzytelniania "EAPTLS" z plikiem certyfikatu VpnProfileRadiusCert.

## PARAMETERS

### -AuthenticationMethod
Metoda uwierzytelniania może przyjmować wartości EAPMSCHAPv2 lub EAPTLS. Gdy zostanie określony protokół EAPMSCHAPv2, polecenie cmdlet generuje instalator konfiguracji klienta dla nazwy użytkownika/uwierzytelnianie hasłem korzystającego z protokołu EAP-MSCHAPv2 uwierzytelniania. Jeśli zostanie określony protokół EAPTLS, polecenie cmdlet wygeneruje instalatora konfiguracji klienta dla uwierzytelniania certyfikatów, który korzysta z protokołu EAP-TLS. Opcja "EapTls" może być używana zarówno w przypadku uwierzytelniania certyfikatów opartego na funkcji RADIUS, jak i uwierzytelniania certyfikacji wykonywanego przez wirtualną bramę sieciową przez przekazanie zaufanego katalogu głównego. Polecenie cmdlet automatycznie wykrywa skonfigurowane ustawienia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
Lista głównych ścieżek certyfikatów klienta

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### — Nazwa
Nazwa zasobu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProcessorArchitecture
ProcesorArchitecture

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusRootCertificateFile
Ścieżka certyfikatu głównego serwera Radius. Jest to obowiązkowy parametr, który należy określić podczas korzystania z protokołu EAP-TLS z uwierzytelnianiem RADIUS. Jest to nazwa pełnej ścieżki pliku cer zawierającego certyfikat główny RADIUS, który jest używany przez klienta do sprawdzania poprawności serwera RADIUS podczas uwierzytelniania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### System.String[]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSVpnProfile

## NOTATKI

## LINKI POKREWNE

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
