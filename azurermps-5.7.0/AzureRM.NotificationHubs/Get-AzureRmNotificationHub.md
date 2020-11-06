---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: cfe24ac2900e46a031980886f80bf39b9eee28e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553651"
---
# <span data-ttu-id="e8023-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e8023-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="e8023-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8023-102">SYNOPSIS</span></span>
<span data-ttu-id="e8023-103">Pobiera informacje o koncentratorach powiadomień.</span><span class="sxs-lookup"><span data-stu-id="e8023-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8023-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8023-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8023-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8023-105">DESCRIPTION</span></span>
<span data-ttu-id="e8023-106">Polecenie cmdlet **Get-AzureRmNotificationHub** pobiera informacje o koncentratorach powiadomień w określonym obszarze nazw i przypisano do określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8023-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="e8023-107">Na przykład możesz uzyskać informacje o wszystkich koncentratorach powiadomień w obszarze nazw ContosoNamespace i przypisać je do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="e8023-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>

<span data-ttu-id="e8023-108">Możesz też użyć parametru *NotificationHub* , aby ograniczyć zwracane dane do informacji dotyczących określonego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="e8023-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>

<span data-ttu-id="e8023-109">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy, takiej jak iOS, Android, Windows Phone 8 i Windows Store, używanych przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="e8023-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="e8023-110">Te koncentratory są w przybliżeniu równoważne poszczególnym aplikacjom, a każda z Twoich aplikacji zazwyczaj ma własne centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="e8023-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="e8023-111">To polecenie cmdlet pobiera tylko informacje o koncentratorze.</span><span class="sxs-lookup"><span data-stu-id="e8023-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="e8023-112">Potrzebne są inne polecenia cmdlet, takie jak Get-AzureRmNotificationHubAuthorizationRules, get-AzureRmNotificationHubListKeys i Get-AzureRmNotificationHubPNSCredentials, aby uzyskać informacje na temat reguł autoryzacji koncentratora, ciągów połączeń i poświadczeń usługi powiadamiania o platformie.</span><span class="sxs-lookup"><span data-stu-id="e8023-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="e8023-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8023-113">EXAMPLES</span></span>

### <span data-ttu-id="e8023-114">Przykład 1: uzyskiwanie informacji o wszystkich koncentratorach powiadomień w określonym obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="e8023-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="e8023-115">To polecenie pobiera informacje dotyczące wszystkich koncentratorów powiadomień w przestrzeni nazw o nazwie ContosoNamespace, które zostały przypisane do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="e8023-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="e8023-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8023-116">PARAMETERS</span></span>

### <span data-ttu-id="e8023-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8023-117">-DefaultProfile</span></span>
<span data-ttu-id="e8023-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e8023-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8023-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e8023-119">-Namespace</span></span>
<span data-ttu-id="e8023-120">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="e8023-120">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="e8023-121">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="e8023-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8023-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="e8023-122">-NotificationHub</span></span>
<span data-ttu-id="e8023-123">Określa nazwę centrum powiadomień, które ma być pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8023-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>

<span data-ttu-id="e8023-124">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="e8023-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8023-125">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e8023-125">-ResourceGroup</span></span>
<span data-ttu-id="e8023-126">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="e8023-126">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="e8023-127">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="e8023-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8023-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8023-128">CommonParameters</span></span>
<span data-ttu-id="e8023-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8023-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8023-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8023-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8023-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8023-131">INPUTS</span></span>

### <span data-ttu-id="e8023-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e8023-132">None</span></span>
<span data-ttu-id="e8023-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e8023-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8023-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8023-134">OUTPUTS</span></span>

### <span data-ttu-id="e8023-135">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. NotificationHubs. modele. NotificationHubAttributes]</span><span class="sxs-lookup"><span data-stu-id="e8023-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes]</span></span>

## <span data-ttu-id="e8023-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8023-136">NOTES</span></span>

## <span data-ttu-id="e8023-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8023-137">RELATED LINKS</span></span>

[<span data-ttu-id="e8023-138">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="e8023-138">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="e8023-139">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="e8023-139">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="e8023-140">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="e8023-140">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="e8023-141">Nowe — AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e8023-141">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="e8023-142">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e8023-142">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="e8023-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="e8023-143">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


