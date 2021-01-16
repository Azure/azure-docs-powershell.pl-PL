---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: e997013eb5646ca0f22904dd6fc68cf09a3ba228
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333262"
---
# Connect-AzAccount

## STRESZCZENIe
Połącz się z platformą Azure za pomocą konta uwierzytelnionego do użycia z poleceniami cmdlet z poziomu AZ modułów programu PowerShell.

## POLECENIA

### UserWithSubscriptionId (domyślny)
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

## Opis

`Connect-AzAccount`Polecenie cmdlet umożliwia nawiązanie połączenia z platformą Azure za pomocą konta uwierzytelnionego do użycia z poleceniami cmdlet z modułów AZ programu PowerShell. Możesz używać tego konta uwierzytelnionego tylko w przypadku żądań usługi Azure Resource Manager. Aby dodać uwierzytelnione konto do użytku z zarządzaniem usługami, użyj `Add-AzureAccount` polecenia cmdlet z modułu Azure PowerShell. Jeśli nie odnaleziono kontekstu dla bieżącego użytkownika, lista kontekstowa użytkownika zostanie uzupełniona kontekstem dla każdego z nich pierwszych 25 abonamentów.
Lista kontekstów utworzonych dla użytkownika można znaleźć, uruchamiając `Get-AzContext -ListAvailable` . Aby pominąć tę populację kontekstu, określ parametr przełącznika **SkipContextPopulation** . Po wykonaniu tego polecenia cmdlet możesz rozłączyć konto platformy Azure przy użyciu `Disconnect-AzAccount` .

## Przykłady

### Przykład 1: Nawiązywanie połączenia z kontem na platformie Azure

W tym przykładzie nawiążesz połączenie z kontem na platformie Azure. Musisz podać poświadczenia konta Microsoft lub identyfikatora organizacji. Jeśli dla poświadczeń włączono uwierzytelnianie wieloskładnikowe, należy zalogować się przy użyciu opcji interakcyjnej lub użyć uwierzytelniania głównego usługi.

```powershell
Connect-AzAccount
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 2: (tylko program Windows PowerShell 5,1) Nawiązywanie połączenia z usługą Azure przy użyciu poświadczeń identyfikatora organizacji

Ten scenariusz działa tylko w programie Windows PowerShell 5,1. Pierwsze polecenie monituje o podanie poświadczeń użytkownika i przechowuje je w `$Credential` zmiennej. Drugie polecenie nawiązuje połączenie z kontem na platformie Azure przy użyciu poświadczeń przechowywanych w programie `$Credential` . To konto jest uwierzytelniane na platformie Azure przy użyciu poświadczeń identyfikatora organizacji.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 3: Nawiązywanie połączenia z platformą Azure przy użyciu głównego konta usługi

Pierwsze polecenie monituje o podanie poświadczeń głównych usług i zapisuje je w `$Credential` zmiennej. Jeśli zostanie wyświetlony monit, wprowadź identyfikator aplikacji dla nazwy użytkownika i hasła głównego usługi. Drugie polecenie łączy określoną dzierżawę platformy Azure przy użyciu głównych poświadczeń usługi przechowywanych w `$Credential` zmiennej. Parametr **serviceprincipal** Switch wskazuje, że konto jest uwierzytelniane jako podmiot zabezpieczeń usługi.

```powershell
$Credential = Get-Credential
Connect-AzAccount -Credential $Credential -Tenant 'xxxx-xxxx-xxxx-xxxx' -ServicePrincipal
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 4: używanie interakcyjnego logowania do nawiązywania połączenia z określonym dzierżawcą i abonamentem

W tym przykładzie nawiążesz połączenie z kontem platformy Azure z określonym dzierżawcą i abonamentem.

```powershell
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx' -SubscriptionId 'yyyy-yyyy-yyyy-yyyy'
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 5: Nawiązywanie połączenia przy użyciu tożsamości usługi zarządzanej

W tym przykładzie nawiąże połączenie przy użyciu tożsamości usługi zarządzanej (MSI) środowiska hosta. Na przykład użytkownik loguje się do platformy Azure z maszyny wirtualnej z przypisanym instalatorem MSI.

```powershell
Connect-AzAccount -Identity
```

```Output
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

### Przykład 6: Nawiązywanie połączenia przy użyciu identyfikatora logowania i ClientId tożsamości zarządzanych usług

W tym przykładzie nawiąże połączenie przy użyciu tożsamości usługi zarządzanej **myUserAssignedIdentity**. Do maszyny wirtualnej zostanie dodana tożsamość użytkownika, a następnie nawiążesz połączenie przy użyciu ClientIda tożsamości przypisanej do użytkownika. Aby uzyskać więcej informacji, zobacz [Konfigurowanie tożsamości zarządzanych dla zasobów platformy Azure na maszynie wirtualnej Azure](/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm).

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

### Przykład 7: Nawiązywanie połączenia przy użyciu certyfikatów

W tym przykładzie nawiążesz połączenie z kontem na platformie Azure przy użyciu uwierzytelniania głównego usług opartego na certyfikatach.
Podmiot zabezpieczeń usługi służący do uwierzytelniania musi zostać utworzony przy użyciu określonego certyfikatu. Aby uzyskać więcej informacji na temat tworzenia certyfikatów z podpisem własnym i przypisywania im uprawnień, zobacz [Używanie platformy Azure PowerShell do tworzenia podmiotu usługi z certyfikatem](/azure/active-directory/develop/howto-authenticate-service-principal-powershell)

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

## PARAMETRÓW

### -AccessToken

Określa token dostępu.

> [!CAUTION]
> Tokeny dostępu są typu poświadczenia. Należy podjąć odpowiednie środki ostrożności, aby zachować ich poufność. Tokeny dostępu również przekroczą limit czasu i mogą uniemożliwiać wykonywanie długotrwałych zadań.

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

Identyfikator konta dla tokenu dostępu w zestawie parametrów **AccessToken** . Identyfikator konta dla usługi zarządzanej w zestawie parametrów **ManagedService** . Może to być zarządzany identyfikator zasobu usługi lub skojarzony identyfikator klienta.
Aby użyć tożsamości przypisanej do systemu, pozostaw to pole puste.

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

### -Identyfikator aplikacji

Identyfikator aplikacji głównej usługi.

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

Skrót certyfikatu lub odcisk palca.

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

### -Ontextname

Nazwa domyślnego kontekstu platformy Azure dla tego logowania. Aby uzyskać więcej informacji na temat kontekstów platformy Azure, zobacz [obiekty kontekstu usługi Azure PowerShell](/powershell/azure/context-persistence).

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

### — Poświadczenie

Określa obiekt **PSCredential** . Aby uzyskać więcej informacji na temat obiektu **PSCredential** , wpisz `Get-Help Get-Credential` . Obiekt **PSCredential** zapewnia identyfikator użytkownika i hasło dla poświadczeń identyfikatora organizacji lub identyfikator aplikacji oraz klucz tajny dla poświadczeń głównych usługi.

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

### -Środowisko

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

### -Force

Zastąp istniejący kontekst o tej samej nazwie bez monitowania.

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

AccessToken dla usługi Graph.

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

### -Identity (tożsamość)

Logowanie przy użyciu tożsamości usługi zarządzanej.

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

AccessToken dla usługi magazynu.

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

Przestarzałego. Aby użyć niestandardowego punktu końcowego MSI, Ustaw zmienną środowiskową MSI_ENDPOINT, na przykład " http://localhost:50342/oauth2/token ". Nazwa hosta usługi zarządzanej.

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

Przestarzałego. Aby użyć niestandardowego punktu końcowego MSI, Ustaw zmienną środowiskową MSI_ENDPOINT, na przykład " http://localhost:50342/oauth2/token ". Numer portu zarządzanej usługi.

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

Przestarzałego. Aby użyć niestandardowego klucza tajnego MSI, Ustaw zmienną środowiskową MSI_SECRET. Token służący do logowania zarządzanych usług.

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

Maksymalny numer abonamentu, aby wypełnić konteksty po zalogowaniu. Wartość domyślna to 25. Aby wypełnić wszystkie abonamenty kontekstowe, ustaw wartość-1.

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

### -Zakres

Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.

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

### -Serviceprincipal

Wskazuje, że to konto uwierzytelnia się, dostarczając poświadczenia podmiotu zabezpieczeń usługi.

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

### -SkipContextPopulation

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

Pomijanie sprawdzania poprawności tokenu dostępu.

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

### -Subscription

Nazwa lub Identyfikator subskrypcji.

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

### -Dzierżawca

Opcjonalna nazwa lub identyfikator dzierżawy.

> [!NOTE]
> Ze względu na ograniczenia bieżącego interfejsu API podczas łączenia się z kontem firmowym (B2B) należy użyć identyfikatora dzierżawy zamiast nazwy dzierżawy.

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

### -Potwierdź

Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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

Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. profile. Core. PSAzureProfile

## INFORMACYJN

## LINKI POKREWNE
