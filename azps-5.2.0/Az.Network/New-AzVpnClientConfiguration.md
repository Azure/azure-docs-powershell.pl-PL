---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362672"
---
# New-AzVpnClientConfiguration

## STRESZCZENIe
To polecenie umożliwia użytkownikom tworzenie pakietu profilu sieci VPN na podstawie wstępnie skonfigurowanych ustawień sieci VPN w bramie sieci VPN, oprócz dodatkowych ustawień, które mogą być potrzebne użytkownikom do skonfigurowania (na przykład niektóre certyfikaty główne).

## POLECENIA

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Dzięki temu użytkownicy mogą utworzyć pakiet profilów sieci VPN na podstawie wstępnie skonfigurowanych ustawień sieci VPN w bramie sieci VPN, oprócz dodatkowych ustawień, które użytkownicy mogą potrzebować skonfigurować, na przykład niektóre certyfikaty główne.

## Przykłady

### Przykład 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

To polecenie cmdlet służy do tworzenia pliku zip profilu klienta VPN dla "ContosoVirtualNetworkGateway" w przystawce "ContosoResourceGroup". Profil jest generowany dla wstępnie skonfigurowanego serwera RADIUS, który jest skonfigurowany do używania metody uwierzytelniania "EAPTLS" z plikiem certyfikatu VpnProfileRadiusCert.

## PARAMETRÓW

### -Metodę uwierzytelniania
Metoda uwierzytelniania może pobierać wartości EAPMSCHAPv2 lub EAPTLS. Gdy EAPMSCHAPv2 jest określony, polecenie cmdlet generuje Instalator konfiguracji klienta dla uwierzytelniania nazwy użytkownika i hasła, który używa protokołu uwierzytelniania EAP-MSCHAPv2. Jeśli EAPTLS jest określony, polecenie cmdlet generuje instalatora konfiguracji klienta w celu uwierzytelnienia przy użyciu protokołu EAP-TLS. Opcja "EapTls" może być używana zarówno do uwierzytelniania certyfikatu opartego na usłudze RADIUS, jak i uwierzytelniania certyfikacji przeprowadzanych przez wirtualną bramę sieciową przez przekazanie zaufanego certyfikatu głównego. Polecenie cmdlet automatycznie wykrywa, co jest skonfigurowane.

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
Lista ścieżek certyfikatów głównych klienta

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Name (nazwa)
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
ProcessorArchitecture

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
Ścieżka głównego certyfikatu serwera usługi RADIUS. Jest to obowiązkowy parametr, który należy określić, gdy jest używana funkcja EAP-TLS z uwierzytelnianiem usługi RADIUS. Jest to pełna nazwa ścieżki pliku CER zawierającego główny certyfikat RADIUS używany przez klienta do sprawdzania poprawności serwera RADIUS podczas uwierzytelniania.

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### System. String []

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSVpnProfile

## INFORMACYJN

## LINKI POKREWNE

[Get-AzVpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
