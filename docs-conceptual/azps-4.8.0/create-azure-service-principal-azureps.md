---
title: Używanie jednostek usługi platformy Azure w programie Azure PowerShell
description: Dowiedz się, jak utworzyć jednostkę usługi i używać jej za pomocą programu Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 08d0f055a1f17b4da7e68885c8611e790aab3a3d
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251798"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell

Zautomatyzowane narzędzia, które korzystają z usług platformy Azure, powinny zawsze mieć ograniczone uprawnienia. Zamiast wymagać, aby aplikacje logowały się jako użytkownik z pełnymi uprawnieniami, platforma Azure oferuje jednostki usługi.

Jednostka usługi platformy Azure to tożsamość przeznaczona do użycia z aplikacjami, usługami hostowanymi i zautomatyzowanymi narzędziami w celu uzyskiwania dostępu do zasobów platformy Azure. Ten dostęp jest ograniczony przez role przypisane do jednostki usługi, dzięki czemu możesz kontrolować, do których zasobów jest uzyskiwany dostęp i na jakim poziomie. Ze względów bezpieczeństwa zawsze zaleca się używanie jednostek usługi ze zautomatyzowanymi narzędziami, zamiast zezwalać im na logowanie za pomocą tożsamości użytkownika.

W tym artykule przedstawiono kroki tworzenia i resetowania jednostki usługi oraz uzyskiwania informacji o niej przy użyciu programu Azure PowerShell.

> [!WARNING]
> Gdy tworzysz jednostkę usługi za pomocą polecenia [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal), dane wyjściowe zawierają poświadczenia, które należy chronić. Alternatywnie rozważ użycie [tożsamości zarządzanych](/azure/active-directory/managed-identities-azure-resources/overview), aby uniknąć konieczności używania poświadczeń.
>
> Domyślnie polecenie [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) przypisuje rolę [Współautor](/azure/role-based-access-control/built-in-roles#contributor) do jednostki usługi w zakresie subskrypcji. Aby zmniejszyć ryzyko naruszenia zabezpieczeń jednostki usługi, przypisz bardziej konkretną rolę i zawęź zakres do zasobu lub grupy zasobów. Aby uzyskać więcej informacji, zobacz [Kroki dodawania przypisania roli](/azure/role-based-access-control/role-assignments-steps).

## <a name="create-a-service-principal"></a>Tworzenie nazwy głównej usługi

Utwórz jednostkę usługi za pomocą polecenia cmdlet [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal). Podczas tworzenia jednostki usługi wybierz używany przez nią typ uwierzytelniania logowania.

> [!NOTE]
> Jeśli konto nie ma wystarczających uprawnień do utworzenia jednostki usługi, polecenie `New-AzADServicePrincipal` zwróci komunikat „Uprawnienia niewystarczające do ukończenia operacji”.
> Skontaktuj się z administratorem usługi Azure Active Directory w celu utworzenia jednostki usługi.

Istnieją dwa typy uwierzytelniania dostępne dla jednostek usługi: Uwierzytelnianie oparte na hasłach i uwierzytelnianie oparte na certyfikatach.

### <a name="password-based-authentication"></a>Uwierzytelnianie oparte na hasłach

> [!IMPORTANT]
> Domyślna rola jednostki usługi uwierzytelniania opartego na hasłach to **Współautor**. Ta rola ma pełne uprawnienia do odczytu i zapisu dla konta platformy Azure. Aby uzyskać informacje na temat zarządzania przypisaniami ról, zobacz [Zarządzanie rolami jednostki usługi](#manage-service-principal-roles).

Jeśli żadne inne parametry uwierzytelniania nie istnieją, jest używane uwierzytelnianie oparte na hasłach i otrzymujesz hasło utworzone losowo. Jeśli chcesz używać uwierzytelniania opartego na hasłach, ta metoda jest zalecana.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Zwrócony obiekt zawiera element członkowski `Secret`, który jest elementem `SecureString` zawierającym wygenerowane hasło. Upewnij się, że ta wartość jest przechowywana w bezpiecznym miejscu, aby przeprowadzać uwierzytelnianie za pomocą jednostki usługi. Wartość _nie_ będzie wyświetlana w danych wyjściowych konsoli. W przypadku utraty hasła [zresetuj poświadczenia jednostki usługi](#reset-credentials).

Następujący kod pozwala wyeksportować wpis tajny:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

W przypadku haseł podawanych przez użytkowników argument `-PasswordCredential` przyjmuje obiekty `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`. Te obiekty muszą mieć prawidłowe daty `StartDate` i `EndDate` oraz zawierać zwykły tekst typu `Password`. Podczas tworzenia hasła upewnij się, że przestrzegasz [reguł i ograniczeń dotyczących haseł usługi Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).
Nie używaj słabych haseł ani nie stosuj ponownie tych samych haseł.

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

Obiekt zwrócony przez polecenie `New-AzADServicePrincipal` zawiera elementy członkowskie `Id` i `DisplayName`. Każdego z nich można użyć do logowania przy użyciu jednostki usługi.

> [!IMPORTANT]
> Logowanie za pomocą jednostki usługi wymaga identyfikatora dzierżawy, w ramach którego utworzono jednostkę usługi. Aby pobrać dzierżawę aktywną w trakcie tworzenia jednostki usługi, uruchom następujące polecenie _natychmiast po_ utworzeniu jednostki usługi:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a>Uwierzytelnianie oparte na certyfikacie

> [!IMPORTANT]
> Podczas tworzenia jednostki usługi uwierzytelniania opartego na certyfikacie nie jest przypisywana rola domyślna. Aby uzyskać informacje na temat zarządzania przypisaniami ról, zobacz [Zarządzanie rolami jednostki usługi](#manage-service-principal-roles).

Jednostki usługi używające uwierzytelniania opartego na certyfikatach są tworzone za pomocą parametru `-CertValue`. Ten parametr przyjmuje ciąg ASCII szyfrowany przy użyciu algorytmu base64 z certyfikatu publicznego. Jest on reprezentowany przez plik PEM lub plik CRT lub CER zakodowany jako tekst. Kodowania plików binarnych certyfikatu publicznego nie są obsługiwane. W instrukcjach założono, że masz już dostępny certyfikat.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

Możesz również użyć parametru `-KeyCredential`, który przyjmuje obiekty `PSADKeyCredential`. Te obiekty muszą mieć prawidłowe daty `StartDate` i `EndDate` oraz element członkowski `CertValue` ustawiony na ciąg ASCII kodowany przy użyciu algorytmu base64 z certyfikatu publicznego.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

Obiekt zwrócony przez polecenie `New-AzADServicePrincipal` zawiera elementy członkowskie `Id` i `DisplayName`. Każdego z nich można użyć do logowania przy użyciu jednostki usługi. Klienci logujący się przy użyciu jednostki usługi potrzebują również dostępu do klucza prywatnego certyfikatu.

> [!IMPORTANT]
> Logowanie za pomocą jednostki usługi wymaga identyfikatora dzierżawy, w ramach którego utworzono jednostkę usługi. Aby pobrać dzierżawę aktywną w trakcie tworzenia jednostki usługi, uruchom następujące polecenie _natychmiast po_ utworzeniu jednostki usługi:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a>Uzyskiwanie istniejącej jednostki usługi

Listę jednostek usługi dla aktywnej dzierżawy można pobrać przy użyciu polecenia [Get AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal). Domyślnie to polecenie zwraca _wszystkie_ jednostki usługi w dzierżawie. Zwrócenie wyników w przypadku dużych organizacji może zająć dużo czasu. Zamiast tego zaleca się użycie jednego z opcjonalnych argumentów filtrowania po stronie serwera:

- `-DisplayNameBeginsWith` żąda jednostek usługi, które mają _prefiks_ odpowiadający podanej wartości. Nazwa wyświetlana jednostki usługi jest wartością ustawioną przy użyciu opcji `-DisplayName` podczas tworzenia.
- `-DisplayName` żąda _dokładnego dopasowania_ nazwy jednostki usługi.

## <a name="manage-service-principal-roles"></a>Zarządzanie rolami jednostki usługi

Program Azure PowerShell oferuje następujące polecenia cmdlet do zarządzania przypisaniami ról:

- [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
- [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
- [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

Domyślna rola jednostki usługi uwierzytelniania opartego na hasłach to **Współautor**. Ta rola ma pełne uprawnienia do odczytu i zapisu dla konta platformy Azure. Rola **Czytelnik** jest bardziej restrykcyjna i zapewnia dostęp tylko do odczytu. Aby uzyskać więcej informacji o rolach i kontroli dostępu opartej na rolach (RBAC), zobacz [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles) (Kontrola dostępu oparta na rolach: role wbudowane).

W tym przykładzie jest dodawana rola **Czytelnik** i usuwana rola **Współautor**:

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> Polecenia cmdlet przypisania roli nie przyjmują identyfikatora obiektu jednostki usługi. Przyjmują one identyfikator skojarzonej aplikacji, który jest generowany podczas tworzenia. Aby uzyskać identyfikator aplikacji dla jednostki usługi, użyj polecenia `Get-AzADServicePrincipal`.

> [!NOTE]
> Jeśli konto nie ma uprawnienia do przypisywania roli, zobaczysz komunikat o błędzie informujący, że Twoje konto „nie ma autoryzacji do wykonania akcji Microsoft.Authorization/roleAssignments/write”. Skontaktuj się z administratorem usługi Azure Active Directory w celu zarządzania rolami.

Dodanie roli _nie_ ogranicza wcześniej przypisanych uprawnień. Po ograniczeniu uprawnień jednostki usługi rola **Współautor** powinna zostać usunięta.

Zmiany można zweryfikować przez wyświetlenie listy przypisanych ról:

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>Logowanie za pomocą jednostki usługi

Przetestuj poświadczenia i uprawnienia nowej jednostki usługi przez zalogowanie. Do zalogowania się przy użyciu jednostki usługi potrzebujesz skojarzonej z nią wartości `applicationId`, a także dzierżawy, w ramach której została utworzona.

Aby zalogować się przy użyciu jednostki usługi używającej hasła:

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID>
```

Uwierzytelnianie oparte na certyfikatach wymaga, aby program Azure PowerShell mógł pobierać informacje z lokalnego magazynu certyfikatów na podstawie na odcisku palca certyfikatu.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

Aby uzyskać instrukcje dotyczące importowania certyfikatu do magazynu poświadczeń dostępnego z programu PowerShell, zobacz [Logowanie się w programie Azure PowerShell](authenticate-azureps.md#sp-signin)

## <a name="reset-credentials"></a>Resetowanie poświadczeń

Jeśli nie pamiętasz poświadczeń dla jednostki usługi, użyj polecenia [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential), aby dodać nowe poświadczenie z losowym hasłem. To polecenie cmdlet nie obsługuje poświadczeń zdefiniowanych przez użytkownika podczas resetowania hasła.

> [!IMPORTANT]
> Przed przypisaniem nowych poświadczeń możesz usunąć istniejące poświadczenia, aby zapobiec logowaniu przy ich użyciu. W tym celu użyj polecenia cmdlet [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a>Rozwiązywanie problemów

Jeśli zostanie wyświetlony błąd: _„New-AzADServicePrincipal: Istnieje już inny obiekt o tej samej wartości właściwości identifierUris”_ , upewnij się, że nie istnieje jednostka usługi o tej samej nazwie.

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Jeśli istniejąca jednostka usługi nie jest już potrzebna, możesz ją usunąć przy użyciu poniższego przykładu.

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Ten błąd może wystąpić również wtedy, gdy wcześniej utworzono jednostkę usługi dla aplikacji usługi Azure Active Directory. Po usunięciu jednostki usługi aplikacja będzie nadal dostępna. Ta aplikacja uniemożliwia utworzenie innej jednostki usługi o tej samej nazwie.

Za pomocą następującego przykładu możesz się upewnić, że aplikacja usługi Azure Active Directory o tej samej nazwie nie istnieje:

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

Jeśli aplikacja o tej samej nazwie istnieje i nie jest już potrzebna, możesz ją usunąć przy użyciu poniższego przykładu.

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

W przeciwnym razie wybierz alternatywną nazwę nowej jednostki usługi, którą próbujesz utworzyć.
