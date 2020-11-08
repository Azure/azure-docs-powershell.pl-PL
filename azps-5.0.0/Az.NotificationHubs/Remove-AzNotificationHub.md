---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225011"
---
# <span data-ttu-id="214cc-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="214cc-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="214cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="214cc-102">SYNOPSIS</span></span>
<span data-ttu-id="214cc-103">Usuwa istniejącego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="214cc-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="214cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="214cc-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="214cc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="214cc-105">DESCRIPTION</span></span>
<span data-ttu-id="214cc-106">Polecenie cmdlet **Remove-AzNotificationHub** Usuwa istniejącego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="214cc-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="214cc-107">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="214cc-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="214cc-108">Platformy obejmują między innymi: iOS, Android, Windows Phone 8 i Windows Store.</span><span class="sxs-lookup"><span data-stu-id="214cc-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="214cc-109">Koncentratory powiadomień są w przybliżeniu równoważne z poszczególnymi aplikacjami: każdy z Twoich aplikacji ma zwykle swój własny centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="214cc-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="214cc-110">Możesz usunąć istniejącego centrum powiadomień za pomocą polecenia cmdlet **Remove-AzNotificationHub** .</span><span class="sxs-lookup"><span data-stu-id="214cc-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="214cc-111">Po usunięciu centrum nie można już używać tego koncentratora w celu wysyłania powiadomień wypychanych do użytkowników.</span><span class="sxs-lookup"><span data-stu-id="214cc-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="214cc-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="214cc-112">EXAMPLES</span></span>

### <span data-ttu-id="214cc-113">Przykład 1: usuwanie centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="214cc-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="214cc-114">To polecenie usuwa centrum powiadomień o nazwie ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="214cc-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="214cc-115">Aby usunąć centrum, należy określić obszar nazw, w którym znajduje się centrum, a także grupę zasobów, do której jest przydzielony koncentrator.</span><span class="sxs-lookup"><span data-stu-id="214cc-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="214cc-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="214cc-116">PARAMETERS</span></span>

### <span data-ttu-id="214cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214cc-117">-DefaultProfile</span></span>
<span data-ttu-id="214cc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="214cc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="214cc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="214cc-119">-Force</span></span>
<span data-ttu-id="214cc-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="214cc-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="214cc-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="214cc-121">-Namespace</span></span>
<span data-ttu-id="214cc-122">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="214cc-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="214cc-123">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="214cc-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="214cc-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="214cc-124">-NotificationHub</span></span>
<span data-ttu-id="214cc-125">Określa centrum powiadomień, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="214cc-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="214cc-126">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="214cc-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="214cc-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="214cc-127">-ResourceGroup</span></span>
<span data-ttu-id="214cc-128">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="214cc-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="214cc-129">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="214cc-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="214cc-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="214cc-130">-Confirm</span></span>
<span data-ttu-id="214cc-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214cc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214cc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214cc-132">-WhatIf</span></span>
<span data-ttu-id="214cc-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214cc-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="214cc-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="214cc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214cc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214cc-135">CommonParameters</span></span>
<span data-ttu-id="214cc-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214cc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214cc-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="214cc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214cc-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="214cc-138">INPUTS</span></span>

### <span data-ttu-id="214cc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="214cc-139">System.String</span></span>

## <span data-ttu-id="214cc-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="214cc-140">OUTPUTS</span></span>

### <span data-ttu-id="214cc-141">System. void</span><span class="sxs-lookup"><span data-stu-id="214cc-141">System.Void</span></span>

## <span data-ttu-id="214cc-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="214cc-142">NOTES</span></span>

## <span data-ttu-id="214cc-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="214cc-143">RELATED LINKS</span></span>

[<span data-ttu-id="214cc-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="214cc-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="214cc-145">Nowe — AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="214cc-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="214cc-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="214cc-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


