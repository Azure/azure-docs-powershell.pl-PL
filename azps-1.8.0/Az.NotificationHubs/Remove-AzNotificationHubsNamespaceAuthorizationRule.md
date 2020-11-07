---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 1d400cd9cd9d9201db77ba5bab36cf80238e9979
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708849"
---
# <span data-ttu-id="fbacd-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fbacd-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="fbacd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbacd-102">SYNOPSIS</span></span>
<span data-ttu-id="fbacd-103">Usuwa regułę autoryzacji z obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fbacd-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="fbacd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbacd-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbacd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbacd-105">DESCRIPTION</span></span>
<span data-ttu-id="fbacd-106">Polecenie cmdlet **Remove-AzNotificationHubsNamespaceAuthorizationRule** usuwa regułę autoryzacji współużytkowanego podpisu dostępu (SAS) z obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fbacd-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="fbacd-107">Reguły autoryzacji zarządzają dostępem do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="fbacd-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="fbacd-108">Odbywa się to za pomocą tworzenia linków, takich jak identyfikatory URI, na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="fbacd-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="fbacd-109">Poziomy uprawnień mogą być następujące:</span><span class="sxs-lookup"><span data-stu-id="fbacd-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="fbacd-110">Słuch</span><span class="sxs-lookup"><span data-stu-id="fbacd-110">Listen</span></span>
- <span data-ttu-id="fbacd-111">Wyślij</span><span class="sxs-lookup"><span data-stu-id="fbacd-111">Send</span></span>
- <span data-ttu-id="fbacd-112">Zarządzanie klientami jest przekierowywane do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="fbacd-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="fbacd-113">Na przykład klient, który udzielił uprawnień do odsłuchiwania, jest kierowany na identyfikator URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="fbacd-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="fbacd-114">Usunięcie reguły autoryzacji powoduje również usunięcie odpowiednich uprawnień użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fbacd-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="fbacd-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbacd-115">EXAMPLES</span></span>

### <span data-ttu-id="fbacd-116">Przykład 1: Usuwanie reguły autoryzacji z obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="fbacd-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="fbacd-117">To polecenie usuwa regułę autoryzacji o nazwie ListenRule z obszaru nazw o nazwie ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="fbacd-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="fbacd-118">Po uruchomieniu tego polecenia musisz określić grupę zasobów, do której jest przypisany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="fbacd-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="fbacd-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbacd-119">PARAMETERS</span></span>

### <span data-ttu-id="fbacd-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fbacd-120">-AuthorizationRule</span></span>
<span data-ttu-id="fbacd-121">Określa nazwę reguły uwierzytelniania SAS do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="fbacd-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="fbacd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbacd-122">-DefaultProfile</span></span>
<span data-ttu-id="fbacd-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fbacd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbacd-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fbacd-124">-Force</span></span>
<span data-ttu-id="fbacd-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fbacd-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fbacd-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fbacd-126">-Namespace</span></span>
<span data-ttu-id="fbacd-127">Określa obszar nazw, do którego są przypisywane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="fbacd-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="fbacd-128">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fbacd-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="fbacd-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fbacd-129">-ResourceGroup</span></span>
<span data-ttu-id="fbacd-130">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="fbacd-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="fbacd-131">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="fbacd-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="fbacd-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbacd-132">-Confirm</span></span>
<span data-ttu-id="fbacd-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbacd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbacd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbacd-134">-WhatIf</span></span>
<span data-ttu-id="fbacd-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbacd-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbacd-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fbacd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbacd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbacd-137">CommonParameters</span></span>
<span data-ttu-id="fbacd-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbacd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbacd-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbacd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbacd-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbacd-140">INPUTS</span></span>

### <span data-ttu-id="fbacd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fbacd-141">System.String</span></span>

## <span data-ttu-id="fbacd-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbacd-142">OUTPUTS</span></span>

### <span data-ttu-id="fbacd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fbacd-143">System.Boolean</span></span>

## <span data-ttu-id="fbacd-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbacd-144">NOTES</span></span>

## <span data-ttu-id="fbacd-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbacd-145">RELATED LINKS</span></span>

[<span data-ttu-id="fbacd-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fbacd-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="fbacd-147">Nowe — AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fbacd-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="fbacd-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fbacd-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)

