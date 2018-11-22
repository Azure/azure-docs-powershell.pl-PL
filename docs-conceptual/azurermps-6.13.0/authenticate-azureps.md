---
title: Logowanie się w programie Azure PowerShell
description: Jak zalogować się w programie Azure PowerShell jako użytkownik albo za pomocą jednostki usługi lub tożsamości zarządzanych dla zasobów platformy Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 6a42217c47c1e5101a708da87c15fc14004f2069
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259690"
---
# <a name="sign-in-with-azure-powershell"></a>Logowanie się w programie Azure PowerShell

Program Azure PowerShell obsługuje kilka metod uwierzytelniania. Najprostszym sposobem rozpoczęcia pracy jest interaktywne zalogowanie się w wierszu polecenia.

## <a name="sign-in-interactively"></a>Logowanie interakcyjne

Aby zalogować się interakcyjnie, skorzystaj z polecenia cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).

```azurepowershell-interactive
Connect-AzureRmAccount
```

Po uruchomieniu to polecenie cmdlet spowoduje otworzenie okna dialogowego z monitem o podanie adresu e-mail i hasła skojarzonego z kontem platformy Azure. To uwierzytelnienie obowiązuje dla bieżącej sesji programu PowerShell.

> [!IMPORTANT]
> Począwszy od programu Azure PowerShell w wersji 6.3.0, poświadczenia są współużytkowane w ramach wielu sesji programu PowerShell, dopóki użytkownik jest zalogowany w systemie Windows. Aby uzyskać więcej informacji, zobacz artykuł dotyczący [poświadczeń trwałych](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Logowanie za pomocą jednostki usługi

Jednostki usługi to nieinterakcyjne konta platformy Azure. Podobnie jak w przypadku innych kont użytkownika, ich uprawnieniami zarządza się za pomocą usługi Azure Active Directory. Udzielając jednostce usługi tylko potrzebnych uprawnień, możesz zapewnić bezpieczeństwo skryptom automatyzacji.

Aby dowiedzieć się, jak utworzyć jednostkę usługi do użycia z programem Azure PowerShell, zobacz [Tworzenie jednostki usługi platformy Azure za pomocą programu Azure PowerShell](create-azure-service-principal-azureps.md).

Aby zalogować się przy użyciu jednostki usługi, podaj argument `-ServicePrincipal` w poleceniu cmdlet `Connect-AzureRmAccount`. Z jednostką usługi trzeba będzie również skojarzyć jej identyfikator aplikacji, poświadczenia logowania oraz identyfikator dzierżawy. Aby pobrać poświadczenia jednostki usługi jako odpowiedni obiekt, użyj polecenia cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). To polecenie cmdlet spowoduje wyświetlenie okna dialogowego umożliwiającego wprowadzenie identyfikatora i hasła użytkownika.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Logowanie się za pomocą tożsamości usługi zarządzanej platformy Azure

Zarządzane tożsamości dla zasobów platformy Azure to funkcja usługi Azure Active Directory. Jednostki usługi tożsamości zarządzanej można używać do logowania się i uzyskiwania aplikacyjnego tokenu dostępu do uzyskania dostępu do innych zasobów. Tożsamości zarządzane są dostępne tylko w przypadku maszyn wirtualnych działających w chmurze platformy Azure.

Aby uzyskać więcej informacji na temat tożsamości zarządzanych dla zasobów platformy Azure, zobacz [Jak używać tożsamości zarządzanych dla zasobów platformy Azure na maszynie wirtualnej platformy Azure w celu uzyskania tokenu dostępu](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>Logowanie się jako dostawca rozwiązań w chmurze

Do zalogowania [dostawcy rozwiązań w chmurze](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) wymagane jest użycie parametru `-TenantId`. Zazwyczaj ten parametr można podać jako identyfikator dzierżawy lub nazwę domeny. Jednak w przypadku logowania dostawcy rozwiązań w chmurze trzeba podać **identyfikator dzierżawy**.

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Logowanie się do innej chmury

Usługi w chmurze platformy Azure oferują środowiska zgodne z regionalnymi przepisami dotyczącymi obsługi danych.
W przypadku kont w chmurze regionalnej określ środowisko po zalogowaniu się, używając argumentu `-Environment`.
Na przykład jeśli Twoje konto znajduje się w chmurze w Chinach:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Następujące polecenie pozwala uzyskać listę dostępnych środowisk:

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Dowiedz się więcej o zarządzaniu dostępem opartym na rolach na platformie Azure

Aby uzyskać więcej informacji o zarządzaniu uwierzytelnianiem i subskrypcjami platformy Azure, zobacz [Zarządzanie kontami, subskrypcjami i rolami administracyjnymi](/azure/active-directory/role-based-access-control-configure).

Polecenia cmdlet programu Azure PowerShell umożliwiające zarządzanie rolami:

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
