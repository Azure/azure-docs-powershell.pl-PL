---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 3429868b1d603606f64c75ec23505cf63f9ade03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999160"
---
# New-AzWebAppSSLBinding

## SYNOPSIS
Tworzy powiązanie certyfikatu SSL dla aplikacji Azure Web App.

## SKŁADNIA

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

### S4
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzWebAppSSLBinding** tworzy powiązanie certyfikatu SSL (Secure Socket Layer) dla aplikacji Azure Web App.
Polecenie cmdlet tworzy powiązanie PROTOKOŁU SSL na dwa sposoby: 
- Aplikację Sieci Web można powiązać z istniejącym certyfikatem.
- Możesz przekazać nowy certyfikat, a następnie powiązać aplikację Web App z tym nowym certyfikatem.
Niezależnie od tego, której metody używasz, certyfikat i aplikacja sieci Web muszą być skojarzone z tą samą grupą zasobów platformy Azure.
Jeśli masz aplikację sieci Web w grupie Zasobów A i chcesz powiązać ten certyfikat z certyfikatem w grupie Zasobów B, jedynym sposobem jest przekazanie kopii certyfikatu do grupy zasobów A. W przypadku przekazywania nowego certyfikatu pamiętaj o następujących wymaganiach dotyczących certyfikatu AZURE SSL: 
- Certyfikat musi zawierać klucz prywatny. 
- Certyfikat musi mieć format wymiany informacji osobistych (PFX). 
- Nazwa podmiotu certyfikatu musi być dopasowana do domeny używanej do uzyskiwania dostępu do aplikacji sieci Web. 
- Certyfikat musi korzystać z co najmniej 2048-bitowego szyfrowania.

## PRZYKŁADY

### Przykład 1. Powiązanie certyfikatu z aplikacją Web App
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

To polecenie wiąże istniejący certyfikat platformy Azure (certyfikat z kciukiem E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) z aplikacją sieci Web o nazwie ContosoWebApp.

### Przykład 2

Tworzy powiązanie certyfikatu SSL dla aplikacji Azure Web App. (wygenerowane automatycznie)

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## PARAMETERS

### -CertificateFilePath
Określa ścieżkę pliku certyfikatu do przesłania.
Parametr *CertificateFilePath* jest wymagany tylko wtedy, gdy certyfikat nie został jeszcze przekazany do platformy Azure.

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
Określa hasło do odszyfrowywania certyfikatu.

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
Określa nazwę aplikacji Sieci Web.

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
Określa nazwę grupy zasobów, do których jest przypisany certyfikat.
W tym samym *poleceniu nie można* użyć parametru ResourceGroupName ani *parametru WebApp.*

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

### — Slot
Określa nazwę miejsca wdrożenia aplikacji Web App.
Możesz użyć Get-AzWebAppSlot cmdlet, aby uzyskać miejsce.
W aplikacjach wdrożeniowych można etapować i weryfikować aplikacje sieci Web bez dostępu do nich przez Internet.
Zazwyczaj zmiany są wdrażane w witrynie tymczasowej, weryfikowane, a następnie wdrażane w witrynie produkcyjnej (dostępnej w Internecie).

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
Ustaw dla *parametru SSLState* wartość 1, aby włączyć certyfikat, lub ustaw dla *parametru SSLState* wartość 0, aby wyłączyć certyfikat.

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

### - Thumbprint
Określa identyfikator unikatowy certyfikatu.

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

### - WebApp
Określa aplikację sieci Web.
Aby uzyskać aplikację Sieci Web, użyj Get-AzWebApp cmdlet.
Nie można użyć *parametru WebApp* w tym samym poleceniu co parametr *ResourceGroupName* i/lub *nazwa_sieci Web.*

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
W tym samym poleceniu nie można użyć parametru *WebAppName* ani parametru *WebApp.*

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## DANE WYJŚCIOWE

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## NOTATKI

## LINKI POKREWNE

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppslot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


