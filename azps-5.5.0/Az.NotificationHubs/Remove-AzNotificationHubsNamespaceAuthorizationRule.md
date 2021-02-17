---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191506"
---
# <span data-ttu-id="44302-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="44302-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="44302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44302-102">SYNOPSIS</span></span>
<span data-ttu-id="44302-103">Usuwa regułę autoryzacji z przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="44302-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="44302-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="44302-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44302-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="44302-105">DESCRIPTION</span></span>
<span data-ttu-id="44302-106">Polecenie **cmdlet Remove-AzNotificationHubsNamespaceAuthorizationRule** usuwa regułę autoryzacji sygnatury dostępu udostępnionego (SAS) z przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="44302-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="44302-107">Reguły autoryzacji zarządzają dostępem do przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="44302-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="44302-108">Robi się to przez utworzenie linków jako URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="44302-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="44302-109">Poziomy uprawnień mogą być następujące:</span><span class="sxs-lookup"><span data-stu-id="44302-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="44302-110">Słuchaj</span><span class="sxs-lookup"><span data-stu-id="44302-110">Listen</span></span>
- <span data-ttu-id="44302-111">Wyślij</span><span class="sxs-lookup"><span data-stu-id="44302-111">Send</span></span>
- <span data-ttu-id="44302-112">Zarządzanie klientami jest kierowane do jednego z tych URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="44302-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="44302-113">Na przykład klient z uprawnieniem Dosłuchiwać jest przekierowywowany do URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="44302-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="44302-114">Usunięcie reguły autoryzacji powoduje również usunięcie odpowiednich uprawnień użytkownika.</span><span class="sxs-lookup"><span data-stu-id="44302-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="44302-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="44302-115">EXAMPLES</span></span>

### <span data-ttu-id="44302-116">Przykład 1. Usuwanie reguły autoryzacji z przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="44302-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="44302-117">To polecenie usuwa regułę autoryzacji o nazwie ListenRule z przestrzeni nazw o nazwie ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="44302-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="44302-118">Po uruchomieniu tego polecenia musisz określić grupę zasobów, do których jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="44302-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="44302-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44302-119">PARAMETERS</span></span>

### <span data-ttu-id="44302-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="44302-120">-AuthorizationRule</span></span>
<span data-ttu-id="44302-121">Określa nazwę reguły uwierzytelniania SAS do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="44302-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="44302-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44302-122">-DefaultProfile</span></span>
<span data-ttu-id="44302-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="44302-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44302-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="44302-124">-Force</span></span>
<span data-ttu-id="44302-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44302-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="44302-126">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="44302-126">-Namespace</span></span>
<span data-ttu-id="44302-127">Określa przestrzeń nazw, do której są przypisane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="44302-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="44302-128">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="44302-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="44302-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="44302-129">-ResourceGroup</span></span>
<span data-ttu-id="44302-130">Określa grupę zasobów, do której jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="44302-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="44302-131">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="44302-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="44302-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44302-132">-Confirm</span></span>
<span data-ttu-id="44302-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44302-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44302-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44302-134">-WhatIf</span></span>
<span data-ttu-id="44302-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44302-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44302-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="44302-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44302-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44302-137">CommonParameters</span></span>
<span data-ttu-id="44302-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44302-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44302-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44302-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44302-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44302-140">INPUTS</span></span>

### <span data-ttu-id="44302-141">System.String</span><span class="sxs-lookup"><span data-stu-id="44302-141">System.String</span></span>

## <span data-ttu-id="44302-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44302-142">OUTPUTS</span></span>

### <span data-ttu-id="44302-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44302-143">System.Boolean</span></span>

## <span data-ttu-id="44302-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="44302-144">NOTES</span></span>

## <span data-ttu-id="44302-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44302-145">RELATED LINKS</span></span>

[<span data-ttu-id="44302-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="44302-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="44302-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="44302-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="44302-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="44302-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


