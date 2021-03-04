---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 5087351b3c868c8d1e536423c435481e6e2f6feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951281"
---
# <span data-ttu-id="4434a-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="4434a-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="4434a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4434a-102">SYNOPSIS</span></span>
<span data-ttu-id="4434a-103">Pobiera podstawowe i pomocnicze parametry połączenia skojarzone z regułą autoryzacji przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="4434a-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="4434a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4434a-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4434a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4434a-105">DESCRIPTION</span></span>
<span data-ttu-id="4434a-106">Polecenie **cmdlet Get-AzNotificationHubsNamespaceListKey** zwraca podstawowe i pomocnicze parametry połączenia dla reguły autoryzacji SAS (Shared Access Signature) przypisanej do przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="4434a-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="4434a-107">Reguły autoryzacji zarządzają prawami użytkowników do przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="4434a-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="4434a-108">Każda reguła zawiera podstawowy i pomocniczy ciąg połączenia.</span><span class="sxs-lookup"><span data-stu-id="4434a-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="4434a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4434a-109">EXAMPLES</span></span>

### <span data-ttu-id="4434a-110">Przykład 1. Uzyskiwanie podstawowych i pomocniczych ciągów połączenia dla reguły autoryzacji</span><span class="sxs-lookup"><span data-stu-id="4434a-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="4434a-111">To polecenie zwraca podstawowe i pomocnicze parametry połączenia reguły autoryzacji o nazwie ListenRule przypisanej do przestrzeni nazw ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="4434a-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="4434a-112">Po uruchomieniu tego polecenia musisz podać nazwę grupy zasobów, do których jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="4434a-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="4434a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4434a-113">PARAMETERS</span></span>

### <span data-ttu-id="4434a-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4434a-114">-AuthorizationRule</span></span>
<span data-ttu-id="4434a-115">Określa nazwę reguły uwierzytelniania SAS.</span><span class="sxs-lookup"><span data-stu-id="4434a-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="4434a-116">Te reguły określają typ dostępu użytkowników do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="4434a-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="4434a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4434a-117">-DefaultProfile</span></span>
<span data-ttu-id="4434a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4434a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4434a-119">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="4434a-119">-Namespace</span></span>
<span data-ttu-id="4434a-120">Określa przestrzeń nazw zawierającą ciągi połączeń, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4434a-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4434a-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4434a-121">-ResourceGroup</span></span>
<span data-ttu-id="4434a-122">Określa grupę zasobów, do której jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="4434a-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="4434a-123">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4434a-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="4434a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4434a-124">CommonParameters</span></span>
<span data-ttu-id="4434a-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4434a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4434a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4434a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4434a-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4434a-127">INPUTS</span></span>

### <span data-ttu-id="4434a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4434a-128">System.String</span></span>

## <span data-ttu-id="4434a-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4434a-129">OUTPUTS</span></span>

### <span data-ttu-id="4434a-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="4434a-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="4434a-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4434a-131">NOTES</span></span>

## <span data-ttu-id="4434a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4434a-132">RELATED LINKS</span></span>

[<span data-ttu-id="4434a-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="4434a-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="4434a-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4434a-134">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)


