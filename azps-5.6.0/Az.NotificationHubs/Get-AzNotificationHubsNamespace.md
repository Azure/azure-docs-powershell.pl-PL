---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 5a8d38adf8016d8f0a71877aa1717df9f3389c93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951306"
---
# <span data-ttu-id="1c619-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1c619-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="1c619-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c619-102">SYNOPSIS</span></span>
<span data-ttu-id="1c619-103">Pobiera informacje o przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1c619-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="1c619-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1c619-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c619-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1c619-105">DESCRIPTION</span></span>
<span data-ttu-id="1c619-106">**Polecenie cmdlet Get-AzNotificationHubsNamespace** pobiera informacje o przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1c619-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="1c619-107">To polecenie cmdlet umożliwia uzyskanie informacji dla wszystkich przestrzeni nazw, informacji o przestrzeni nazw przypisanych do określonej grupy zasobów; lub na celu zwrócenie informacji o określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="1c619-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="1c619-108">Przestrzenie nazw to kontenery logiczne, które ułatwiają organizowanie centrum powiadomień i zarządzanie nimi.</span><span class="sxs-lookup"><span data-stu-id="1c619-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="1c619-109">Musisz mieć co najmniej jedną przestrzeń nazw centrum powiadomień: wszystkie centra powiadomień muszą być przypisane do przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="1c619-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="1c619-110">Jedna przestrzeń nazw może zawierać wiele koncentratorów, co oznacza, że w organizacji może być potrzebna tylko jedna przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="1c619-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="1c619-111">Możesz jednak mieć także wiele przestrzeni nazw, aby lepiej zorganizować swoje centrum lub nadawać określonym osobom uprawnienia do zarządzania wybranym podzestawem centrów.</span><span class="sxs-lookup"><span data-stu-id="1c619-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="1c619-112">Polecenie **cmdlet Get-AzNotificationHubsNamespace** zwraca podstawowe informacje o samej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="1c619-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="1c619-113">Aby uzyskać informacje na temat reguł autoryzacji skojarzonych z przestrzenią nazw, użyj funkcji Get-AzNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="1c619-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="1c619-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1c619-114">EXAMPLES</span></span>

### <span data-ttu-id="1c619-115">Przykład 1. Uzyskiwanie informacji dla wszystkich przestrzeni nazw centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="1c619-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="1c619-116">To polecenie zwraca informacje dla wszystkich przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1c619-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="1c619-117">Przykład 2. Uzyskiwanie informacji dotyczących przestrzeni nazw pojedynczego centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="1c619-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="1c619-118">To polecenie pobiera informacje dla przestrzeni nazw centrum powiadomień: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="1c619-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="1c619-119">Przykład 3. Uzyskiwanie informacji dla wszystkich centrum powiadomień przypisanych do określonej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="1c619-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="1c619-120">To polecenie pobiera informacje dla wszystkich przestrzeni nazw centrum powiadomień przypisanych do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="1c619-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="1c619-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c619-121">PARAMETERS</span></span>

### <span data-ttu-id="1c619-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c619-122">-DefaultProfile</span></span>
<span data-ttu-id="1c619-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1c619-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c619-124">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="1c619-124">-Namespace</span></span>
<span data-ttu-id="1c619-125">Określa unikatową nazwę przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="1c619-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="1c619-126">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="1c619-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c619-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c619-127">-ResourceGroup</span></span>
<span data-ttu-id="1c619-128">Określa grupę zasobów, do której jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="1c619-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="1c619-129">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c619-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c619-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c619-130">CommonParameters</span></span>
<span data-ttu-id="1c619-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c619-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c619-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c619-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c619-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c619-133">INPUTS</span></span>

### <span data-ttu-id="1c619-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1c619-134">System.String</span></span>

## <span data-ttu-id="1c619-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c619-135">OUTPUTS</span></span>

### <span data-ttu-id="1c619-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1c619-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="1c619-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1c619-137">NOTES</span></span>

## <span data-ttu-id="1c619-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c619-138">RELATED LINKS</span></span>

[<span data-ttu-id="1c619-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1c619-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="1c619-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1c619-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="1c619-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1c619-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="1c619-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1c619-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


