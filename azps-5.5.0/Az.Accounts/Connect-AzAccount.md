---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: e997013eb5646ca0f22904dd6fc68cf09a3ba228
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178178"
---
# Connect-AzAccount

## SYNOPSIS
Połącz się z platformą Azure przy użyciu uwierzytelnionego konta w celu używania z poleceniami cmdlet z modułów programu Az PowerShell.

## SKŁADNIA

### UserWithSubscriptionId (domyślne)
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-UseDeviceAuthentication] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UserWithCredential
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ServicePrincipalCertificateWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-MaxContextPopulation <Int32>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccessTokenWithSubscriptionId
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-MaxContextPopulation <Int32>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ManagedServiceLogin
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-MaxContextPopulation <Int32>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS

Polecenie cmdlet łączy się z platformą Azure za pomocą uwierzytelnionego konta w celu używania z `Connect-AzAccount` poleceniami cmdlet z modułów programu Az PowerShell. Tego uwierzytelnionego konta można używać tylko w przypadku żądań usługi Azure Resource Manager. Aby dodać uwierzytelnione konto do użycia z zarządzaniem usługami, użyj `Add-AzureAccount` polecenia cmdlet z modułu programu Azure PowerShell. Jeśli bieżący użytkownik nie znajdzie kontekstu, jego lista kontekstowa zostanie wypełniona kontekstem dla każdej z pierwszych 25 subskrypcji.
Listę kontekstów utworzonych dla użytkownika można znaleźć, uruchamiając `Get-AzContext -ListAvailable` program. Aby pominąć tę populację kontekstu, określ **parametr przełącznika SkipContextPopulation.** Po wykonaniu tego polecenia cmdlet możesz odłączyć się od konta platformy Azure przy `Disconnect-AzAccount` użyciu.

## PRZYKŁADY

### Przykład 1. Nawiązywanie połączenia z kontem platformy Azure

W tym przykładzie jest nawiąże połączenie z kontem platformy Azure. Musisz podać poświadczenia konta Microsoft lub identyfikatora organizacyjnego. Jeśli dla twoich poświadczeń włączono uwierzytelnianie wieloskładnikowe, musisz zalogować się przy użyciu opcji interakcyjnej lub użyć uwierzytelniania podmiotu zabezpieczeń usługi.

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 2. (tylko program Windows PowerShell 5.1) Łączenie się z platformą Azure przy użyciu poświadczeń identyfikatora organizacyjnego

Ten scenariusz działa tylko w programie Windows PowerShell 5.1. Pierwsze polecenie wyświetla monit o poświadczenia użytkownika i zapisuje je w `$Credential` zmiennej. Drugie polecenie łączy się z kontem platformy Azure przy użyciu poświadczeń przechowywanych w `$Credential` usłudze. To konto jest uwierzytelniane na platformie Azure przy użyciu poświadczeń identyfikatora organizacyjnego.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 3. Nawiązywanie połączenia z platformą Azure przy użyciu konta podmiotu zabezpieczeń usługi

Pierwsze polecenie monituje o poświadczenia podmiotu zabezpieczeń usługi i przechowuje je w `$Credential` zmiennej. Po wyświetleniu monitu wprowadź identyfikator aplikacji dla nazwy użytkownika i podmiotu zabezpieczeń usługi jako hasło. Drugie polecenie łączy określoną dzierżawę platformy Azure przy użyciu przechowywanych w zmiennej poświadczeń podmiotu zabezpieczeń `$Credential` usługi. Parametr **przełącznika ServicePrincipal** wskazuje, że konto uwierzytelnia się jako podmiot zabezpieczeń usługi.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 4. Używanie interakcyjnego logowania w celu nawiązania połączenia z konkretną dzierżawą i subskrypcją

W tym przykładzie jest nawiąże połączenie z kontem platformy Azure z określoną dzierżawą i subskrypcją.

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 5. Nawiązywanie połączenia przy użyciu tożsamości usługi zarządzanej

W tym przykładzie jest nawiązuje połączenie przy użyciu tożsamości usługi zarządzanej (MSI, Managed Service Identity) środowiska hosta. Na przykład możesz zalogować się do platformy Azure z maszyny wirtualnej z przypisanym msi.

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 6. Łączenie przy użyciu logowania tożsamości usługi zarządzanej i identyfikatora klienta

W tym przykładzie powiążesz się przy użyciu tożsamości usługi zarządzanej **myUserAssignedIdentity.** Dodaje tożsamość przypisaną do użytkownika do maszyny wirtualnej, a następnie łączy się przy użyciu wartości ClientId przypisanej tożsamości użytkownika. Aby uzyskać więcej informacji, zobacz Konfigurowanie tożsamości [zarządzanych dla zasobów platformy Azure na maszyny wirtualnej platformy Azure.](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm)

```powershell
$identity = Get-AzUserAssignedIdentity -ResourceGroupName 'myResourceGroup' -Name 'myUserAssignedIdentity'
Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the virtual machine
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 7. Nawiązywanie połączenia przy użyciu certyfikatów

W tym przykładzie powiążesz się z kontem platformy Azure przy użyciu uwierzytelniania głównego usługi opartej na certyfikatach.
Podmiot zabezpieczeń usługi używany do uwierzytelniania musi zostać utworzony przy użyciu określonego certyfikatu. Aby uzyskać więcej informacji na temat tworzenia certyfikatów z podpisem własnym i przypisywania do nich uprawnień, zobacz Używanie programu Azure PowerShell do tworzenia podmiotu zabezpieczeń usługi [z certyfikatem.](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)

```powershell
$Thumbprint = '0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV'
$TenantId = '4cd76576-b611-43d0-8f2b-adcb139531bf'
$ApplicationId = '3794a65a-e4e4-493d-ac1d-f04308d712dd'
Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal
```

```Output
Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

## PARAMETERS

### - AccessToken

Określa token dostępu.

> [!CAUTION]
> Tokeny dostępu są typem poświadczeń. Należy podjąć odpowiednie środki ostrożności, aby zachować ich poufność. Limit czasu tokenów programu Access może również uniemożliwiać ukończenie długo wykonywanych zadań.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId

Identyfikator konta tokenu dostępu w zestawie parametrów **AccessToken.** Identyfikator konta dla usługi zarządzanej w zestawie **parametrów ManagedService.** Może być identyfikatorem zarządzanego zasobu usługi lub skojarzonym identyfikatorem klienta.
Aby użyć tożsamości przypisanej przez system, pozostaw to pole puste.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId

Identyfikator aplikacji podmiotu zabezpieczeń usługi.

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateThumbprint

Certificate Hash lub Thumbprint.

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContextName

Nazwa domyślnego kontekstu platformy Azure dla tego logowania. Aby uzyskać więcej informacji o kontekstach platformy Azure, zobacz obiekty kontekstowe [programu Azure PowerShell.](/powershell/azure/context-persistence)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - Credential

Określa obiekt **PSCredential.** Aby uzyskać więcej informacji na **temat obiektu PSCredential,** wpisz `Get-Help Get-Credential` tekst . Obiekt **PSCredential** udostępnia identyfikator użytkownika i hasło dla poświadczeń identyfikatora organizacyjnego lub identyfikator aplikacji i klucz tajny dla poświadczeń podmiotu zabezpieczeń usługi.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
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

### — Środowisko

Środowisko zawierające konto platformy Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Wymuszanie

Zastąp istniejący kontekst bez monitowania o tę samą nazwę.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken

AccessToken for Graph Service.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Tożsamość

Zaloguj się przy użyciu tożsamości usługi zarządzanej.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultAccessToken

AccessToken for KeyVault Service.

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceHostName

Przestarzałe. Aby użyć niestandardowego punktu końcowego MSI, ustaw wartość zmiennej MSI_ENDPOINT, na przykład " http://localhost:50342/oauth2/token ". Nazwa hosta usługi zarządzanej.

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServicePort

Przestarzałe. Aby użyć niestandardowego punktu końcowego MSI, ustaw wartość zmiennej MSI_ENDPOINT, na przykład " http://localhost:50342/oauth2/token ". Numer portu usługi zarządzanej.

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedServiceSecret

Przestarzałe. Aby użyć niestandardowego msi tajnego, ustaw zmienną środowiskową MSI_SECRET. Token dla logowania usługi zarządzanej.

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxContextPopulation

Maksymalny numer subskrypcji, aby wypełnić konteksty po zalogowaniu się. Wartość domyślna to 25. Aby wypełnić wszystkie subskrypcje kontekstami, ustaw wartość -1.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zakres

Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePrincipal

Wskazuje, że to konto uwierzytelnia się, podając poświadczenia podmiotu zabezpieczeń usługi.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - SkipContextPopulation

Pomija populację kontekstu, jeśli nie zostaną znalezione żadne konteksty.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipValidation

Pomiń sprawdzanie poprawności tokenu dostępu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Subskrypcja

Nazwa lub identyfikator subskrypcji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Dzierżawa

Opcjonalna nazwa dzierżawy lub identyfikator.

> [!NOTE]
> Ze względu na ograniczenia bieżącego interfejsu API podczas łączenia się z kontem między firmami (B2B) należy użyć identyfikatora dzierżawy zamiast nazwy dzierżawy.

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDeviceAuthentication

Użyj uwierzytelniania kodu urządzenia zamiast kontrolki przeglądarki.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile

## NOTATKI

## LINKI POKREWNE
