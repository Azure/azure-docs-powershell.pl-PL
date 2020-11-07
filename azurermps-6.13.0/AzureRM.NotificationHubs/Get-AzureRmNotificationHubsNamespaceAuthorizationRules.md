---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 9546039459792d5ef72807d8466f728f2060a346
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716936"
---
# <span data-ttu-id="135ea-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="135ea-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="135ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="135ea-102">SYNOPSIS</span></span>
<span data-ttu-id="135ea-103">Pobiera informacje o regułach autoryzacji skojarzonych z obszarem nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="135ea-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="135ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="135ea-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="135ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="135ea-105">DESCRIPTION</span></span>
<span data-ttu-id="135ea-106">Polecenie cmdlet **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** zwraca informacje o regułach autoryzacji związanych z dostępem do funkcji podpisów udostępnionych (SAS) skojarzonych z obszarem nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="135ea-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="135ea-107">Możesz zwrócić informacje dotyczące wszystkich reguł skojarzonych z obszarem nazw.</span><span class="sxs-lookup"><span data-stu-id="135ea-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="135ea-108">Możesz również zwrócić informacje dotyczące konkretnej reguły, a także podając parametr *AuthorizationRule* .</span><span class="sxs-lookup"><span data-stu-id="135ea-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="135ea-109">Reguły autoryzacji zarządzają dostępem do obszarów nazw.</span><span class="sxs-lookup"><span data-stu-id="135ea-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="135ea-110">Służą do tego tworzenie linków jako identyfikatorów URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="135ea-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="135ea-111">Może to być jedna z następujących poziomów platformy:</span><span class="sxs-lookup"><span data-stu-id="135ea-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="135ea-112">Słuch</span><span class="sxs-lookup"><span data-stu-id="135ea-112">Listen</span></span>
- <span data-ttu-id="135ea-113">Wyślij</span><span class="sxs-lookup"><span data-stu-id="135ea-113">Send</span></span>
- <span data-ttu-id="135ea-114">Zarządzanie klientami jest przekierowywane do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="135ea-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="135ea-115">Na przykład klient, któremu nadano uprawnienie do odsłuchiwania, będzie kierowany na identyfikator URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="135ea-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="135ea-116">To polecenie cmdlet pobiera tylko reguły autoryzacji skojarzone z obszarem nazw.</span><span class="sxs-lookup"><span data-stu-id="135ea-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="135ea-117">Aby uzyskać informacje na temat samego obszaru nazw, użyj polecenie Get-AzureRmNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="135ea-117">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="135ea-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="135ea-118">EXAMPLES</span></span>

### <span data-ttu-id="135ea-119">Przykład 1: uzyskiwanie informacji o wszystkich regułach autoryzacji przypisanych do obszarów nazw</span><span class="sxs-lookup"><span data-stu-id="135ea-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="135ea-120">To polecenie pobiera informacje o wszystkich regułach autoryzacji przypisanych zarówno do obszaru nazw ContosoNamespace, jak i grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="135ea-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="135ea-121">Przykład 2: uzyskiwanie informacji na temat reguły autoryzacji</span><span class="sxs-lookup"><span data-stu-id="135ea-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="135ea-122">To polecenie pobiera informacje na temat jednej reguły autoryzacji obszaru nazw o nazwie ListenRule.</span><span class="sxs-lookup"><span data-stu-id="135ea-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="135ea-123">Aby uzyskać informacje dotyczące określonej reguły autoryzacji, należy uwzględnić obszar nazw i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="135ea-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="135ea-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="135ea-124">PARAMETERS</span></span>

### <span data-ttu-id="135ea-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="135ea-125">-AuthorizationRule</span></span>
<span data-ttu-id="135ea-126">Określa nazwę reguły uwierzytelniania SAS.</span><span class="sxs-lookup"><span data-stu-id="135ea-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="135ea-127">Te reguły określają typ dostępu do obszaru nazw użytkownikom.</span><span class="sxs-lookup"><span data-stu-id="135ea-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="135ea-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="135ea-128">-DefaultProfile</span></span>
<span data-ttu-id="135ea-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="135ea-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135ea-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="135ea-130">-Namespace</span></span>
<span data-ttu-id="135ea-131">Określa obszar nazw, do którego są przypisywane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="135ea-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="135ea-132">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="135ea-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="135ea-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="135ea-133">-ResourceGroup</span></span>
<span data-ttu-id="135ea-134">Określa grupę zasobów, do której są przydzielone reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="135ea-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="135ea-135">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="135ea-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="135ea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="135ea-136">CommonParameters</span></span>
<span data-ttu-id="135ea-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="135ea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="135ea-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="135ea-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="135ea-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="135ea-139">INPUTS</span></span>

### <span data-ttu-id="135ea-140">System. String</span><span class="sxs-lookup"><span data-stu-id="135ea-140">System.String</span></span>

## <span data-ttu-id="135ea-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="135ea-141">OUTPUTS</span></span>

### <span data-ttu-id="135ea-142">Microsoft. Azure. Commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="135ea-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="135ea-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="135ea-143">NOTES</span></span>

## <span data-ttu-id="135ea-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="135ea-144">RELATED LINKS</span></span>

[<span data-ttu-id="135ea-145">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="135ea-145">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="135ea-146">Nowe — AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="135ea-146">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="135ea-147">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="135ea-147">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="135ea-148">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="135ea-148">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


