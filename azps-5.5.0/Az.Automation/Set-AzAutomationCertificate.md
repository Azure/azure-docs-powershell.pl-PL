---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199611"
---
# Set-AzAutomationCertificate

## SYNOPSIS
Modyfikuje konfigurację certyfikatu automatyzacji.

## SKŁADNIA

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzAutomationCertificate** modyfikuje konfigurację certyfikatu w usłudze Azure Automation.

## PRZYKŁADY

### Przykład 1. Modyfikowanie certyfikatu
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

Pierwsze polecenie konwertuje hasło w formacie zwykłego tekstu na bezpieczny ciąg za pomocą ConvertTo-SecureString cmdlet.
Polecenie przechowuje ten obiekt w $Password zmienną.
Drugie polecenie modyfikuje certyfikat o nazwie ContosoCertificate.
To polecenie używa hasła przechowywanego w $Password.
To polecenie określa nazwę konta i ścieżkę do pliku, który jest przesyłany.

## PARAMETERS

### -AutomationAccountName
Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje certyfikat.

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
Określa opis certyfikatu, który zostanie zmodyfikowany przez to polecenie cmdlet.

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
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę certyfikatu, który zostanie zmodyfikowany przez to polecenie cmdlet.

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
Określa ścieżkę do pliku skryptu do przekazania.
Plik może być plikiem cer lub plikiem pfx.

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
Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje certyfikat.

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

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## OUTPUTS

### Microsoft.Azure.Commands.Automation.Model.CertificateInfo

## NOTATKI

## LINKI POKREWNE

[Get-AzAutomationCertificate](./Get-AzAutomationCertificate.md)

[New-AzAutomationCertificate](./New-AzAutomationCertificate.md)

[Remove-AzAutomationCertificate](./Remove-AzAutomationCertificate.md)


