---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240491"
---
# <span data-ttu-id="d2aaa-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d2aaa-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="d2aaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="d2aaa-103">Pobiera informacje o zasadach autoryzacji skojarzonych z przestrzenią nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="d2aaa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2aaa-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2aaa-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2aaa-105">DESCRIPTION</span></span>
<span data-ttu-id="d2aaa-106">Polecenie **cmdlet Get-AzNotificationHubsNamespaceAuthorizationRule** zwraca informacje o zasadach autoryzacji podpisu dostępu udostępnionego (SAS) skojarzonych z przestrzenią nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="d2aaa-107">Możesz zwrócić informacje o wszystkich regułach skojarzonych z przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="d2aaa-108">Ewentualnie, uwzględniając parametr *AuthorizationRule,* możesz zwrócić informacje dotyczące określonej reguły.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="d2aaa-109">Reguły autoryzacji zarządzają dostępem do przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="d2aaa-110">Jest to wykonywane przez utworzenie linków jako URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="d2aaa-111">Poziomy platformy mogą być następujące:</span><span class="sxs-lookup"><span data-stu-id="d2aaa-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="d2aaa-112">Słuchaj</span><span class="sxs-lookup"><span data-stu-id="d2aaa-112">Listen</span></span>
- <span data-ttu-id="d2aaa-113">Wyślij</span><span class="sxs-lookup"><span data-stu-id="d2aaa-113">Send</span></span>
- <span data-ttu-id="d2aaa-114">Zarządzanie klientami jest kierowane do jednego z tych URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="d2aaa-115">Na przykład klient, który otrzymał uprawnienie Posłuchaj, zostanie przekierowyowany do URI dla tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="d2aaa-116">To polecenie cmdlet pobiera tylko reguły autoryzacji skojarzone z przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="d2aaa-117">Aby uzyskać informacje o samej przestrzeni nazw, użyj funkcji Get-AzNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="d2aaa-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2aaa-118">EXAMPLES</span></span>

### <span data-ttu-id="d2aaa-119">Przykład 1. Uzyskiwanie informacji na temat wszystkich reguł autoryzacji przypisanych do przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="d2aaa-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="d2aaa-120">To polecenie pobiera informacje na temat wszystkich reguł autoryzacji przypisanych zarówno do grupy zasobów ContosoNamespace przestrzeni nazw, jak i grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="d2aaa-121">Przykład 2. Uzyskiwanie informacji o regułzie autoryzacji</span><span class="sxs-lookup"><span data-stu-id="d2aaa-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="d2aaa-122">To polecenie pobiera informacje na temat jednej reguły autoryzacji przestrzeni nazw o nazwie ListenRule.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="d2aaa-123">Aby uzyskać informacje dotyczące określonej reguły autoryzacji, musisz dołączyć przestrzeń nazw i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="d2aaa-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2aaa-124">PARAMETERS</span></span>

### <span data-ttu-id="d2aaa-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d2aaa-125">-AuthorizationRule</span></span>
<span data-ttu-id="d2aaa-126">Określa nazwę reguły uwierzytelniania SAS.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="d2aaa-127">Te reguły określają typ dostępu, jaki użytkownicy mają do przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="d2aaa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2aaa-128">-DefaultProfile</span></span>
<span data-ttu-id="d2aaa-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d2aaa-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2aaa-130">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="d2aaa-130">-Namespace</span></span>
<span data-ttu-id="d2aaa-131">Określa przestrzeń nazw, do której są przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="d2aaa-132">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d2aaa-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d2aaa-133">-ResourceGroup</span></span>
<span data-ttu-id="d2aaa-134">Określa grupę zasobów, do której są przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="d2aaa-135">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d2aaa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2aaa-136">CommonParameters</span></span>
<span data-ttu-id="d2aaa-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2aaa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2aaa-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2aaa-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2aaa-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2aaa-139">INPUTS</span></span>

### <span data-ttu-id="d2aaa-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d2aaa-140">System.String</span></span>

## <span data-ttu-id="d2aaa-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2aaa-141">OUTPUTS</span></span>

### <span data-ttu-id="d2aaa-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d2aaa-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d2aaa-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2aaa-143">NOTES</span></span>

## <span data-ttu-id="d2aaa-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2aaa-144">RELATED LINKS</span></span>

[<span data-ttu-id="d2aaa-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d2aaa-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d2aaa-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d2aaa-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d2aaa-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d2aaa-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="d2aaa-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d2aaa-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


