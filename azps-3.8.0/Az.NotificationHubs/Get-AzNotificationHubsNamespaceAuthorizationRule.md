---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895486"
---
# <span data-ttu-id="c3cac-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c3cac-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="c3cac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3cac-102">SYNOPSIS</span></span>
<span data-ttu-id="c3cac-103">Pobiera informacje o regułach autoryzacji skojarzonych z obszarem nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c3cac-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="c3cac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3cac-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3cac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3cac-105">DESCRIPTION</span></span>
<span data-ttu-id="c3cac-106">Polecenie cmdlet **Get-AzNotificationHubsNamespaceAuthorizationRule** zwraca informacje o regułach autoryzacji związanych z dostępem do funkcji podpisów udostępnionych (SAS) skojarzonych z obszarem nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c3cac-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="c3cac-107">Możesz zwrócić informacje dotyczące wszystkich reguł skojarzonych z obszarem nazw.</span><span class="sxs-lookup"><span data-stu-id="c3cac-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="c3cac-108">Możesz również zwrócić informacje dotyczące konkretnej reguły, a także podając parametr *AuthorizationRule* .</span><span class="sxs-lookup"><span data-stu-id="c3cac-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="c3cac-109">Reguły autoryzacji zarządzają dostępem do obszarów nazw.</span><span class="sxs-lookup"><span data-stu-id="c3cac-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="c3cac-110">Służą do tego tworzenie linków jako identyfikatorów URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="c3cac-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="c3cac-111">Może to być jedna z następujących poziomów platformy:</span><span class="sxs-lookup"><span data-stu-id="c3cac-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="c3cac-112">Słuch</span><span class="sxs-lookup"><span data-stu-id="c3cac-112">Listen</span></span>
- <span data-ttu-id="c3cac-113">Wyślij</span><span class="sxs-lookup"><span data-stu-id="c3cac-113">Send</span></span>
- <span data-ttu-id="c3cac-114">Zarządzanie klientami jest przekierowywane do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="c3cac-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="c3cac-115">Na przykład klient, któremu nadano uprawnienie do odsłuchiwania, będzie kierowany na identyfikator URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="c3cac-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="c3cac-116">To polecenie cmdlet pobiera tylko reguły autoryzacji skojarzone z obszarem nazw.</span><span class="sxs-lookup"><span data-stu-id="c3cac-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="c3cac-117">Aby uzyskać informacje na temat samego obszaru nazw, użyj polecenie Get-AzNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="c3cac-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="c3cac-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3cac-118">EXAMPLES</span></span>

### <span data-ttu-id="c3cac-119">Przykład 1: uzyskiwanie informacji o wszystkich regułach autoryzacji przypisanych do obszarów nazw</span><span class="sxs-lookup"><span data-stu-id="c3cac-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="c3cac-120">To polecenie pobiera informacje o wszystkich regułach autoryzacji przypisanych zarówno do obszaru nazw ContosoNamespace, jak i grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="c3cac-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="c3cac-121">Przykład 2: uzyskiwanie informacji na temat reguły autoryzacji</span><span class="sxs-lookup"><span data-stu-id="c3cac-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="c3cac-122">To polecenie pobiera informacje na temat jednej reguły autoryzacji obszaru nazw o nazwie ListenRule.</span><span class="sxs-lookup"><span data-stu-id="c3cac-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="c3cac-123">Aby uzyskać informacje dotyczące określonej reguły autoryzacji, należy uwzględnić obszar nazw i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="c3cac-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="c3cac-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3cac-124">PARAMETERS</span></span>

### <span data-ttu-id="c3cac-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c3cac-125">-AuthorizationRule</span></span>
<span data-ttu-id="c3cac-126">Określa nazwę reguły uwierzytelniania SAS.</span><span class="sxs-lookup"><span data-stu-id="c3cac-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="c3cac-127">Te reguły określają typ dostępu do obszaru nazw użytkownikom.</span><span class="sxs-lookup"><span data-stu-id="c3cac-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="c3cac-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3cac-128">-DefaultProfile</span></span>
<span data-ttu-id="c3cac-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c3cac-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3cac-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c3cac-130">-Namespace</span></span>
<span data-ttu-id="c3cac-131">Określa obszar nazw, do którego są przypisywane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="c3cac-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="c3cac-132">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c3cac-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="c3cac-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c3cac-133">-ResourceGroup</span></span>
<span data-ttu-id="c3cac-134">Określa grupę zasobów, do której są przydzielone reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="c3cac-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="c3cac-135">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="c3cac-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c3cac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3cac-136">CommonParameters</span></span>
<span data-ttu-id="c3cac-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3cac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3cac-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3cac-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3cac-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3cac-139">INPUTS</span></span>

### <span data-ttu-id="c3cac-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c3cac-140">System.String</span></span>

## <span data-ttu-id="c3cac-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3cac-141">OUTPUTS</span></span>

### <span data-ttu-id="c3cac-142">Microsoft. Azure. Commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c3cac-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c3cac-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3cac-143">NOTES</span></span>

## <span data-ttu-id="c3cac-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3cac-144">RELATED LINKS</span></span>

[<span data-ttu-id="c3cac-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c3cac-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="c3cac-146">Nowe — AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c3cac-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="c3cac-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c3cac-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="c3cac-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c3cac-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


