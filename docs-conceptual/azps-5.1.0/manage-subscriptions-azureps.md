---
title: Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell
description: Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 4f48e009d9769cba671ea54e8f619a9ad40603d1
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715742"
---
# <a name="use-multiple-azure-subscriptions"></a>Korzystanie z wielu subskrypcji platformy Azure

Większość użytkowników platformy Azure będzie mieć tylko jedną subskrypcję. Jeśli jednak stanowisz składnik więcej niż jednej organizacji lub Twoja organizacja podzieliła dostęp do niektórych zasobów między grupy, możesz mieć wiele subskrypcji w obrębie platformy Azure. Interfejs wiersza polecenia obsługuje wybór subskrypcji zarówno globalnie, jak i za pomocą poleceń.

Aby uzyskać szczegółowe informacje o subskrypcjach, rozliczeniach i zarządzaniu kosztami, zobacz [dokumentację dotyczącą rozliczeń i zarządzania kosztami](/azure/billing/).

## <a name="tenants-users-and-subscriptions"></a>Dzierżawy, użytkownicy i subskrypcje

Rozpoznanie różnic między dzierżawami, użytkownikami i subskrypcjami w obrębie platformy Azure może być trudne. _Dzierżawa_ to jednostka usługi Azure Active Directory, która obejmuje całą organizację. Ta dzierżawa ma co najmniej jedną _subskrypcję_ i jednego _użytkownika_. Użytkownik to osoba skojarzona z tylko jedną dzierżawą — organizacją, do której należy. Użytkownicy to konta, które logują się do platformy Azure w celu tworzenia zasobów, korzystania z nich i zarządzania nimi.
Użytkownik może mieć dostęp do wielu _subskrypcji_, które są umowami z firmą Microsoft na korzystanie z usług w chmurze, w tym z platformy Azure. Każdy zasób jest skojarzony z subskrypcją.

Aby dowiedzieć się więcej na temat różnic między dzierżawami, użytkownikami i subskrypcjami, zobacz [Słownik terminologii dotyczący chmury Azure](/azure/azure-glossary-cloud-terminology).  Aby dowiedzieć się, jak dodać nową subskrypcję do dzierżawy usługi Azure Active Directory, zobacz [Kojarzenie subskrypcji platformy Azure z dzierżawą usługi Azure Active Directory lub dodawanie subskrypcji](/azure/active-directory/active-directory-how-subscriptions-associated-directory).
Aby dowiedzieć się, jak zalogować się do określonej dzierżawy, zobacz [Logowanie się za pomocą programu Azure PowerShell](/powershell/azure/authenticate-azureps).

## <a name="change-the-active-subscription"></a>Zmiana aktywnej subskrypcji

W programie Azure PowerShell uzyskiwanie dostępu do zasobów subskrypcji wymaga zmiany subskrypcji skojarzonej z bieżącą sesją platformy Azure.
Odbywa się to poprzez zmodyfikowanie kontekstu aktywnej sesji, czyli informacji o tym, względem której dzierżawy, subskrypcji i użytkownika powinny być uruchamiane polecenia cmdlet.
Aby zmienić subskrypcje, należy najpierw pobrać obiekt kontekstu programu Azure PowerShell za pomocą polecenia [Get AzSubscription](/powershell/module/az.accounts/get-azsubscription), a następnie zmienić bieżący kontekst przy użyciu polecenia[Set-AzContext](/powershell/module/az.accounts/set-azcontext).

W kolejnym przykładzie pokazano, jak uzyskać subskrypcję w ramach bieżącej aktywnej dzierżawy i ustawić ją jako aktywną sesję:

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

Aby dowiedzieć się więcej na temat kontekstów programu Azure PowerShell, w tym jak je zapisać, a następnie szybko przełączać się między nimi na potrzeby pracy z wieloma subskrypcjami, zobacz [Persist credentials with Azure PowerShell contexts](context-persistence.md) (Utrwalanie poświadczeń za pomocą kontekstów programu Azure PowerShell).
