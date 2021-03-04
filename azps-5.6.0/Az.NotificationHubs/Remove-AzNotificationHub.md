---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: b7932eb4f5d68986033243bc3e5e5161861a0bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951153"
---
# <span data-ttu-id="3c9da-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3c9da-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="3c9da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c9da-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9da-103">Usuwa istniejące centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3c9da-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="3c9da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3c9da-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c9da-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3c9da-105">DESCRIPTION</span></span>
<span data-ttu-id="3c9da-106">Polecenie **cmdlet Remove-AzNotificationHub** usuwa istniejące centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3c9da-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="3c9da-107">Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="3c9da-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="3c9da-108">Platformy obejmują między innymi: systemy iOS, Android, Windows Phone 8 i Sklep Windows.</span><span class="sxs-lookup"><span data-stu-id="3c9da-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="3c9da-109">Centra powiadomień są mniej więcej równoważne poszczególnym aplikacjom: każda z Twoich aplikacji zazwyczaj ma własne centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3c9da-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="3c9da-110">Istniejące centrum powiadomień można usunąć za pomocą polecenia cmdlet **Remove-AzNotificationHub.**</span><span class="sxs-lookup"><span data-stu-id="3c9da-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="3c9da-111">Po usunięciu centrum nie można go już używać do wysyłania powiadomień wypychanych do użytkowników.</span><span class="sxs-lookup"><span data-stu-id="3c9da-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="3c9da-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3c9da-112">EXAMPLES</span></span>

### <span data-ttu-id="3c9da-113">Przykład 1. Usuwanie centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="3c9da-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="3c9da-114">To polecenie usuwa centrum powiadomień o nazwie ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="3c9da-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="3c9da-115">Aby usunąć centrum, musisz określić przestrzeń nazw, w której znajduje się centrum, oraz grupę zasobów, do której centrum jest przypisane.</span><span class="sxs-lookup"><span data-stu-id="3c9da-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="3c9da-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c9da-116">PARAMETERS</span></span>

### <span data-ttu-id="3c9da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9da-117">-DefaultProfile</span></span>
<span data-ttu-id="3c9da-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3c9da-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c9da-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="3c9da-119">-Force</span></span>
<span data-ttu-id="3c9da-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3c9da-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3c9da-121">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="3c9da-121">-Namespace</span></span>
<span data-ttu-id="3c9da-122">Określa przestrzeń nazw, do której jest przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3c9da-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="3c9da-123">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3c9da-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3c9da-124">- NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3c9da-124">-NotificationHub</span></span>
<span data-ttu-id="3c9da-125">Określa centrum powiadomień do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="3c9da-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="3c9da-126">Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="3c9da-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="3c9da-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3c9da-127">-ResourceGroup</span></span>
<span data-ttu-id="3c9da-128">Określa grupę zasobów, do której jest przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3c9da-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="3c9da-129">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c9da-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3c9da-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c9da-130">-Confirm</span></span>
<span data-ttu-id="3c9da-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3c9da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c9da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c9da-132">-WhatIf</span></span>
<span data-ttu-id="3c9da-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c9da-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c9da-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3c9da-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c9da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9da-135">CommonParameters</span></span>
<span data-ttu-id="3c9da-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c9da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9da-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c9da-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9da-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c9da-138">INPUTS</span></span>

### <span data-ttu-id="3c9da-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3c9da-139">System.String</span></span>

## <span data-ttu-id="3c9da-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c9da-140">OUTPUTS</span></span>

### <span data-ttu-id="3c9da-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="3c9da-141">System.Void</span></span>

## <span data-ttu-id="3c9da-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3c9da-142">NOTES</span></span>

## <span data-ttu-id="3c9da-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c9da-143">RELATED LINKS</span></span>

[<span data-ttu-id="3c9da-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3c9da-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="3c9da-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3c9da-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="3c9da-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3c9da-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


