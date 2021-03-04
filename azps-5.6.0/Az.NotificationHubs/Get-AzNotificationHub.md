---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: fe2949e5b7eb8c3c5f1261072e755bcbb0b6eb00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951418"
---
# <span data-ttu-id="cc26f-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cc26f-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="cc26f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc26f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc26f-103">Otrzymuje informacje na temat swoich centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cc26f-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="cc26f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cc26f-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc26f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="cc26f-105">DESCRIPTION</span></span>
<span data-ttu-id="cc26f-106">Polecenie **cmdlet Get-AzNotificationHub** pobiera informacje o centrach powiadomień w określonej przestrzeni nazw i przypisuje je do określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc26f-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="cc26f-107">Możesz na przykład uzyskać informacje dla wszystkich centrum powiadomień w przestrzeni nazw ContosoNamespace i przypisać je do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="cc26f-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="cc26f-108">Możesz również użyć parametru *NotificationHub,* aby ograniczyć zwracane dane do informacji o określonym centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cc26f-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="cc26f-109">Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy, takiej jak systemy iOS, Android, Windows Phone 8 i Sklep Windows, używane przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="cc26f-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="cc26f-110">Te centra są mniej więcej równoważne poszczególnym aplikacjom, a każda z nich ma zazwyczaj własne centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cc26f-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="cc26f-111">To polecenie cmdlet pobiera tylko informacje o samym centrum.</span><span class="sxs-lookup"><span data-stu-id="cc26f-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="cc26f-112">Inne polecenia cmdlet, takie jak Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys i Get-AzNotificationHubPNSCredentials, są potrzebne do uzyskania informacji o zasadach autoryzacji centrum, ciągach połączeń i poświadczeniach usługi powiadomień platformy.</span><span class="sxs-lookup"><span data-stu-id="cc26f-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="cc26f-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cc26f-113">EXAMPLES</span></span>

### <span data-ttu-id="cc26f-114">Przykład 1. Uzyskiwanie informacji dla wszystkich centrum powiadomień w określonej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="cc26f-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="cc26f-115">To polecenie pobiera informacje dla wszystkich centrum powiadomień w przestrzeni nazw o nazwie ContosoNamespace, które zostały przypisane do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="cc26f-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="cc26f-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cc26f-116">Example 2</span></span>

<span data-ttu-id="cc26f-117">Otrzymuje informacje na temat swoich centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cc26f-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="cc26f-118">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="cc26f-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="cc26f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc26f-119">PARAMETERS</span></span>

### <span data-ttu-id="cc26f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc26f-120">-DefaultProfile</span></span>
<span data-ttu-id="cc26f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cc26f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc26f-122">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="cc26f-122">-Namespace</span></span>
<span data-ttu-id="cc26f-123">Określa przestrzeń nazw, do której jest przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cc26f-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="cc26f-124">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cc26f-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc26f-125">- NotificationHub</span><span class="sxs-lookup"><span data-stu-id="cc26f-125">-NotificationHub</span></span>
<span data-ttu-id="cc26f-126">Określa nazwę centrum powiadomień, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc26f-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="cc26f-127">Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="cc26f-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc26f-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc26f-128">-ResourceGroup</span></span>
<span data-ttu-id="cc26f-129">Określa grupę zasobów, do której jest przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="cc26f-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="cc26f-130">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc26f-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc26f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc26f-131">CommonParameters</span></span>
<span data-ttu-id="cc26f-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc26f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc26f-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc26f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc26f-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc26f-134">INPUTS</span></span>

### <span data-ttu-id="cc26f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="cc26f-135">System.String</span></span>

## <span data-ttu-id="cc26f-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc26f-136">OUTPUTS</span></span>

### <span data-ttu-id="cc26f-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="cc26f-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="cc26f-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cc26f-138">NOTES</span></span>

## <span data-ttu-id="cc26f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc26f-139">RELATED LINKS</span></span>

[<span data-ttu-id="cc26f-140">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cc26f-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="cc26f-141">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="cc26f-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="cc26f-142">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="cc26f-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="cc26f-143">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cc26f-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="cc26f-144">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cc26f-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="cc26f-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cc26f-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


