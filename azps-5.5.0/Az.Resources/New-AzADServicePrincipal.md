---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: e7c77dc4daf38634e7661f4579dd5bbcc81d0443
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242562"
---
# New-AzADServicePrincipal

## SYNOPSIS
Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.

## SKŁADNIA

### SimpleParameterSet (domyślne)

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithoutCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ApplicationWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithoutCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DisplayNameWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyPlainParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisplayNameWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithPasswordCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyPlainParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationObjectWithKeyCredentialParameterSet

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS

Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory. Domyślny zestaw parametrów używa wartości domyślnych dla parametrów, jeśli nie zostały podane. Aby uzyskać więcej informacji na temat wartości domyślnych, zobacz opis każdego parametru. To polecenie cmdlet umożliwia przypisanie roli do podmiotu zabezpieczeń usługi za pomocą **parametrów Rola** **i** Zakres. Jeśli oba te czynniki zostaną pominięte, rola współautora zostanie przypisana do podmiotu zabezpieczeń usługi. Wartości domyślne parametrów **rola** i zakres są  **wartościami współautorów** dla bieżącej subskrypcji. Polecenie cmdlet tworzy aplikację i ustawia jej właściwości, jeśli nie podano właściwości ApplicationId. Aby zaktualizować parametry specyficzne dla aplikacji, użyj polecenia cmdlet [Update-AzADApplication.](./update-azadapplication.md)

> [!WARNING]
> Po utworzeniu podmiotu zabezpieczeń usługi za pomocą **polecenia New-AzADServicePrincipal** dane wyjściowe zawierają poświadczenia, które należy chronić. Rozważ użycie tożsamości [zarządzanych,](/azure/active-directory/managed-identities-azure-resources/overview) aby uniknąć konieczności używania poświadczeń.
>
> Domyślnie **new-AzADServicePrincipal** przypisuje rolę [](/azure/role-based-access-control/built-in-roles#contributor) współautora podmiotowi usługi w zakresie subskrypcji. Aby zmniejszyć ryzyko wystąpienia naruszonego podmiotu zabezpieczeń usługi, przypisz bardziej konkretną rolę i zawęzij zakres do zasobu lub grupy zasobów. Zobacz [Kroki, aby dodać przypisanie roli,](/azure/role-based-access-control/role-assignments-steps) aby uzyskać więcej informacji.

## PRZYKŁADY

### Przykład 1. Tworzenie podmiotu zabezpieczeń prostej usługi AD

W poniższym przykładzie jest domyślną jednostką zabezpieczeń usługi AD dla parametrów, które nie zostały określone. Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu zabezpieczeń usługi jest tworzona aplikacja. Ponieważ nie podano żadnych wartości dla **roli** lub **zakresu,** do utworzonego podmiotu zabezpieczeń usługi jest przypisywana rola **współautora** dla bieżącej subskrypcji.

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### Przykład 2. Tworzenie podmiotu zabezpieczeń prostej usługi AD z określoną rolą i zakresem domyślnym

W poniższym przykładzie jest domyślną jednostką zabezpieczeń usługi AD dla parametrów, które nie zostały określone. Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu zabezpieczeń usługi jest tworzona aplikacja. Podmiot zabezpieczeń usługi jest tworzony z **uprawnieniami czytnika** dla bieżącej subskrypcji, ponieważ dla **parametru Zakres** nie jest podano żadnej wartości.

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### Przykład 3. Proste tworzenie podmiotu zabezpieczeń usługi AD z określonym zakresem i rolą domyślną

W poniższym przykładzie jest domyślną jednostką zabezpieczeń usługi AD dla parametrów, które nie zostały określone. Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu zabezpieczeń usługi jest tworzona aplikacja. Podmiot zabezpieczeń usługi jest tworzony z uprawnieniami **współautora** dla podanego zakresu grupy zasobów, ponieważ dla parametru Rola nie jest podano **żadnej** wartości.

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Przykład 4. Tworzenie podmiotu zabezpieczeń prostej usługi AD z określonym zakresem i rolą

W poniższym przykładzie jest domyślną jednostką zabezpieczeń usługi AD dla parametrów, które nie zostały określone. Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu zabezpieczeń usługi jest tworzona aplikacja. Podmiot zabezpieczeń usługi jest tworzony przy użyciu uprawnień **czytnika** dla podanego zakresu grupy zasobów.

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### Przykład 5. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu identyfikatora aplikacji z przypisaniem roli

Poniższy przykład tworzy nowy podmiot zabezpieczeń usługi AD dla aplikacji o identyfikatorze aplikacji "000000000-0000-0000-0000-0000000000000". Ponieważ nie podano żadnych wartości dla **roli** lub **zakresu,** do utworzonego podmiotu zabezpieczeń usługi jest przypisywana rola **współautora** dla bieżącej subskrypcji.

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### Przykład 6. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu funkcji rurowych

Poniższy przykład pobiera aplikację z identyfikatorem obiektu "3ede3c26-b443-4e0b-9efc-b05e68338dc3" za pomocą polecenia cmdlet [Get-AzADApplication.](./get-azadapplication.md) Wyniki są potokowe do polecenia cmdlet w celu utworzenia nowego podmiotu zabezpieczeń usługi `New-AzADServicePrincipal` AD dla tej aplikacji.

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### Przykład 7. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu poświadczeń displayname i hasła

Poniższy przykład tworzy nową aplikację o nazwie **ServicePrincipalName** i hasłem **nazwy StrongPassworld!23.** Na podstawie utworzonej aplikacji jest tworzony podmiot zabezpieczeń usługi. Data rozpoczęcia i data zakończenia zostaną dodane do poświadczeń hasła.

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### Przykład 8. Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu poświadczeń DisplayName i zwykłego klucza

W poniższym przykładzie jest podmiot tworzący nową aplikację o nazwie **ServicePrincipalName** i **$cert.** Podmiot zabezpieczeń usługi jest tworzony na podstawie utworzonej aplikacji. Data zakończenia zostanie dodana do poświadczeń klucza.

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## PARAMETERS

### -ApplicationId

Unikatowy identyfikator aplikacji dla podmiotu zabezpieczeń usługi w dzierżawie. Po utworzeniu tej właściwości nie można jej zmienić. Jeśli nie określono identyfikatora aplikacji dla istniejącej aplikacji, zostanie utworzona aplikacja.

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationObject

Obiekt reprezentujący aplikację, dla której jest tworzony podmiot zabezpieczeń usługi.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CertValue

Wartość asymetrycznego typu poświadczeń. Reprezentuje certyfikat zakodowany w bazie danych Base64.

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
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

### — DisplayName

Przyjazna nazwa podmiotu zabezpieczeń usługi. Jeśli nazwa wyświetlana nie zostanie podany, ta wartość będzie domyślnie wyświetlana w programie **azure-powershell-MM-dd-yyyy-HH-mm-ss,** gdzie sufiks jest czasem tworzenia aplikacji.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate

Data zakończenia użytkowania poświadczeń. Domyślna wartość daty końcowej to rok od dnia dzisiejszego.
W przypadku poświadczeń typu asymetrycznego musi to być ustawione na datę ważności certyfikatu X509 lub wcześniejszą.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyCredential

Zbiór poświadczeń klucza skojarzonych z aplikacją.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - PasswordCredential

Zbiór poświadczeń hasła skojarzonych z aplikacją.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - Rola

Rola podmiotu zabezpieczeń usługi w zakresie. Jeśli nie podano żadnej wartości, **rola będzie domyślnie** pełnić rolę **współautora.**

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zakres

Zakres uprawnień podmiotu zabezpieczeń usługi. Jeśli nie podano żadnej wartości, **zakres jest** domyślnie domyślny dla bieżącej subskrypcji.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SkipAssignment

Jeśli ta opcja jest ustawiona, pomiń tworzenie domyślnego przydziału ról dla podmiotu zabezpieczeń usługi.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - StartDate

Data rozpoczęcia użytkowania poświadczeń. Domyślną wartością daty rozpoczęcia jest dzisiaj. W przypadku poświadczeń typu asymetrycznego musi to być wartość ustawiona na datę ważności certyfikatu X509 lub późniejszą.

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)
## DANE WEJŚCIOWE

### System.Guid

### System.String

### Microsoft.Azure.Commands.ActiveDirectory.PSADApplication

### Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]

### Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]

### System.DateTime

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper

## NOTATKI

Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie

## LINKI POKREWNE

[Remove-AzadServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzadServicePrincipal](./Get-AzADServicePrincipal.md)

[New-AzadApplication](./New-AzADApplication.md)

[Remove-AzadApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[New-AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)