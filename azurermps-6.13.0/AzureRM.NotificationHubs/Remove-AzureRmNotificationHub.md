---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: f4dc14fd922852fa67085588c78847623eb5eb64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544983"
---
# <span data-ttu-id="36374-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="36374-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="36374-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36374-102">SYNOPSIS</span></span>
<span data-ttu-id="36374-103">Usuwa istniejącego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="36374-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36374-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36374-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36374-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36374-105">DESCRIPTION</span></span>
<span data-ttu-id="36374-106">Polecenie cmdlet **Remove-AzureRmNotificationHub** Usuwa istniejącego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="36374-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="36374-107">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="36374-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="36374-108">Platformy obejmują między innymi: iOS, Android, Windows Phone 8 i Windows Store.</span><span class="sxs-lookup"><span data-stu-id="36374-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="36374-109">Koncentratory powiadomień są w przybliżeniu równoważne z poszczególnymi aplikacjami: każdy z Twoich aplikacji ma zwykle swój własny centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="36374-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="36374-110">Możesz usunąć istniejącego centrum powiadomień za pomocą polecenia cmdlet **Remove-AzureRmNotificationHub** .</span><span class="sxs-lookup"><span data-stu-id="36374-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="36374-111">Po usunięciu centrum nie można już używać tego koncentratora w celu wysyłania powiadomień wypychanych do użytkowników.</span><span class="sxs-lookup"><span data-stu-id="36374-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="36374-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36374-112">EXAMPLES</span></span>

### <span data-ttu-id="36374-113">Przykład 1: usuwanie centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="36374-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="36374-114">To polecenie usuwa centrum powiadomień o nazwie ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="36374-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="36374-115">Aby usunąć centrum, należy określić obszar nazw, w którym znajduje się centrum, a także grupę zasobów, do której jest przydzielony koncentrator.</span><span class="sxs-lookup"><span data-stu-id="36374-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="36374-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36374-116">PARAMETERS</span></span>

### <span data-ttu-id="36374-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36374-117">-DefaultProfile</span></span>
<span data-ttu-id="36374-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="36374-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36374-119">-Force</span><span class="sxs-lookup"><span data-stu-id="36374-119">-Force</span></span>
<span data-ttu-id="36374-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36374-120">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36374-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="36374-121">-Namespace</span></span>
<span data-ttu-id="36374-122">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="36374-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="36374-123">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="36374-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="36374-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="36374-124">-NotificationHub</span></span>
<span data-ttu-id="36374-125">Określa centrum powiadomień, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="36374-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="36374-126">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="36374-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36374-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="36374-127">-ResourceGroup</span></span>
<span data-ttu-id="36374-128">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="36374-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="36374-129">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="36374-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="36374-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36374-130">-Confirm</span></span>
<span data-ttu-id="36374-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36374-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36374-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36374-132">-WhatIf</span></span>
<span data-ttu-id="36374-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36374-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36374-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36374-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36374-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36374-135">CommonParameters</span></span>
<span data-ttu-id="36374-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36374-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36374-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36374-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36374-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36374-138">INPUTS</span></span>

### <span data-ttu-id="36374-139">System. String</span><span class="sxs-lookup"><span data-stu-id="36374-139">System.String</span></span>

## <span data-ttu-id="36374-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36374-140">OUTPUTS</span></span>

### <span data-ttu-id="36374-141">System. void</span><span class="sxs-lookup"><span data-stu-id="36374-141">System.Void</span></span>

## <span data-ttu-id="36374-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36374-142">NOTES</span></span>

## <span data-ttu-id="36374-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36374-143">RELATED LINKS</span></span>

[<span data-ttu-id="36374-144">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="36374-144">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="36374-145">Nowe — AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="36374-145">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="36374-146">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="36374-146">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


