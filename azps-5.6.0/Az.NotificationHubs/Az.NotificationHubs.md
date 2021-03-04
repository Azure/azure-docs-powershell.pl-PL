---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: f82f5ec814159bd71a83594a501df3561b747aee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951425"
---
# <span data-ttu-id="1af68-101">Moduł Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="1af68-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="1af68-102">Opis</span><span class="sxs-lookup"><span data-stu-id="1af68-102">Description</span></span>
<span data-ttu-id="1af68-103">W tym temacie są wyświetlane tematy pomocy dotyczące polecenia cmdlet centrum powiadomień platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1af68-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="1af68-104">Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy (iOS, Android, Windows Phone 8, Sklepu Windows itp.) używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="1af68-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="1af68-105">Te centra są mniej więcej równoważne poszczególnym aplikacjom: każda z tych aplikacji zwykle ma własne centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="1af68-106">Centra powiadomień są zorganizowane w kontenerach logicznych nazywanych przestrzeniami nazw, a reguły autoryzacji podpisu dostępu udostępnionego (SAS) są używane do zarządzania dostępem do centrum i przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="1af68-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="1af68-107">Tymi wszystkimi elementami można zarządzać przy użyciu polecenia cmdlet Centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="1af68-108">Az.NotificationHubs Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1af68-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="1af68-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1af68-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="1af68-110">Otrzymuje informacje na temat swoich centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="1af68-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1af68-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1af68-112">Pobiera informacje o zasadach autoryzacji skojarzonych z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="1af68-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="1af68-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="1af68-114">Pobiera podstawowe i pomocnicze parametry połączenia skojarzone z regułą autoryzacji centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="1af68-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="1af68-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="1af68-116">Pobiera poświadczenia usługi PNS dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="1af68-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1af68-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="1af68-118">Pobiera informacje o przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="1af68-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1af68-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1af68-120">Pobiera informacje o zasadach autoryzacji skojarzonych z przestrzenią nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="1af68-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="1af68-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="1af68-122">Pobiera podstawowe i pomocnicze parametry połączenia skojarzone z regułą autoryzacji przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="1af68-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1af68-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="1af68-124">Tworzy centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="1af68-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1af68-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1af68-126">Tworzy regułę autoryzacji i przypisuje regułę do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="1af68-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="1af68-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="1af68-128">Ponownie wygeneruj klucz reguły autoryzacji dla usługi NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="1af68-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="1af68-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1af68-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="1af68-130">Tworzy przestrzeń nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="1af68-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1af68-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1af68-132">Tworzy regułę autoryzacji i przypisuje regułę do przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="1af68-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="1af68-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="1af68-134">Ponownie wygeneruj klucz reguły autoryzacji dla przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="1af68-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="1af68-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1af68-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="1af68-136">Usuwa istniejące centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="1af68-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1af68-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1af68-138">Usuwa regułę autoryzacji z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="1af68-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1af68-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="1af68-140">Usuwa przestrzeń nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="1af68-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1af68-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1af68-142">Usuwa regułę autoryzacji z przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="1af68-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1af68-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="1af68-144">Ustawia wartości właściwości centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="1af68-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1af68-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1af68-146">Ustawia reguły autoryzacji dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="1af68-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1af68-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="1af68-148">Ustawia wartości właściwości przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="1af68-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1af68-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1af68-150">Ustawia reguły autoryzacji dla przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1af68-150">Sets authorization rules for a notification hub namespace.</span></span>

