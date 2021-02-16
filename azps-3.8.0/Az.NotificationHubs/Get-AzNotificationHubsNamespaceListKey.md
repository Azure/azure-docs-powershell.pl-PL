---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 5244602a6b6266ebabf02bbb927facda93e61d8b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403803"
---
# <span data-ttu-id="11347-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="11347-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="11347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11347-102">SYNOPSIS</span></span>
<span data-ttu-id="11347-103">Pobiera podstawowe i pomocnicze parametry połączenia skojarzone z regułą autoryzacji przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="11347-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="11347-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11347-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11347-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="11347-105">DESCRIPTION</span></span>
<span data-ttu-id="11347-106">Polecenie **cmdlet Get-AzNotificationHubsNamespaceListKey** zwraca podstawowe i pomocnicze parametry połączenia dla reguły autoryzacji sas (Shared Access Signature) przypisanej do przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="11347-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="11347-107">Reguły autoryzacji zarządzają prawami użytkowników do przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="11347-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="11347-108">Każda reguła zawiera podstawowy i pomocniczy ciąg połączenia.</span><span class="sxs-lookup"><span data-stu-id="11347-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="11347-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11347-109">EXAMPLES</span></span>

### <span data-ttu-id="11347-110">Przykład 1. Uzyskiwanie podstawowych i pomocniczych ciągów połączenia dla reguły autoryzacji</span><span class="sxs-lookup"><span data-stu-id="11347-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="11347-111">To polecenie zwraca podstawowe i pomocnicze ciągi połączeń reguły autoryzacji o nazwie ListenRule przypisanej do przestrzeni nazw ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="11347-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="11347-112">Po uruchomieniu tego polecenia musisz podać nazwę grupy zasobów, do których jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="11347-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="11347-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11347-113">PARAMETERS</span></span>

### <span data-ttu-id="11347-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="11347-114">-AuthorizationRule</span></span>
<span data-ttu-id="11347-115">Określa nazwę reguły uwierzytelniania SAS.</span><span class="sxs-lookup"><span data-stu-id="11347-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="11347-116">Te reguły określają typ dostępu użytkowników do Centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="11347-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="11347-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11347-117">-DefaultProfile</span></span>
<span data-ttu-id="11347-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="11347-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11347-119">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="11347-119">-Namespace</span></span>
<span data-ttu-id="11347-120">Określa przestrzeń nazw zawierającą ciągi połączeń, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11347-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="11347-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11347-121">-ResourceGroup</span></span>
<span data-ttu-id="11347-122">Określa grupę zasobów, do której jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="11347-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="11347-123">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11347-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="11347-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11347-124">CommonParameters</span></span>
<span data-ttu-id="11347-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11347-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11347-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11347-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11347-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11347-127">INPUTS</span></span>

### <span data-ttu-id="11347-128">System.String</span><span class="sxs-lookup"><span data-stu-id="11347-128">System.String</span></span>

## <span data-ttu-id="11347-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11347-129">OUTPUTS</span></span>

### <span data-ttu-id="11347-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="11347-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="11347-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11347-131">NOTES</span></span>

## <span data-ttu-id="11347-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11347-132">RELATED LINKS</span></span>

[<span data-ttu-id="11347-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="11347-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)



