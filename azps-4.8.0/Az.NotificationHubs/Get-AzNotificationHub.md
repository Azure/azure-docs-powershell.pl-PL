---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: d270e3020e03a02461d9c54e19458af10401ee79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223273"
---
# <span data-ttu-id="723d2-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="723d2-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="723d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="723d2-102">SYNOPSIS</span></span>
<span data-ttu-id="723d2-103">Pobiera informacje o koncentratorach powiadomień.</span><span class="sxs-lookup"><span data-stu-id="723d2-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="723d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="723d2-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="723d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="723d2-105">DESCRIPTION</span></span>
<span data-ttu-id="723d2-106">Polecenie cmdlet **Get-AzNotificationHub** pobiera informacje o koncentratorach powiadomień w określonym obszarze nazw i przypisano do określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="723d2-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="723d2-107">Na przykład możesz uzyskać informacje o wszystkich koncentratorach powiadomień w obszarze nazw ContosoNamespace i przypisać je do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="723d2-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="723d2-108">Możesz też użyć parametru *NotificationHub* , aby ograniczyć zwracane dane do informacji dotyczących określonego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="723d2-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="723d2-109">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy, takiej jak iOS, Android, Windows Phone 8 i Windows Store, używanych przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="723d2-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="723d2-110">Te koncentratory są w przybliżeniu równoważne poszczególnym aplikacjom, a każda z Twoich aplikacji zazwyczaj ma własne centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="723d2-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="723d2-111">To polecenie cmdlet pobiera tylko informacje o koncentratorze.</span><span class="sxs-lookup"><span data-stu-id="723d2-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="723d2-112">Potrzebne są inne polecenia cmdlet, takie jak Get-AzNotificationHubAuthorizationRules, get-AzNotificationHubListKeys i Get-AzNotificationHubPNSCredentials, aby uzyskać informacje na temat reguł autoryzacji koncentratora, ciągów połączeń i poświadczeń usługi powiadamiania o platformie.</span><span class="sxs-lookup"><span data-stu-id="723d2-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="723d2-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="723d2-113">EXAMPLES</span></span>

### <span data-ttu-id="723d2-114">Przykład 1: uzyskiwanie informacji o wszystkich koncentratorach powiadomień w określonym obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="723d2-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="723d2-115">To polecenie pobiera informacje dotyczące wszystkich koncentratorów powiadomień w przestrzeni nazw o nazwie ContosoNamespace, które zostały przypisane do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="723d2-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="723d2-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="723d2-116">PARAMETERS</span></span>

### <span data-ttu-id="723d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723d2-117">-DefaultProfile</span></span>
<span data-ttu-id="723d2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="723d2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="723d2-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="723d2-119">-Namespace</span></span>
<span data-ttu-id="723d2-120">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="723d2-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="723d2-121">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="723d2-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="723d2-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="723d2-122">-NotificationHub</span></span>
<span data-ttu-id="723d2-123">Określa nazwę centrum powiadomień, które ma być pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="723d2-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="723d2-124">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="723d2-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="723d2-125">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="723d2-125">-ResourceGroup</span></span>
<span data-ttu-id="723d2-126">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="723d2-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="723d2-127">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="723d2-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="723d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723d2-128">CommonParameters</span></span>
<span data-ttu-id="723d2-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="723d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723d2-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="723d2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723d2-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="723d2-131">INPUTS</span></span>

### <span data-ttu-id="723d2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="723d2-132">System.String</span></span>

## <span data-ttu-id="723d2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="723d2-133">OUTPUTS</span></span>

### <span data-ttu-id="723d2-134">Microsoft. Azure. Commands. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="723d2-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="723d2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="723d2-135">NOTES</span></span>

## <span data-ttu-id="723d2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="723d2-136">RELATED LINKS</span></span>

[<span data-ttu-id="723d2-137">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="723d2-137">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="723d2-138">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="723d2-138">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="723d2-139">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="723d2-139">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="723d2-140">Nowe — AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="723d2-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="723d2-141">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="723d2-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="723d2-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="723d2-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


