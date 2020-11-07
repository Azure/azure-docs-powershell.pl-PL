---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 90e617f35442470cef2d11c2de032679698ea167
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895849"
---
# <span data-ttu-id="0a8a3-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="0a8a3-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="0a8a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a8a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8a3-103">Pobiera parametry połączenia podstawowego i pomocniczego skojarzone z regułą autoryzacji obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="0a8a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a8a3-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a8a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a8a3-105">DESCRIPTION</span></span>
<span data-ttu-id="0a8a3-106">Polecenie cmdlet **Get-AzNotificationHubsNamespaceListKey** zwraca podstawowe i pomocnicze ciągi połączeń dla reguły autoryzacji podpisu dostępu współużytkowanego (SAS) przypisanej do obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="0a8a3-107">Reguły autoryzacji Zarządzaj prawami użytkownika w obszarze nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="0a8a3-108">Każda reguła zawiera parametry połączenia podstawowego i pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="0a8a3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a8a3-109">EXAMPLES</span></span>

### <span data-ttu-id="0a8a3-110">Przykład 1: uzyskiwanie ciągów połączenia podstawowego i pomocniczego dla reguły autoryzacji</span><span class="sxs-lookup"><span data-stu-id="0a8a3-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="0a8a3-111">To polecenie zwraca podstawowe i pomocnicze parametry połączenia dla reguły autoryzacji o nazwie ListenRule przypisanej do przestrzeni nazw ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="0a8a3-112">Po uruchomieniu tego polecenia musisz dołączyć nazwę grupy zasobów, do której jest przypisany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="0a8a3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a8a3-113">PARAMETERS</span></span>

### <span data-ttu-id="0a8a3-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0a8a3-114">-AuthorizationRule</span></span>
<span data-ttu-id="0a8a3-115">Określa nazwę reguły uwierzytelniania SAS.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="0a8a3-116">Te reguły określają typ dostępu do centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="0a8a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8a3-117">-DefaultProfile</span></span>
<span data-ttu-id="0a8a3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0a8a3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a8a3-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0a8a3-119">-Namespace</span></span>
<span data-ttu-id="0a8a3-120">Określa obszar nazw zawierający parametry połączenia, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0a8a3-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0a8a3-121">-ResourceGroup</span></span>
<span data-ttu-id="0a8a3-122">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="0a8a3-123">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="0a8a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8a3-124">CommonParameters</span></span>
<span data-ttu-id="0a8a3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a8a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8a3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a8a3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8a3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a8a3-127">INPUTS</span></span>

### <span data-ttu-id="0a8a3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0a8a3-128">System.String</span></span>

## <span data-ttu-id="0a8a3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a8a3-129">OUTPUTS</span></span>

### <span data-ttu-id="0a8a3-130">Microsoft. Azure. Management. NotificationHubs. MODELES. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="0a8a3-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="0a8a3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a8a3-131">NOTES</span></span>

## <span data-ttu-id="0a8a3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a8a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="0a8a3-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0a8a3-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="0a8a3-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="0a8a3-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)


