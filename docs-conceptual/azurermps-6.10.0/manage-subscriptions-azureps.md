---
title: Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell
description: Zarządzanie subskrypcjami platformy Azure za pomocą programu Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 3f1c1bab5f9903ee7df813bf1ef043c7107ebe79
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399131"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="3790e-103">Zarządzanie wieloma subskrypcjami platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3790e-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="3790e-104">Jeśli dopiero zaczynasz korzystać z platformy Azure, najprawdopodobniej masz tylko jedną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="3790e-104">If you're brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="3790e-105">Jeśli jednak korzystasz z platformy Azure już przez jakiś czas, możesz mieć utworzonych wiele subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3790e-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="3790e-106">Możesz skonfigurować program Azure PowerShell do wykonywania poleceń dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3790e-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="3790e-107">Pobierz listę wszystkich subskrypcji na swoim koncie.</span><span class="sxs-lookup"><span data-stu-id="3790e-107">Get a list of all subscriptions in your account.</span></span>

    ```azurepowershell-interactive
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

2. <span data-ttu-id="3790e-108">Ustaw domyślną.</span><span class="sxs-lookup"><span data-stu-id="3790e-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. <span data-ttu-id="3790e-109">Sprawdź zmiany, uruchamiając polecenie cmdlet `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="3790e-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```azurepowershell-interactive
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

<span data-ttu-id="3790e-110">Po ustawieniu domyślnej subskrypcji wszystkie polecenia programu Azure PowerShell będą uruchamiane dla tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3790e-110">Once you set your default subscription, all Azure PowerShell commands run against this subscription.</span></span>
