---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191515"
---
# <span data-ttu-id="36484-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="36484-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="36484-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36484-102">SYNOPSIS</span></span>
<span data-ttu-id="36484-103">Usuwa przestrzeń nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="36484-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="36484-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36484-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36484-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="36484-105">DESCRIPTION</span></span>
<span data-ttu-id="36484-106">Polecenie **cmdlet Remove-AzNotificationHubsNamespace** usuwa przestrzeń nazw centrum powiadomień z wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="36484-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="36484-107">Przestrzenie nazw to kontenery logiczne, które ułatwiają organizowanie centrum powiadomień i zarządzanie nimi.</span><span class="sxs-lookup"><span data-stu-id="36484-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="36484-108">Polecenie **cmdlet Remove-AzNotificationHubsNamespace** usuwa przestrzeń nazw centrum powiadomień z wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="36484-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="36484-109">Po uruchomieniu tego polecenia cmdlet określona przestrzeń nazw zostanie usunięta wraz ze wszystkimi centrami powiadomień skojarzonymi z tą przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="36484-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="36484-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36484-110">EXAMPLES</span></span>

### <span data-ttu-id="36484-111">Przykład 1. Usuwanie przestrzeni nazw centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="36484-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="36484-112">To polecenie usuwa przestrzeń nazw o nazwie ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="36484-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="36484-113">Należy określić grupę zasobów, do których jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="36484-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="36484-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36484-114">PARAMETERS</span></span>

### <span data-ttu-id="36484-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36484-115">-DefaultProfile</span></span>
<span data-ttu-id="36484-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="36484-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36484-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="36484-117">-Force</span></span>
<span data-ttu-id="36484-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36484-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="36484-119">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="36484-119">-Namespace</span></span>
<span data-ttu-id="36484-120">Określa przestrzeń nazw, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36484-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="36484-121">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="36484-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="36484-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36484-122">-ResourceGroup</span></span>
<span data-ttu-id="36484-123">Określa grupę zasobów, do której jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="36484-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="36484-124">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="36484-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="36484-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36484-125">-Confirm</span></span>
<span data-ttu-id="36484-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36484-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36484-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36484-127">-WhatIf</span></span>
<span data-ttu-id="36484-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36484-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36484-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="36484-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36484-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36484-130">CommonParameters</span></span>
<span data-ttu-id="36484-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36484-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36484-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36484-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36484-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36484-133">INPUTS</span></span>

### <span data-ttu-id="36484-134">System.String</span><span class="sxs-lookup"><span data-stu-id="36484-134">System.String</span></span>

## <span data-ttu-id="36484-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36484-135">OUTPUTS</span></span>

### <span data-ttu-id="36484-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="36484-136">System.Void</span></span>

## <span data-ttu-id="36484-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36484-137">NOTES</span></span>

## <span data-ttu-id="36484-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36484-138">RELATED LINKS</span></span>

[<span data-ttu-id="36484-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="36484-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="36484-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="36484-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="36484-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="36484-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


