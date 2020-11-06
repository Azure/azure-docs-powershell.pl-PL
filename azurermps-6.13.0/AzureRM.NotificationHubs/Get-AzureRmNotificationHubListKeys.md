---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhublistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 05c6ce89577e3c24368ddf47a0dec0abfeb2a388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547395"
---
# <span data-ttu-id="8f38b-101">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="8f38b-101">Get-AzureRmNotificationHubListKeys</span></span>

## <span data-ttu-id="8f38b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f38b-102">SYNOPSIS</span></span>
<span data-ttu-id="8f38b-103">Pobiera parametry połączenia podstawowego i pomocniczego skojarzone z regułą autoryzacji centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8f38b-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f38b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f38b-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f38b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8f38b-105">DESCRIPTION</span></span>
<span data-ttu-id="8f38b-106">Polecenie cmdlet **Get-AzureRmNotificationHubListKeys** zwraca podstawowe i pomocnicze ciągi połączeń dla reguły autoryzacji podpisu dostępu udostępnionego w centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8f38b-106">The **Get-AzureRmNotificationHubListKeys** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="8f38b-107">Reguły autoryzacji Zarządzaj prawami użytkowników do centrum.</span><span class="sxs-lookup"><span data-stu-id="8f38b-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="8f38b-108">Każda reguła zawiera parametry połączenia podstawowego i pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="8f38b-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="8f38b-109">Te ciągi połączeń (identyfikatory URI) wykonują następujące czynności:</span><span class="sxs-lookup"><span data-stu-id="8f38b-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="8f38b-110">Wskazywanie użytkownikom zasobu.</span><span class="sxs-lookup"><span data-stu-id="8f38b-110">Point users to a resource.</span></span>
- <span data-ttu-id="8f38b-111">Dołącz token zawierający parametry zapytania.</span><span class="sxs-lookup"><span data-stu-id="8f38b-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="8f38b-112">Za pomocą jednego z tych parametrów podpis służy do uwierzytelniania użytkownika i zapewnia określony poziom dostępu.</span><span class="sxs-lookup"><span data-stu-id="8f38b-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="8f38b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f38b-113">EXAMPLES</span></span>

### <span data-ttu-id="8f38b-114">Przykład 1: uzyskiwanie ciągów połączenia podstawowego i pomocniczego dla reguły autoryzacji</span><span class="sxs-lookup"><span data-stu-id="8f38b-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="8f38b-115">To polecenie pobiera podstawowe i pomocnicze ciągi połączeń dla reguły autoryzacji ListenRule, regułę przypisaną do centrum powiadomień usługi ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="8f38b-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="8f38b-116">Polecenie musi zawierać obszar nazw centrum i grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f38b-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="8f38b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f38b-117">PARAMETERS</span></span>

### <span data-ttu-id="8f38b-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8f38b-118">-AuthorizationRule</span></span>
<span data-ttu-id="8f38b-119">Określa nazwę reguły uwierzytelniania w ramach udostępniania podpisu dostępu (SAS).</span><span class="sxs-lookup"><span data-stu-id="8f38b-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="8f38b-120">Te reguły określają typ dostępu do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8f38b-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="8f38b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f38b-121">-DefaultProfile</span></span>
<span data-ttu-id="8f38b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8f38b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f38b-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8f38b-123">-Namespace</span></span>
<span data-ttu-id="8f38b-124">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8f38b-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="8f38b-125">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8f38b-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8f38b-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="8f38b-126">-NotificationHub</span></span>
<span data-ttu-id="8f38b-127">Określa centrum powiadomień, do którego jest przypisywana reguła autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="8f38b-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="8f38b-128">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="8f38b-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="8f38b-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8f38b-129">-ResourceGroup</span></span>
<span data-ttu-id="8f38b-130">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8f38b-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="8f38b-131">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="8f38b-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8f38b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f38b-132">CommonParameters</span></span>
<span data-ttu-id="8f38b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f38b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f38b-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f38b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f38b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f38b-135">INPUTS</span></span>

### <span data-ttu-id="8f38b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8f38b-136">System.String</span></span>

## <span data-ttu-id="8f38b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f38b-137">OUTPUTS</span></span>

### <span data-ttu-id="8f38b-138">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="8f38b-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="8f38b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f38b-139">NOTES</span></span>

## <span data-ttu-id="8f38b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f38b-140">RELATED LINKS</span></span>

[<span data-ttu-id="8f38b-141">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8f38b-141">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)


