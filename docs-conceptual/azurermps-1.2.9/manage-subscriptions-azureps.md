---
title: Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell | Microsoft Docs
description: Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell
keywords: Azure PowerShell, subskrypcja
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 8869b700e513d6fc07e69de1dbfe852bd2a52df1
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211064"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="86ad9-104">Zarządzanie wieloma subskrypcjami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="86ad9-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="86ad9-105">Jeśli dopiero zaczynasz korzystać z platformy Azure, najprawdopodobniej masz tylko jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="86ad9-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="86ad9-106">Jeśli jednak korzystasz z platformy Azure już przez jakiś czas, możesz mieć utworzonych wiele subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="86ad9-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="86ad9-107">Możesz skonfigurować program Azure PowerShell do wykonywania poleceń dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="86ad9-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="86ad9-108">Pobierz listę wszystkich subskrypcji na swoim koncie.</span><span class="sxs-lookup"><span data-stu-id="86ad9-108">Get a list of all subscriptions in your account.</span></span>

    ```powershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. <span data-ttu-id="86ad9-109">Ustaw domyślną.</span><span class="sxs-lookup"><span data-stu-id="86ad9-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="86ad9-110">Sprawdź zmiany, uruchamiając polecenie cmdlet `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="86ad9-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```powershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="86ad9-111">Po ustawieniu domyślnej subskrypcji wszystkie kolejne polecenia programu Azure PowerShell będą uruchamiane dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="86ad9-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
