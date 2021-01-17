---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490430"
---
# New-AzADServicePrincipal

## STRESZCZENIe
Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.

## POLECENIA

### SimpleParameterSet (domyślny)

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

## Opis

Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory. W domyślnym ustawieniu parametrów są używane wartości domyślne parametrów, o ile nie zostały one podane. Aby uzyskać więcej informacji na temat wartości domyślnych, zobacz opisy poszczególnych parametrów. To polecenie cmdlet umożliwia przypisanie roli do podmiotu zabezpieczeń przy użyciu parametrów **rola** i **zakres** . Jeśli oba zostaną pominięte, rola współautora zostanie przypisana do podmiotu usługi. Domyślne wartości parametrów **rola** i **zakres** są **współautorami** dla bieżącej subskrypcji. Polecenie cmdlet tworzy aplikację i ustawia jej właściwości, jeśli nie jest podany identyfikator aplikacji. Aby zaktualizować parametry specyficzne dla aplikacji, użyj polecenia cmdlet [Update-AzADApplication](./update-azadapplication.md) .

> [!WARNING]
> Podczas tworzenia podmiotu usługi za pomocą polecenia **New-AzADServicePrincipal** dane wyjściowe będą zawierały poświadczenia, które należy chronić. Upewnij się, że nie są uwzględniane te poświadczenia w kodzie, lub sprawdź poświadczenia w kontroli źródła. Alternatywne rozwiązanie polega na użyciu [tożsamości zarządzanych](/azure/active-directory/managed-identities-azure-resources/overview) , aby uniknąć konieczności korzystania z poświadczeń.
>
> Domyślnie polecenie **New-AzADServicePrincipal** przypisuje rolę [współautora](/azure/role-based-access-control/built-in-roles#contributor) głównemu usługi w zakresie subskrypcji. Aby zmniejszyć ryzyko naruszenia zabezpieczeń usługi, należy przypisać bardziej określoną rolę i zawęzić jej zakres do zasobu lub grupy zasobów. Aby uzyskać więcej informacji [, zobacz instrukcje dodawania zadania roli](/azure/role-based-access-control/role-assignments-steps) .

## Przykłady

### Przykład 1: proste tworzenie podmiotu zabezpieczeń usługi reklamy

W poniższym przykładzie jest tworzony podmiot zabezpieczeń usługi AD, który używa wartości domyślnych dla parametrów, które nie zostały określone. Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu usługi jest tworzona aplikacja. Ponieważ dla **roli** lub **zakresu** nie są podane żadne wartości, utworzonym podmiotowi zabezpieczeń usługi jest przypisywana rola **współautora** dla bieżącej subskrypcji.

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

### Przykład 2: proste tworzenie podmiotów głównych usługi REKLAMowej z określoną rolą i zakresem domyślnym

W poniższym przykładzie następuje utworzenie podmiotu zabezpieczeń usługi AD przy użyciu wartości domyślnych dla parametrów, które nie zostały określone. Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu usługi jest tworzona aplikacja. Podmiot zabezpieczeń usługi jest tworzony z uprawnieniami **czytelnika** dla bieżącej subskrypcji, ponieważ parametr **zakres** nie ma wartości.

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

### Przykład 3: proste tworzenie głównych usług REKLAMowych z określonym zakresem i rolą domyślną

W poniższym przykładzie następuje utworzenie podmiotu zabezpieczeń usługi AD przy użyciu wartości domyślnych dla parametrów, które nie zostały określone. Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu usługi jest tworzona aplikacja. Podmiot zabezpieczeń usługi jest tworzony z uprawnieniami **współautorów** dla podanego zakresu grupy zasobów, ponieważ nie jest podana wartość parametru **role** .

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

### Przykład 4: proste tworzenie głównych usług REKLAMowych z określonym zakresem i rolą

W poniższym przykładzie następuje utworzenie podmiotu zabezpieczeń usługi AD przy użyciu wartości domyślnych dla parametrów, które nie zostały określone. Ponieważ identyfikator aplikacji nie jest podany, dla podmiotu usługi jest tworzona aplikacja. Podmiot zabezpieczeń usługi jest tworzony z uprawnieniami **czytelnika** dla podanego zakresu grupy zasobów.

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

### Przykład 5: Tworzenie nowego podmiotu usługi reklamy przy użyciu identyfikatora aplikacji z przypisaniem roli

W poniższym przykładzie jest tworzony nowy podmiot zabezpieczeń usługi reklamy dla aplikacji z IDENTYFIKATORem aplikacji ' 00000000-0000-0000-0000-000000000000 '. Ponieważ dla **roli** lub **zakresu** nie są podane żadne wartości, utworzonym podmiotowi zabezpieczeń usługi jest przypisywana rola **współautora** dla bieżącej subskrypcji.

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

### Przykład 6: Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu połączeń rurowych

Poniższy przykład pobiera aplikację z IDENTYFIKATORem obiektu 3ede3c26-B443-4e0b-9efc-b05e68338dc3 ' przy użyciu polecenia cmdlet [Get-AzADApplication](./get-azadapplication.md) . Wyniki są potoku do `New-AzADServicePrincipal` polecenia cmdlet w celu utworzenia nowego podmiotu zabezpieczeń usługi AD dla tej aplikacji.

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### Przykład 7: Tworzenie nowego podmiotu zabezpieczeń usługi AD przy użyciu poświadczenia DisplayName i hasła

W poniższym przykładzie jest tworzona nowa aplikacja z nazwą **ServicePrincipalName** i hasłem **StrongPassworld! 23**. Tworzy on nazwę główną usługi na podstawie utworzonej aplikacji. Data rozpoczęcia i Data zakończenia zostaną dodane do poświadczenia hasła.

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

### Przykład 8: Tworzenie nowego podmiotu usługi reklamy przy użyciu poświadczenia DisplayName i zwykłego klucza

W poniższym przykładzie jest tworzona nowa aplikacja z nazwą **ServicePrincipalName** i certyfikatem **$CERT**. Tworzy on nazwę główną usługi na podstawie utworzonej aplikacji. Data zakończenia zostanie dodana do poświadczenia klucza.

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

## PARAMETRÓW

### -Identyfikator aplikacji

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

### -Applicationobject

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

Wartość typu poświadczeń asymetrycznych. Reprezentuje certyfikat kodowany algorytmem Base64.

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

### -DisplayName

Przyjazna nazwa podmiotu zabezpieczeń usługi. Jeśli nie podano nazwy wyświetlanej, ta wartość będzie domyślnie równa **platformie Azure-PowerShell-mm-dd-rrrr-hh-mm-SS** , gdzie sufiks jest momentem utworzenia aplikacji.

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

Efektywna Data zakończenia użycia poświadczeń. Domyślną wartością daty zakończenia jest rok od dzisiaj.
W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.

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

### -Poświadczenia

Kolekcja kluczowych poświadczeń skojarzonych z aplikacją.

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

### -PasswordCredential

Kolekcja poświadczeń haseł skojarzonych z aplikacją.

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

### -Rola

Rola podmiotu zabezpieczeń usługi w zakresie. Jeśli nie podano żadnej wartości, rola jest domyślnie ustawiana przez **rolę** **współautora** .

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

### -Zakres

Zakres, dla którego główna usługa ma uprawnienia. Jeśli nie podano żadnej wartości, to **zakresem** domyślnym jest bieżący abonament.

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

### -SkipAssignment

Jeśli jest ustawiona, Pomiń tworzenie domyślnego zadania roli dla podmiotu usługi.

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

### -DataRozpoczęcia

Efektywna Data rozpoczęcia użycia poświadczeń. Domyślna wartość daty rozpoczęcia przypada dzisiaj. W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).
## WEJŚCIOWE

### System. GUID

### System. String

### Microsoft. Azure. Commands. pozycji. PSADApplication

### Microsoft. Azure. Commands. pozycji. PSADPasswordCredential []

### Microsoft. Azure. Commands. pozycji. PSADKeyCredential []

### System. DateTime

## WYSYŁA

### Microsoft. Azure. Commands. pozycji. PSADServicePrincipal

### Microsoft. Azure. Commands. resources. models. Authorization. PSADServicePrincipalWrapper

## INFORMACYJN

Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie

## LINKI POKREWNE

[Remove-AzADServicePrincipal](./Remove-AzADServicePrincipal.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)

[Nowe — AzADApplication](./New-AzADApplication.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[Nowe — AzADSpCredential](./New-AzADSpCredential.md)

[Remove-AzADSpCredential](./Remove-AzADSpCredential.md)