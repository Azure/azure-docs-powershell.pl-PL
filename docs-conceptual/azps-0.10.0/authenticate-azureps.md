---
title: Logowanie się w programie Azure PowerShell
description: Jak zalogować się w programie Azure PowerShell jako użytkownik albo za pomocą jednostki usługi lub tożsamości zarządzanych dla zasobów platformy Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/04/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: e9eccbcb88074db19701fef86b1ff03b4ec2ae87
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/06/2020
ms.locfileid: "93409928"
---
# <a name="sign-in-with-azure-powershell"></a>Logowanie się w programie Azure PowerShell

Program Azure PowerShell obsługuje kilka metod uwierzytelniania. Najprostszym sposobem na rozpoczęcie pracy jest usługa [Azure Cloud Shell](/azure/cloud-shell/overview), która loguje Cię automatycznie. W przypadku instalacji lokalnej możesz logować się interaktywnie za pośrednictwem przeglądarki. Podczas pisania skryptów automatyzacji zalecanym rozwiązaniem jest użycie [jednostki usługi](create-azure-service-principal-azureps.md) z odpowiednimi uprawnieniami. Możliwie największe ograniczenie uprawnień logowania w danym przypadku użycia pomaga w zabezpieczeniu zasobów platformy Azure.

Po zalogowaniu się polecenia są uruchamiane względem subskrypcji domyślnej. Aby zmienić aktywną subskrypcję dla sesji, użyj polecenia cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext). Aby zmienić domyślną subskrypcję używaną podczas logowania się przy użyciu programu Azure PowerShell, użyj polecenia [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).

> [!IMPORTANT]
>
> Poświadczenia są współdzielone w ramach wielu sesji programu PowerShell, dopóki użytkownik pozostanie zalogowany.
> Aby uzyskać więcej informacji, zobacz artykuł dotyczący [poświadczeń trwałych](context-persistence.md).

## <a name="sign-in-interactively"></a>Logowanie interakcyjne

Aby zalogować się interakcyjnie, skorzystaj z polecenia cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

Po uruchomieniu to polecenie cmdlet spowoduje wyświetlenie ciągu tokenu. Aby się zalogować, skopiuj ten ciąg i wklej go w witrynie https://microsoft.com/devicelogin w przeglądarce. Sesja programu PowerShell zostanie uwierzytelniona na potrzeby połączenia z platformą Azure.

> [!IMPORTANT]
>
> Autoryzacja poświadczenia nazwy użytkownika/hasła została usunięta z programu Azure PowerShell z powodu zmian implementacji autoryzacji usługi Active Directory i zagadnień związanych z bezpieczeństwem.
> Jeśli używasz autoryzacji poświadczeń do celów automatyzacji, w zamian [utwórz jednostkę usługi](create-azure-service-principal-azureps.md).

## <a name="sign-in-with-a-service-principal"></a>Logowanie za pomocą jednostki usługi <a name="sp-signin"/>

Jednostki usługi to nieinterakcyjne konta platformy Azure. Podobnie jak w przypadku innych kont użytkownika, ich uprawnieniami zarządza się za pomocą usługi Azure Active Directory. Udzielając jednostce usługi tylko potrzebnych uprawnień, możesz zapewnić bezpieczeństwo skryptom automatyzacji.

Aby dowiedzieć się, jak utworzyć jednostkę usługi do użycia z programem Azure PowerShell, zobacz [Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell](create-azure-service-principal-azureps.md).

Aby zalogować się przy użyciu jednostki usługi, podaj argument `-ServicePrincipal` w poleceniu cmdlet `Connect-AzAccount`. Z jednostką usługi trzeba będzie również skojarzyć jej identyfikator aplikacji, poświadczenia logowania oraz identyfikator dzierżawy. Sposób logowania przy użyciu jednostki usługi będzie zależeć od tego, czy została ona skonfigurowana do uwierzytelniania opartego na hasłach, czy opartego na certyfikatach.

### <a name="password-based-authentication"></a>Uwierzytelnianie oparte na hasłach

Aby pobrać poświadczenia jednostki usługi jako odpowiedni obiekt, użyj polecenia cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). To polecenie cmdlet wyświetli monit o podanie nazwy użytkownika i hasła. Użyj identyfikatora jednostki usługi w przypadku nazwy użytkownika.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Dla scenariuszy automatyzacji musisz utworzyć poświadczenia na podstawie nazwy użytkownika i bezpiecznego ciągu:

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Upewnij się, że podczas automatyzowania połączeń jednostki usługi używasz najlepszych rozwiązań dotyczących magazynu haseł.

### <a name="certificate-based-authentication"></a>Uwierzytelnianie oparte na certyfikacie

Uwierzytelnianie oparte na certyfikatach wymaga, aby program Azure PowerShell mógł pobierać informacje z lokalnego magazynu certyfikatów na podstawie na odcisku palca certyfikatu.

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

Jeśli zamiast zarejestrowanej aplikacji używasz jednostki usługi, dodaj argument `-ServicePrincipal` i podaj identyfikator aplikacji jednostki usługi jako wartość parametru `-ApplicationId`.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

W programie PowerShell 5.1 zarządzanie magazynem certyfikatów i jego badanie może odbywać się za pomocą modułu infrastruktury [PKI](/powershell/module/pkiclient). Dla programu PowerShell Core w wersji 6.x i późniejszych proces jest bardziej skomplikowany. Poniższe skrypty pokazują, jak zaimportować istniejący certyfikat do magazynu certyfikatów dostępnego w programie PowerShell.

#### <a name="import-a-certificate-in-powershell-51"></a>Importowanie certyfikatu w programie PowerShell 5.1

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a>Importowanie certyfikatu w programie PowerShell Core w wersji 6.x lub nowszej

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My 
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser 
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation) 
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable 
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag) 
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite) 
$store.Add($Certificate) 
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a>Logowanie się przy użyciu tożsamości zarządzanej

Tożsamości zarządzane to funkcja w usłudze Azure Active Directory. Tożsamości zarządzane to jednostki usługi przypisane do zasobów, które działają na platformie Azure. Jednostki usługi tożsamości zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów. Tożsamości zarządzane są dostępne tylko w przypadku zasobów działających w chmurze platformy Azure.

To polecenie nawiązuje połączenie przy użyciu tożsamości zarządzanej środowiska hosta. Na przykład w przypadku wykonania na maszynie wirtualnej z przypisaną tożsamością usługi zarządzanej umożliwia kodowi logowanie się przy użyciu tej przypisanej tożsamości.

```azurepowershell-interactive
 Connect-AzAccount -Identity 
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Logowanie się przy użyciu innej niż domyślnej dzierżawy lub jako dostawca rozwiązań w chmurze (CSP, Cloud Solution Provider)

Jeśli konto jest skojarzone z więcej niż jedną dzierżawą, logowanie wymaga użycia parametru `-Tenant` podczas nawiązywania połączenia. Ten parametr będzie współdziałać z każdą metodą logowania. Podczas logowania się wartość tego parametru może być identyfikatorem obiektu platformy Azure dzierżawy (identyfikatorem dzierżawy) lub w pełni kwalifikowaną nazwą domeny dzierżawy.

Jeśli jesteś [dostawcą rozwiązań w chmurze (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), wartość `-Tenant`**musi** być identyfikatorem dzierżawy.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Logowanie się do innej chmury

Usługi w chmurze platformy Azure oferują środowiska zgodne z regionalnymi przepisami dotyczącymi obsługi danych.
W przypadku kont w chmurze regionalnej określ środowisko po zalogowaniu się, używając argumentu `-Environment`.
Ten parametr będzie współdziałać z każdą metodą logowania. Na przykład jeśli Twoje konto znajduje się w chmurze w Chinach:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Następujące polecenie pozwala uzyskać listę dostępnych środowisk:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
