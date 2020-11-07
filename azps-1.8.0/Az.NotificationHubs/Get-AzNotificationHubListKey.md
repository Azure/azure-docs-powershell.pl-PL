---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 6b9aa676e00d137612908955e88558b4cefb0eb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708875"
---
# <span data-ttu-id="aa307-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="aa307-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="aa307-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa307-102">SYNOPSIS</span></span>
<span data-ttu-id="aa307-103">Pobiera parametry połączenia podstawowego i pomocniczego skojarzone z regułą autoryzacji centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="aa307-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="aa307-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa307-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa307-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa307-105">DESCRIPTION</span></span>
<span data-ttu-id="aa307-106">Polecenie cmdlet **Get-AzNotificationHubListKey** zwraca podstawowe i pomocnicze ciągi połączeń dla reguły autoryzacji podpisu dostępu udostępnionego w centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="aa307-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="aa307-107">Reguły autoryzacji Zarządzaj prawami użytkowników do centrum.</span><span class="sxs-lookup"><span data-stu-id="aa307-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="aa307-108">Każda reguła zawiera parametry połączenia podstawowego i pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="aa307-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="aa307-109">Te ciągi połączeń (identyfikatory URI) wykonują następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="aa307-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="aa307-110">Wskazywanie użytkownikom zasobu.</span><span class="sxs-lookup"><span data-stu-id="aa307-110">Point users to a resource.</span></span>
- <span data-ttu-id="aa307-111">Dołącz token zawierający parametry zapytania.</span><span class="sxs-lookup"><span data-stu-id="aa307-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="aa307-112">Za pomocą jednego z tych parametrów podpis służy do uwierzytelniania użytkownika i zapewnia określony poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="aa307-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="aa307-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa307-113">EXAMPLES</span></span>

### <span data-ttu-id="aa307-114">Przykład 1: uzyskiwanie ciągów połączenia podstawowego i pomocniczego dla reguły autoryzacji</span><span class="sxs-lookup"><span data-stu-id="aa307-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="aa307-115">To polecenie pobiera podstawowe i pomocnicze ciągi połączeń dla reguły autoryzacji ListenRule, regułę przypisaną do centrum powiadomień usługi ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="aa307-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="aa307-116">Polecenie musi zawierać obszar nazw centrum i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa307-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="aa307-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa307-117">PARAMETERS</span></span>

### <span data-ttu-id="aa307-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="aa307-118">-AuthorizationRule</span></span>
<span data-ttu-id="aa307-119">Określa nazwę reguły uwierzytelniania w ramach udostępniania podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="aa307-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="aa307-120">Te reguły określają typ dostępu do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="aa307-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="aa307-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa307-121">-DefaultProfile</span></span>
<span data-ttu-id="aa307-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="aa307-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa307-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aa307-123">-Namespace</span></span>
<span data-ttu-id="aa307-124">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="aa307-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="aa307-125">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="aa307-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="aa307-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="aa307-126">-NotificationHub</span></span>
<span data-ttu-id="aa307-127">Określa centrum powiadomień, do którego jest przypisywana reguła autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="aa307-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="aa307-128">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="aa307-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="aa307-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aa307-129">-ResourceGroup</span></span>
<span data-ttu-id="aa307-130">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="aa307-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="aa307-131">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="aa307-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="aa307-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa307-132">CommonParameters</span></span>
<span data-ttu-id="aa307-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa307-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa307-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa307-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa307-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa307-135">INPUTS</span></span>

### <span data-ttu-id="aa307-136">System. String</span><span class="sxs-lookup"><span data-stu-id="aa307-136">System.String</span></span>

## <span data-ttu-id="aa307-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa307-137">OUTPUTS</span></span>

### <span data-ttu-id="aa307-138">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="aa307-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="aa307-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa307-139">NOTES</span></span>

## <span data-ttu-id="aa307-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa307-140">RELATED LINKS</span></span>

[<span data-ttu-id="aa307-141">Get-AzNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="aa307-141">Get-AzNotificationHubAuthorizationRules</span></span>](./Get-AzNotificationHubAuthorizationRules.md)

