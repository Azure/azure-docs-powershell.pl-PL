---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: f58a34c5fb5a7ca108f2f4f55c9322f1f439fbf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872032"
---
# <span data-ttu-id="51473-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="51473-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="51473-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51473-102">SYNOPSIS</span></span>
<span data-ttu-id="51473-103">Pobiera informacje o koncentratorach powiadomień.</span><span class="sxs-lookup"><span data-stu-id="51473-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="51473-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51473-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51473-105">Opis</span><span class="sxs-lookup"><span data-stu-id="51473-105">DESCRIPTION</span></span>
<span data-ttu-id="51473-106">Polecenie cmdlet **Get-AzNotificationHub** pobiera informacje o koncentratorach powiadomień w określonym obszarze nazw i przypisano do określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51473-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="51473-107">Na przykład możesz uzyskać informacje o wszystkich koncentratorach powiadomień w obszarze nazw ContosoNamespace i przypisać je do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="51473-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="51473-108">Możesz też użyć parametru *NotificationHub* , aby ograniczyć zwracane dane do informacji dotyczących określonego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="51473-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="51473-109">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy, takiej jak iOS, Android, Windows Phone 8 i Windows Store, używanych przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="51473-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="51473-110">Te koncentratory są w przybliżeniu równoważne poszczególnym aplikacjom, a każda z Twoich aplikacji zazwyczaj ma własne centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="51473-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="51473-111">To polecenie cmdlet pobiera tylko informacje o koncentratorze.</span><span class="sxs-lookup"><span data-stu-id="51473-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="51473-112">Potrzebne są inne polecenia cmdlet, takie jak Get-AzNotificationHubAuthorizationRules, get-AzNotificationHubListKeys i Get-AzNotificationHubPNSCredentials, aby uzyskać informacje na temat reguł autoryzacji koncentratora, ciągów połączeń i poświadczeń usługi powiadamiania o platformie.</span><span class="sxs-lookup"><span data-stu-id="51473-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="51473-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51473-113">EXAMPLES</span></span>

### <span data-ttu-id="51473-114">Przykład 1: uzyskiwanie informacji o wszystkich koncentratorach powiadomień w określonym obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="51473-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="51473-115">To polecenie pobiera informacje dotyczące wszystkich koncentratorów powiadomień w przestrzeni nazw o nazwie ContosoNamespace, które zostały przypisane do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="51473-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="51473-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51473-116">PARAMETERS</span></span>

### <span data-ttu-id="51473-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51473-117">-DefaultProfile</span></span>
<span data-ttu-id="51473-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="51473-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51473-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="51473-119">-Namespace</span></span>
<span data-ttu-id="51473-120">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="51473-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="51473-121">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="51473-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="51473-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="51473-122">-NotificationHub</span></span>
<span data-ttu-id="51473-123">Określa nazwę centrum powiadomień, które ma być pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51473-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="51473-124">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="51473-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="51473-125">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="51473-125">-ResourceGroup</span></span>
<span data-ttu-id="51473-126">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="51473-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="51473-127">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="51473-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="51473-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51473-128">CommonParameters</span></span>
<span data-ttu-id="51473-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51473-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51473-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51473-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51473-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51473-131">INPUTS</span></span>

### <span data-ttu-id="51473-132">System. String</span><span class="sxs-lookup"><span data-stu-id="51473-132">System.String</span></span>

## <span data-ttu-id="51473-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51473-133">OUTPUTS</span></span>

### <span data-ttu-id="51473-134">Microsoft. Azure. Commands. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="51473-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="51473-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51473-135">NOTES</span></span>

## <span data-ttu-id="51473-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51473-136">RELATED LINKS</span></span>

[<span data-ttu-id="51473-137">Get-AzNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="51473-137">Get-AzNotificationHubAuthorizationRules</span></span>](./Get-AzNotificationHubAuthorizationRules.md)

[<span data-ttu-id="51473-138">Get-AzNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="51473-138">Get-AzNotificationHubListKeys</span></span>](./Get-AzNotificationHubListKeys.md)

[<span data-ttu-id="51473-139">Get-AzNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="51473-139">Get-AzNotificationHubPNSCredentials</span></span>](./Get-AzNotificationHubPNSCredentials.md)

[<span data-ttu-id="51473-140">Nowe — AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="51473-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="51473-141">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="51473-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="51473-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="51473-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


