---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a1c9743d02f10102d9343709599dbed694d37a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951297"
---
# <span data-ttu-id="f27cc-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f27cc-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="f27cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f27cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f27cc-103">Pobiera informacje o zasadach autoryzacji skojarzonych z przestrzenią nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f27cc-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="f27cc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f27cc-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f27cc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f27cc-105">DESCRIPTION</span></span>
<span data-ttu-id="f27cc-106">Polecenie **cmdlet Get-AzNotificationHubsNamespaceAuthorizationRule** zwraca informacje o zasadach autoryzacji podpisu dostępu udostępnionego (SAS) skojarzonych z przestrzenią nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f27cc-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="f27cc-107">Możesz zwrócić informacje o wszystkich regułach skojarzonych z przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="f27cc-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="f27cc-108">Ewentualnie, uwzględniając parametr *AuthorizationRule,* możesz zwrócić informacje dotyczące określonej reguły.</span><span class="sxs-lookup"><span data-stu-id="f27cc-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="f27cc-109">Reguły autoryzacji zarządzają dostępem do przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f27cc-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="f27cc-110">Jest to wykonywane przez utworzenie linków jako URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="f27cc-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="f27cc-111">Poziomy platformy mogą być następujące:</span><span class="sxs-lookup"><span data-stu-id="f27cc-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="f27cc-112">Słuchaj</span><span class="sxs-lookup"><span data-stu-id="f27cc-112">Listen</span></span>
- <span data-ttu-id="f27cc-113">Wyślij</span><span class="sxs-lookup"><span data-stu-id="f27cc-113">Send</span></span>
- <span data-ttu-id="f27cc-114">Zarządzanie klientami jest kierowane do jednego z tych URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="f27cc-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="f27cc-115">Na przykład klient, który otrzymał uprawnienie Posłuchaj, zostanie przekierowyowany do URI dla tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="f27cc-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="f27cc-116">To polecenie cmdlet pobiera tylko reguły autoryzacji skojarzone z przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="f27cc-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="f27cc-117">Aby uzyskać informacje o samej przestrzeni nazw, użyj funkcji Get-AzNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="f27cc-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="f27cc-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f27cc-118">EXAMPLES</span></span>

### <span data-ttu-id="f27cc-119">Przykład 1. Uzyskiwanie informacji na temat wszystkich reguł autoryzacji przypisanych do przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="f27cc-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="f27cc-120">To polecenie pobiera informacje na temat wszystkich reguł autoryzacji przypisanych zarówno do grupy zasobów ContosoNamespace przestrzeni nazw, jak i grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="f27cc-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="f27cc-121">Przykład 2. Uzyskiwanie informacji o regułzie autoryzacji</span><span class="sxs-lookup"><span data-stu-id="f27cc-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f27cc-122">To polecenie pobiera informacje na temat jednej reguły autoryzacji przestrzeni nazw o nazwie ListenRule.</span><span class="sxs-lookup"><span data-stu-id="f27cc-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="f27cc-123">Aby uzyskać informacje dotyczące określonej reguły autoryzacji, musisz dołączyć przestrzeń nazw i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="f27cc-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="f27cc-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f27cc-124">PARAMETERS</span></span>

### <span data-ttu-id="f27cc-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f27cc-125">-AuthorizationRule</span></span>
<span data-ttu-id="f27cc-126">Określa nazwę reguły uwierzytelniania SAS.</span><span class="sxs-lookup"><span data-stu-id="f27cc-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="f27cc-127">Te reguły określają typ dostępu, jaki użytkownicy mają do przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f27cc-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="f27cc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27cc-128">-DefaultProfile</span></span>
<span data-ttu-id="f27cc-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f27cc-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f27cc-130">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="f27cc-130">-Namespace</span></span>
<span data-ttu-id="f27cc-131">Określa przestrzeń nazw, do której są przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="f27cc-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="f27cc-132">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f27cc-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f27cc-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f27cc-133">-ResourceGroup</span></span>
<span data-ttu-id="f27cc-134">Określa grupę zasobów, do której są przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="f27cc-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="f27cc-135">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f27cc-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f27cc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27cc-136">CommonParameters</span></span>
<span data-ttu-id="f27cc-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f27cc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27cc-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f27cc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27cc-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f27cc-139">INPUTS</span></span>

### <span data-ttu-id="f27cc-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f27cc-140">System.String</span></span>

## <span data-ttu-id="f27cc-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f27cc-141">OUTPUTS</span></span>

### <span data-ttu-id="f27cc-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f27cc-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f27cc-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f27cc-143">NOTES</span></span>

## <span data-ttu-id="f27cc-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f27cc-144">RELATED LINKS</span></span>

[<span data-ttu-id="f27cc-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f27cc-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="f27cc-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f27cc-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="f27cc-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f27cc-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="f27cc-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f27cc-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


