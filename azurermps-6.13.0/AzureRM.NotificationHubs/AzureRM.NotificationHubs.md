---
Module Name: AzureRM.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
ms.openlocfilehash: e9f6fce095bd7ea4c494cf778587c3853f347c38
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93704268"
---
# <span data-ttu-id="855be-101">Moduł AzureRM. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="855be-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="855be-102">Opis</span><span class="sxs-lookup"><span data-stu-id="855be-102">Description</span></span>
<span data-ttu-id="855be-103">W tym temacie są wyświetlane tematy pomocy dotyczące apletów poleceń centrum powiadomień platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="855be-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="855be-104">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy (systemy iOS, Android, Windows Phone 8, Sklep Windows itd.) używanych przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="855be-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="855be-105">Te koncentratory są w przybliżeniu równoważne z poszczególnymi aplikacjami: każdy z Twoich aplikacji zazwyczaj ma własny centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="855be-106">Centra powiadomień są zorganizowane w kontenerach logicznych znanych jako przestrzenie nazw, a reguły autoryzacji podpisu dostępu współdzielonego (SAS) są używane do zarządzania dostępem do koncentratorów i obszarów nazw.</span><span class="sxs-lookup"><span data-stu-id="855be-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="855be-107">Wszystkie te elementy można administrować za pomocą poleceń cmdlet centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="855be-108">Polecenia cmdlet AzureRM. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="855be-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="855be-109">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="855be-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="855be-110">Pobiera informacje o koncentratorach powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="855be-111">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="855be-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="855be-112">Pobiera informacje o regułach autoryzacji skojarzonych z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="855be-113">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="855be-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="855be-114">Pobiera parametry połączenia podstawowego i pomocniczego skojarzone z regułą autoryzacji centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="855be-115">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="855be-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="855be-116">Pobiera poświadczenia PNS dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="855be-117">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="855be-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="855be-118">Pobiera informacje o obszarze nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="855be-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="855be-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="855be-120">Pobiera informacje o regułach autoryzacji skojarzonych z obszarem nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="855be-121">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="855be-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="855be-122">Pobiera parametry połączenia podstawowego i pomocniczego skojarzone z regułą autoryzacji obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="855be-123">Nowe — AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="855be-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="855be-124">Tworzy centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="855be-125">Nowe — AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="855be-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="855be-126">Powoduje utworzenie reguły autoryzacji i przypisanie jej do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="855be-127">Nowe — AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="855be-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="855be-128">Ponowne generowanie klucza reguły autoryzacji dla NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="855be-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="855be-129">Nowe — AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="855be-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="855be-130">Tworzy obszar nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="855be-131">Nowe — AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="855be-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="855be-132">Tworzy regułę autoryzacji i przypisuje tę regułę do obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="855be-133">Nowe — AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="855be-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="855be-134">Ponowne generowanie klucza reguły autoryzacji dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="855be-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="855be-135">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="855be-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="855be-136">Usuwa istniejącego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="855be-137">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="855be-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="855be-138">Usuwa regułę autoryzacji z centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="855be-139">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="855be-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="855be-140">Usuwa obszar nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="855be-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="855be-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="855be-142">Usuwa regułę autoryzacji z obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="855be-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="855be-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="855be-144">Ustawia wartości właściwości dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="855be-145">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="855be-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="855be-146">Ustawia reguły autoryzacji dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="855be-147">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="855be-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="855be-148">Ustawia wartości właściwości dla obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="855be-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="855be-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="855be-150">Ustawia reguły autoryzacji obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="855be-150">Sets authorization rules for a notification hub namespace.</span></span>

