---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504352"
---
# <span data-ttu-id="a5e95-101">AZ. NotificationHubs, moduł</span><span class="sxs-lookup"><span data-stu-id="a5e95-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="a5e95-102">Opis</span><span class="sxs-lookup"><span data-stu-id="a5e95-102">Description</span></span>
<span data-ttu-id="a5e95-103">W tym temacie są wyświetlane tematy pomocy dotyczące apletów poleceń centrum powiadomień platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e95-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="a5e95-104">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy (systemy iOS, Android, Windows Phone 8, Sklep Windows itd.) używanych przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="a5e95-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="a5e95-105">Te koncentratory są w przybliżeniu równoważne z poszczególnymi aplikacjami: każdy z Twoich aplikacji zazwyczaj ma własny centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="a5e95-106">Centra powiadomień są zorganizowane w kontenerach logicznych znanych jako przestrzenie nazw, a reguły autoryzacji podpisu dostępu współdzielonego (SAS) są używane do zarządzania dostępem do koncentratorów i obszarów nazw.</span><span class="sxs-lookup"><span data-stu-id="a5e95-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="a5e95-107">Wszystkie te elementy można administrować za pomocą poleceń cmdlet centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="a5e95-108">AZ. NotificationHubs polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="a5e95-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="a5e95-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a5e95-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="a5e95-110">Pobiera informacje o koncentratorach powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="a5e95-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5e95-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="a5e95-112">Pobiera informacje o regułach autoryzacji skojarzonych z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="a5e95-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="a5e95-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="a5e95-114">Pobiera parametry połączenia podstawowego i pomocniczego skojarzone z regułą autoryzacji centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="a5e95-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="a5e95-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="a5e95-116">Pobiera poświadczenia PNS dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="a5e95-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a5e95-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="a5e95-118">Pobiera informacje o obszarze nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="a5e95-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5e95-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="a5e95-120">Pobiera informacje o regułach autoryzacji skojarzonych z obszarem nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="a5e95-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="a5e95-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="a5e95-122">Pobiera parametry połączenia podstawowego i pomocniczego skojarzone z regułą autoryzacji obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="a5e95-123">Nowe — AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a5e95-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="a5e95-124">Tworzy centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="a5e95-125">Nowe — AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5e95-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="a5e95-126">Powoduje utworzenie reguły autoryzacji i przypisanie jej do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="a5e95-127">Nowe — AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="a5e95-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="a5e95-128">Ponowne generowanie klucza reguły autoryzacji dla NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="a5e95-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="a5e95-129">Nowe — AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a5e95-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="a5e95-130">Tworzy obszar nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="a5e95-131">Nowe — AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5e95-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="a5e95-132">Tworzy regułę autoryzacji i przypisuje tę regułę do obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="a5e95-133">Nowe — AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="a5e95-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="a5e95-134">Ponowne generowanie klucza reguły autoryzacji dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a5e95-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="a5e95-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a5e95-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="a5e95-136">Usuwa istniejącego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="a5e95-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5e95-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="a5e95-138">Usuwa regułę autoryzacji z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="a5e95-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a5e95-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="a5e95-140">Usuwa obszar nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="a5e95-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5e95-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="a5e95-142">Usuwa regułę autoryzacji z obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="a5e95-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a5e95-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="a5e95-144">Ustawia wartości właściwości dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="a5e95-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5e95-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="a5e95-146">Ustawia reguły autoryzacji dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="a5e95-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a5e95-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="a5e95-148">Ustawia wartości właściwości dla obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="a5e95-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5e95-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="a5e95-150">Ustawia reguły autoryzacji obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a5e95-150">Sets authorization rules for a notification hub namespace.</span></span>

