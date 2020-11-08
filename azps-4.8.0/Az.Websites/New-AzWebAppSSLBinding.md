---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222088"
---
# New-AzWebAppSSLBinding

## STRESZCZENIe
Tworzy powiązanie certyfikatu SSL dla aplikacji Azure Web App.

## POLECENIA

### S1
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Stanu
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzWebAppSSLBinding** tworzy powiązanie certyfikatu SSL (Secure Socket Layer) z aplikacją Azure Web App.
Polecenie cmdlet tworzy powiązanie SSL na dwa sposoby: 
- Możesz powiązać aplikację sieci Web z istniejącym certyfikatem.
- Możesz przekazać nowy certyfikat, a następnie powiązać aplikację internetową z tym nowym certyfikatem.
Niezależnie od tego, która metoda jest używana, certyfikat i aplikacja sieci Web muszą być skojarzone z tą samą grupą zasobów platformy Azure.
Jeśli masz aplikację sieci Web w grupie zasobów A i chcesz powiązać tę aplikację sieci Web z certyfikatem w grupie zasobów B, jedynym sposobem na przekazanie kopii certyfikatu do grupy zasobów A. Jeśli przekazujesz nowy certyfikat, pamiętaj o następujących wymaganiach dotyczących certyfikatu SSL usługi Azure: 
- Certyfikat musi zawierać klucz prywatny. 
- Certyfikat musi korzystać z formatu Personal Information Exchange (PFX). 
- Nazwa podmiotu certyfikatu musi odpowiadać domenie używanej do uzyskiwania dostępu do aplikacji sieci Web. 
- Certyfikat musi zawierać co najmniej 2048-bitowe szyfrowanie.

## Przykłady

### Przykład 1: powiązanie certyfikatu z aplikacją sieci Web
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

To polecenie wiąże istniejący certyfikat platformy Azure (certyfikat z E3A38EBA60CAA1C162785A2E1C44A15AD450199C3em odcisku palca) aplikacji internetowej o nazwie ContosoWebApp.

### Przykład 2

Tworzy powiązanie certyfikatu SSL dla aplikacji Azure Web App. (autogenerowana)

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## PARAMETRÓW

### -CertificateFilePath
Określa ścieżkę pliku dla certyfikatu, który ma zostać przekazany.
Parametr *CertificateFilePath* jest wymagany tylko wtedy, gdy certyfikat nie został jeszcze przekazany na platformie Azure.

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Określa hasło odszyfrowywania dla certyfikatu.

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
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
Określa nazwę aplikacji sieci Web.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której przypisano certyfikat.
Nie można użyć parametru *ResourceGroupName* i parametru *aplikacji* w tym samym poleceniu.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Określa nazwę miejsca wdrożenia aplikacji sieci Web.
Możesz użyć polecenia cmdlet Get-AzWebAppSlot, aby uzyskać gniazdo.
Miejsca do wdrożenia umożliwiają przemieszczanie i sprawdzanie aplikacji sieci Web bez możliwości dostępu do aplikacji internetowych.
Zazwyczaj zmiany zostaną wdrożone w witrynie etapowej, poprawność tych zmian, a następnie wdrożone w witrynie produkcja (z ułatwieniami dostępu do Internetu).

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslState
Określa, czy certyfikat jest włączony.
Ustaw parametr *SSLState* na wartość 1, aby włączyć certyfikat, lub ustaw dla *SSLState* wartość 0, aby wyłączyć certyfikat.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Odcisk palca
Określa unikatowy identyfikator certyfikatu.

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aplikacji
Określa aplikację sieci Web.
Aby uzyskać aplikację sieci Web, użyj polecenia cmdlet Get-AzWebApp.
Parametru *aplikacji* nie można używać w tym samym poleceniu, co parametr *ResourceGroupName* i/lub *WebAppName*.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Określa nazwę aplikacji sieci Web, dla której jest tworzone nowe powiązanie SSL.
Nie można użyć parametru *WebAppName* i parametru *aplikacji* w tym samym poleceniu.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. webapps. modele. PSSite

## WYSYŁA

### Microsoft. Azure. Management. Web. MODELES. HostNameSslState

## INFORMACYJN

## LINKI POKREWNE

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


