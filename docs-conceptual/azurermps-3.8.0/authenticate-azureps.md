---
title: Logowanie za pomocą programu Azure PowerShell
description: Logowanie za pomocą programu Azure PowerShell
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 1af5aeffb8e87e916df3e2440a84805935136c0f
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 05/08/2018
---
# <a name="log-in-with-azure-powershell"></a>Logowanie za pomocą programu Azure PowerShell

Program Azure PowerShell obsługuje wiele metod logowania. Najprostszym sposobem rozpoczęcia pracy jest interaktywne zalogowanie się w wierszu polecenia.

## <a name="interactive-log-in"></a>Logowanie interaktywne

1. Wpisz polecenie `Login-AzureRmAccount`. Zostanie wyświetlone okno dialogowe z monitem o podanie poświadczeń platformy Azure.

2. Wpisz adres e-mail i hasło skojarzone z kontem. Nastąpi uwierzytelnienie i zapisanie informacji o poświadczeniach na platformie Azure, a następnie zamknięcie okna.

## <a name="log-in-with-a-service-principal"></a>Logowanie za pomocą jednostki usługi

Jednostki usługi zapewniają możliwość tworzenia nieinteraktywnych kont, których możesz używać do manipulowania zasobami. Jednostki usługi są podobne do kont użytkowników, do których można zastosować reguły za pomocą usługi Azure Active Directory. Udzielając minimalnych uprawnień niezbędnych dla jednostki usługi, możesz zapewnić, że skrypty automatyzacji będą jeszcze bezpieczniejsze.

1. Jeśli nie masz jeszcze jednostki usługi, [utwórz ją](create-azure-service-principal-azureps.md).

2. Zaloguj się za pomocą jednostki usługi.

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    Aby uzyskać identyfikator TenantId, zaloguj się interaktywnie i uzyskaj identyfikator dzierżawy ze swojej subskrypcji.

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a>Logowanie się za pomocą tożsamości zarządzanej usługi maszyny wirtualnej platformy Azure

Tożsamość usługi zarządzanej (MSI) jest dostępna w wersji zapoznawczej usługi Azure Active Directory. Jednostki usługi tożsamości usługi zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów.

Aby uzyskać więcej informacji na temat tożsamości usługi zarządzanej, zobacz [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition (Sposób użycia tożsamości usługi zarządzanej maszyny wirtualnej platformy Azure do logowania się i uzyskania tokenu)](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="log-in-to-another-cloud"></a>Logowanie się do innej chmury

Usługi w chmurze platformy Azure udostępniają różne środowiska zgodne z przepisami dotyczącymi obsługi danych określonymi przez administrację rządową poszczególnych krajów. Jeśli dane konto Azure znajduje się w chmurze administracji rządowej, podczas logowania należy określić środowisko. Jeśli na przykład konto należy do chmury chińskiej, rejestracja odbywa się za pomocą następującego polecenia:

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Użyj następującego polecenia, aby uzyskać listę dostępnych środowisk:

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Dowiedz się więcej o zarządzaniu dostępem opartym na rolach na platformie Azure

Aby uzyskać więcej informacji o zarządzaniu uwierzytelnianiem i subskrypcjami platformy Azure, zobacz [Zarządzanie kontami, subskrypcjami i rolami administracyjnymi](/azure/active-directory/role-based-access-control-configure).

Polecenia cmdlet programu Azure PowerShell umożliwiające zarządzanie rolami

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
