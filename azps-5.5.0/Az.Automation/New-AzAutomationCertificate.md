---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: c80eb16f840fb6d590c139a6ec4b30d73584b741
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201082"
---
# New-AzAutomationCertificate

## SYNOPSIS
Tworzy certyfikat automatyzacji.

## SKŁADNIA

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzAutomationCertificate** tworzy certyfikat w usłudze Azure Automation.
Podaj ścieżkę do pliku certyfikatu, który chcesz przekazać.

## PRZYKŁADY

### Przykład 1. Tworzenie nowego certyfikatu
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

Pierwsze polecenie konwertuje hasło w formacie zwykłego tekstu na bezpieczny ciąg za pomocą ConvertTo-SecureString cmdlet.
Polecenie przechowuje ten obiekt w $Password zmienną.
Drugie polecenie tworzy certyfikat o nazwie ContosoCertificate.
To polecenie używa hasła przechowywanego w $Password.
To polecenie określa nazwę konta i ścieżkę do pliku, który jest przesyłany.

## PARAMETERS

### -AutomationAccountName
Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet przechowuje certyfikat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — Opis
Określa opis certyfikatu.

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

### -Exportable
Określa, czy certyfikat można wyeksportować.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę certyfikatu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Hasło
Określa hasło pliku certyfikatu.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Ścieżka
Określa ścieżkę do pliku skryptu, który jest przesyłany przez to polecenie cmdlet.
Plik może być plikiem cer lub pfx.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy certyfikat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### System.Security.SecureString

### System.Management.Automation.SwitchParameters

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Automation.Model.CertificateInfo

## NOTATKI

To polecenie powinno być uruchamiane na komputerze, na których jesteś administratorem, oraz w sesji programu PowerShell o podwyższonym poziomie uprawnień. zanim certyfikat zostanie przekazany, to polecenie cmdlet użyje lokalnego magazynu X.509 do pobrania kciuka i klucza, a jeśli to polecenie cmdlet zostanie uruchomione poza sesją programu PowerShell o podwyższonym poziomie uprawnień, zostanie wyświetlony błąd "Odmowa dostępu".

## LINKI POKREWNE

[Get-AzAutomationCertificate](./Get-AzAutomationCertificate.md)

[Remove-AzAutomationCertificate](./Remove-AzAutomationCertificate.md)

[Set-AzAutomationCertificate](./Set-AzAutomationCertificate.md)


