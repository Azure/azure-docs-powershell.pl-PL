---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223272"
---
# <span data-ttu-id="31ded-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="31ded-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="31ded-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31ded-102">SYNOPSIS</span></span>
<span data-ttu-id="31ded-103">Usuwa obszar nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="31ded-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="31ded-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31ded-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31ded-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31ded-105">DESCRIPTION</span></span>
<span data-ttu-id="31ded-106">Polecenie cmdlet **Remove-AzNotificationHubsNamespace** usuwa obszar nazw centrum powiadomień ze swojego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="31ded-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="31ded-107">Przestrzenie nazw są kontenerami logicznymi, które pomagają organizować Centra powiadomień i zarządzać nimi.</span><span class="sxs-lookup"><span data-stu-id="31ded-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="31ded-108">Polecenie cmdlet **Remove-AzNotificationHubsNamespace** usuwa obszar nazw centrum powiadomień ze swojego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="31ded-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="31ded-109">Po uruchomieniu tego polecenia cmdlet określona przestrzeń nazw zostanie usunięta wraz ze wszystkimi koncentratorami powiadomień skojarzonymi z tym obszarem nazw.</span><span class="sxs-lookup"><span data-stu-id="31ded-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="31ded-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31ded-110">EXAMPLES</span></span>

### <span data-ttu-id="31ded-111">Przykład 1: Usuwanie obszaru nazw centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="31ded-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="31ded-112">To polecenie usuwa obszar nazw o nazwie ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="31ded-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="31ded-113">Musisz określić grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="31ded-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="31ded-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31ded-114">PARAMETERS</span></span>

### <span data-ttu-id="31ded-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ded-115">-DefaultProfile</span></span>
<span data-ttu-id="31ded-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="31ded-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31ded-117">-Force</span><span class="sxs-lookup"><span data-stu-id="31ded-117">-Force</span></span>
<span data-ttu-id="31ded-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="31ded-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="31ded-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="31ded-119">-Namespace</span></span>
<span data-ttu-id="31ded-120">Określa obszar nazw, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31ded-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="31ded-121">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="31ded-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="31ded-122">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="31ded-122">-ResourceGroup</span></span>
<span data-ttu-id="31ded-123">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="31ded-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="31ded-124">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="31ded-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="31ded-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31ded-125">-Confirm</span></span>
<span data-ttu-id="31ded-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31ded-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31ded-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31ded-127">-WhatIf</span></span>
<span data-ttu-id="31ded-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31ded-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31ded-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31ded-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31ded-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ded-130">CommonParameters</span></span>
<span data-ttu-id="31ded-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31ded-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ded-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31ded-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ded-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31ded-133">INPUTS</span></span>

### <span data-ttu-id="31ded-134">System. String</span><span class="sxs-lookup"><span data-stu-id="31ded-134">System.String</span></span>

## <span data-ttu-id="31ded-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31ded-135">OUTPUTS</span></span>

### <span data-ttu-id="31ded-136">System. void</span><span class="sxs-lookup"><span data-stu-id="31ded-136">System.Void</span></span>

## <span data-ttu-id="31ded-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31ded-137">NOTES</span></span>

## <span data-ttu-id="31ded-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31ded-138">RELATED LINKS</span></span>

[<span data-ttu-id="31ded-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="31ded-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="31ded-140">Nowe — AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="31ded-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="31ded-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="31ded-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


