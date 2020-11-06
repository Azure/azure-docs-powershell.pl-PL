---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ade411d6d8ca19a5c17afd87388f9f7ab90d64d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554112"
---
# <span data-ttu-id="ee274-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ee274-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="ee274-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee274-102">SYNOPSIS</span></span>
<span data-ttu-id="ee274-103">Pobiera informacje o regułach autoryzacji skojarzonych z obszarem nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ee274-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee274-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee274-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee274-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee274-105">DESCRIPTION</span></span>
<span data-ttu-id="ee274-106">Polecenie cmdlet **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** zwraca informacje o regułach autoryzacji związanych z dostępem do funkcji podpisów udostępnionych (SAS) skojarzonych z obszarem nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ee274-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="ee274-107">Możesz zwrócić informacje dotyczące wszystkich reguł skojarzonych z obszarem nazw.</span><span class="sxs-lookup"><span data-stu-id="ee274-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="ee274-108">Możesz również zwrócić informacje dotyczące konkretnej reguły, a także podając parametr *AuthorizationRule* .</span><span class="sxs-lookup"><span data-stu-id="ee274-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>

<span data-ttu-id="ee274-109">Reguły autoryzacji zarządzają dostępem do obszarów nazw.</span><span class="sxs-lookup"><span data-stu-id="ee274-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="ee274-110">Służą do tego tworzenie linków jako identyfikatorów URI na podstawie różnych poziomów uprawnień.</span><span class="sxs-lookup"><span data-stu-id="ee274-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="ee274-111">Może to być jedna z następujących poziomów platformy:</span><span class="sxs-lookup"><span data-stu-id="ee274-111">Platform levels can be one of the following:</span></span> 

- <span data-ttu-id="ee274-112">Słuch</span><span class="sxs-lookup"><span data-stu-id="ee274-112">Listen</span></span>
- <span data-ttu-id="ee274-113">Wyślij</span><span class="sxs-lookup"><span data-stu-id="ee274-113">Send</span></span>
- <span data-ttu-id="ee274-114">Zarządzanie</span><span class="sxs-lookup"><span data-stu-id="ee274-114">Manage</span></span>

<span data-ttu-id="ee274-115">Klienci są kierowani do jednego z tych identyfikatorów URI na podstawie odpowiedniego poziomu uprawnień.</span><span class="sxs-lookup"><span data-stu-id="ee274-115">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="ee274-116">Na przykład klient, któremu nadano uprawnienie do odsłuchiwania, będzie kierowany na identyfikator URI tego uprawnienia.</span><span class="sxs-lookup"><span data-stu-id="ee274-116">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="ee274-117">To polecenie cmdlet pobiera tylko reguły autoryzacji skojarzone z obszarem nazw.</span><span class="sxs-lookup"><span data-stu-id="ee274-117">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="ee274-118">Aby uzyskać informacje na temat samego obszaru nazw, użyj polecenie Get-AzureRmNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="ee274-118">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="ee274-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee274-119">EXAMPLES</span></span>

### <span data-ttu-id="ee274-120">Przykład 1: uzyskiwanie informacji o wszystkich regułach autoryzacji przypisanych do obszarów nazw</span><span class="sxs-lookup"><span data-stu-id="ee274-120">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="ee274-121">To polecenie pobiera informacje o wszystkich regułach autoryzacji przypisanych zarówno do obszaru nazw ContosoNamespace, jak i grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="ee274-121">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="ee274-122">Przykład 2: uzyskiwanie informacji na temat reguły autoryzacji</span><span class="sxs-lookup"><span data-stu-id="ee274-122">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="ee274-123">To polecenie pobiera informacje na temat jednej reguły autoryzacji obszaru nazw o nazwie ListenRule.</span><span class="sxs-lookup"><span data-stu-id="ee274-123">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="ee274-124">Aby uzyskać informacje dotyczące określonej reguły autoryzacji, należy uwzględnić obszar nazw i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee274-124">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="ee274-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee274-125">PARAMETERS</span></span>

### <span data-ttu-id="ee274-126">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ee274-126">-AuthorizationRule</span></span>
<span data-ttu-id="ee274-127">Określa nazwę reguły uwierzytelniania SAS.</span><span class="sxs-lookup"><span data-stu-id="ee274-127">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="ee274-128">Te reguły określają typ dostępu do obszaru nazw użytkownikom.</span><span class="sxs-lookup"><span data-stu-id="ee274-128">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee274-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee274-129">-DefaultProfile</span></span>
<span data-ttu-id="ee274-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ee274-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee274-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ee274-131">-Namespace</span></span>
<span data-ttu-id="ee274-132">Określa obszar nazw, do którego są przypisywane reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="ee274-132">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="ee274-133">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ee274-133">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee274-134">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ee274-134">-ResourceGroup</span></span>
<span data-ttu-id="ee274-135">Określa grupę zasobów, do której są przydzielone reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="ee274-135">Specifies the resource group to which the authorization rules are assigned.</span></span>

<span data-ttu-id="ee274-136">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="ee274-136">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee274-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee274-137">CommonParameters</span></span>
<span data-ttu-id="ee274-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee274-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee274-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee274-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee274-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee274-140">INPUTS</span></span>

### <span data-ttu-id="ee274-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ee274-141">None</span></span>
<span data-ttu-id="ee274-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ee274-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee274-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee274-143">OUTPUTS</span></span>

### <span data-ttu-id="ee274-144">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. NotificationHubs. modele. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="ee274-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="ee274-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee274-145">NOTES</span></span>

## <span data-ttu-id="ee274-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee274-146">RELATED LINKS</span></span>

[<span data-ttu-id="ee274-147">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ee274-147">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="ee274-148">Nowe — AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ee274-148">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="ee274-149">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ee274-149">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="ee274-150">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ee274-150">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


