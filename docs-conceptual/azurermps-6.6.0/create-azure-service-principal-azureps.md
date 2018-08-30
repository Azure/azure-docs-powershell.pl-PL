---
title: Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell
description: Dowiedz się, jak utworzyć jednostkę usługi dla swojej aplikacji lub usługi za pomocą programu Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 76d690f3a7206857861e1ee26d8284de419dc70a
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/14/2018
ms.locfileid: "43018810"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell

Jeśli planujesz zarządzanie swoją aplikacją lub usługą za pomocą programu Azure PowerShell, musisz uruchomić go w ramach jednostki usługi Azure Active Directory (AAD), a nie przy użyciu własnych poświadczeń. W tym temacie przedstawiono kroki umożliwiające utworzenie podmiotu zabezpieczeń za pomocą programu Azure PowerShell.

> [!NOTE]
> Za pośrednictwem witryny Azure Portal możesz również utworzyć jednostkę usługi. Aby uzyskać więcej szczegółów, przeczytaj artykuł [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) (Używanie portalu do tworzenia aplikacji usługi Active Directory i jednostki usługi używanej do uzyskiwania dostępu do zasobów).

## <a name="what-is-a-service-principal"></a>Co to jest „jednostka usługi”?

Jednostka usługi platformy Azure to tożsamość zabezpieczeń używana przez aplikacje, usługi i narzędzia automatyzacji utworzone przez użytkownika w celu uzyskania dostępu do określonych zasobów platformy Azure. Można ją traktować jako „tożsamość użytkownika” (nazwa logowania i hasło lub certyfikat) z określoną rolą i ściśle kontrolowanymi uprawnieniami. Musi ona mieć możliwość wykonywania tylko konkretnych czynności w odróżnieniu od ogólnej tożsamości użytkownika. Nazwa główna usługi pozwala poprawić bezpieczeństwo, jeśli przyznasz jej tylko minimalny poziom uprawnień potrzebny do wykonywania zadań zarządzania.

## <a name="verify-your-own-permission-level"></a>Sprawdzenie własnego poziomu uprawnień

Po pierwsze, musisz mieć wystarczające uprawnienia zarówno w usłudze Azure Active Directory, jak i subskrypcji platformy Azure. W szczególności musisz mieć możliwość tworzenia aplikacji w usłudze Active Directory i przypisywania roli do jednostki usługi.

Najłatwiejszym sposobem sprawdzenia, czy Twoje konto ma odpowiednie uprawnienia, jest skorzystanie z portalu. Zobacz [Sprawdzanie wymaganego uprawnienia w portalu](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Tworzenie jednostki usługi dla aplikacji

Po zalogowaniu się na koncie platformy Azure można utworzyć jednostkę usługi. Aby zidentyfikować wdrożoną aplikację, musisz użyć jednej z następujących metod:

* Unikatowa nazwa wdrożonej aplikacji, na przykład „MyDemoWebApp” w poniższych przykładach, lub
* Identyfikator aplikacji, unikatowy identyfikator GUID skojarzony z wdrożoną aplikacją, usługą lub obiektem

### <a name="get-information-about-your-application"></a>Pobieranie informacji o aplikacji

Aby znaleźć informacje o aplikacji, można użyć polecenia cmdlet `Get-AzureRmADApplication`.

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>Tworzenie jednostki usługi dla aplikacji

Do utworzenia jednostki usługi służy polecenie cmdlet `New-AzureRmADServicePrincipal`.

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>Pobieranie informacji o jednostce usługi

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>Logowanie za pomocą jednostki usługi

Możesz teraz zalogować się w ramach nowej jednostki usługi dla aplikacji przy użyciu podanych opcji *appId* i *password*. Musisz podać identyfikator dzierżawy dla swojego konta. Identyfikator dzierżawy jest wyświetlany po zalogowaniu się do platformy Azure przy użyciu osobistych poświadczeń.

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Uruchom to polecenie w nowej sesji programu PowerShell. Po pomyślnym zalogowaniu zostaną wyświetlone dane wyjściowe, wyglądające mniej więcej tak:

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

Gratulacje! Możesz użyć tych poświadczeń do uruchomienia aplikacji. Następnie musisz dostosować uprawnienia jednostki usługi.

## <a name="managing-roles"></a>Zarządzanie rolami

> [!NOTE]
> Kontrola dostępu oparta na rolach (RBAC) platformy Azure to model definiowania ról użytkowników i jednostek usługi oraz zarządzania nimi. Role mają skojarzone ze sobą zestawy uprawnień umożliwiające wskazanie zasobów, które nazwa główna może odczytywać, zapisywać, do których może uzyskać dostęp lub którymi może zarządzać. Aby uzyskać więcej informacji o rolach i kontroli dostępu opartej na rolach, zobacz [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles) (Kontrola dostępu oparta na rolach (RBAC): role wbudowane).

Program Azure PowerShell udostępnia następujące polecenia cmdlet do zarządzania przypisaniami ról:

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

Rolą domyślną dla jednostki usługi jest **Współautor**. Biorąc pod uwagę szerokie uprawnienia tej roli, jej użycie może nie być najlepszą opcją, w zależności od zakresu interakcji aplikacji z usługami platformy Azure.
Rola **Czytelnik** jest bardziej restrykcyjna i jest dobrym wyborem dla aplikacji potrzebujących dostępu tylko do odczytu. Za pomocą witryny Azure Portal możesz wyświetlić szczegóły uprawnień specyficznych dla ról lub utworzyć niestandardowe uprawnienia.

Zmienimy teraz poprzedni przykład — dodamy rolę **Czytelnik** i usuniemy rolę **Współautor**:

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Aby wyświetlić obecnie przypisane role:

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

Inne polecenia cmdlet programu Azure PowerShell umożliwiające zarządzania rolami:

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Zmienianie poświadczeń podmiotu zabezpieczeń

Dobrą praktyką w zakresie zabezpieczeń jest regularne sprawdzanie uprawnień i aktualizowanie haseł. Warto też zarządzać poświadczeniami zabezpieczeń i modyfikować je w miarę wprowadzania zmian w aplikacji. Można na przykład zmienić hasło jednostki usługi, tworząc nowe hasło i usuwając stare.

### <a name="add-a-new-password-for-the-service-principal"></a>Dodawanie nowego hasła dla jednostki usługi

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Pobieranie listy poświadczeń dla jednostki usługi

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Usuwanie starego hasła dla jednostki usługi

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Sprawdzanie listy poświadczeń dla jednostki usługi

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
