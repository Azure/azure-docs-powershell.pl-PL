---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 062d16155d4e1644e09f914a1114741e7bc5365f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179299"
---
# <span data-ttu-id="3d1ab-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="3d1ab-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="3d1ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1ab-103">Pobiera podstawowe i pomocnicze parametry połączenia skojarzone z regułą autoryzacji centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="3d1ab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3d1ab-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d1ab-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3d1ab-105">DESCRIPTION</span></span>
<span data-ttu-id="3d1ab-106">Polecenie **cmdlet Get-AzNotificationHubListKey** zwraca podstawowe i pomocnicze parametry połączenia reguły autoryzacji podpisu dostępu udostępnionego (SAS) centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="3d1ab-107">Reguły autoryzacji zarządzają prawami użytkowników do centrum.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="3d1ab-108">Każda reguła zawiera podstawowy i pomocniczy ciąg połączenia.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="3d1ab-109">Te parametry połączenia ( URI) wykonują następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="3d1ab-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="3d1ab-110">Wskaż użytkownikom zasób.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-110">Point users to a resource.</span></span>
- <span data-ttu-id="3d1ab-111">Uwzględnianie tokenu zawierającego parametry zapytania.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="3d1ab-112">Jeden z tych parametrów ( podpis) służy do uwierzytelniania użytkownika i zapewnienia określonego poziomu dostępu.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="3d1ab-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3d1ab-113">EXAMPLES</span></span>

### <span data-ttu-id="3d1ab-114">Przykład 1. Uzyskiwanie podstawowych i pomocniczych ciągów połączenia dla reguły autoryzacji</span><span class="sxs-lookup"><span data-stu-id="3d1ab-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="3d1ab-115">To polecenie pobiera podstawowe i pomocnicze parametry połączenia dla reguły autoryzacji ListenRule , reguły przypisanej do centrum powiadomień ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="3d1ab-116">To polecenie musi zawierać przestrzeń nazw centrum i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="3d1ab-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d1ab-117">PARAMETERS</span></span>

### <span data-ttu-id="3d1ab-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d1ab-118">-AuthorizationRule</span></span>
<span data-ttu-id="3d1ab-119">Określa nazwę reguły uwierzytelniania SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="3d1ab-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="3d1ab-120">Te reguły określają typ dostępu użytkowników do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d1ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d1ab-121">-DefaultProfile</span></span>
<span data-ttu-id="3d1ab-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3d1ab-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d1ab-123">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="3d1ab-123">-Namespace</span></span>
<span data-ttu-id="3d1ab-124">Określa przestrzeń nazw, do której jest przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="3d1ab-125">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3d1ab-126">- NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3d1ab-126">-NotificationHub</span></span>
<span data-ttu-id="3d1ab-127">Określa centrum powiadomień, do których to polecenie cmdlet przypisuje regułę autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="3d1ab-128">Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów bez względu na platformę używaną przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="3d1ab-129">- ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3d1ab-129">-ResourceGroup</span></span>
<span data-ttu-id="3d1ab-130">Określa grupę zasobów, do której jest przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="3d1ab-131">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3d1ab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1ab-132">CommonParameters</span></span>
<span data-ttu-id="3d1ab-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d1ab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1ab-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d1ab-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1ab-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d1ab-135">INPUTS</span></span>

### <span data-ttu-id="3d1ab-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3d1ab-136">System.String</span></span>

## <span data-ttu-id="3d1ab-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d1ab-137">OUTPUTS</span></span>

### <span data-ttu-id="3d1ab-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="3d1ab-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="3d1ab-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3d1ab-139">NOTES</span></span>

## <span data-ttu-id="3d1ab-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d1ab-140">RELATED LINKS</span></span>

[<span data-ttu-id="3d1ab-141">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3d1ab-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)


