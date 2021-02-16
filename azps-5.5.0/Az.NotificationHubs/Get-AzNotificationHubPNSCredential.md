---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 282e8092050b5859809c8dad71c4da1ee86c779d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184115"
---
# <span data-ttu-id="c270f-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="c270f-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="c270f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c270f-102">SYNOPSIS</span></span>
<span data-ttu-id="c270f-103">Pobiera poświadczenia usługi PNS dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c270f-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="c270f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c270f-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c270f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c270f-105">DESCRIPTION</span></span>
<span data-ttu-id="c270f-106">Polecenie **cmdlet Get-AzNotificationHubPNSCredential** pobiera poświadczenia usługi powiadomień platformy (PNS) dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c270f-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="c270f-107">Każde centrum powiadomień ma jeden zestaw poświadczeń PNS.</span><span class="sxs-lookup"><span data-stu-id="c270f-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="c270f-108">Te poświadczenia są stosowane do poszczególnych usług powiadomień wypychanych, takich jak między innymi; usługi powiadomień wypychanych systemu iOS, usługi powiadomień wypychanych systemu Android i systemu Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="c270f-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="c270f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c270f-109">EXAMPLES</span></span>

### <span data-ttu-id="c270f-110">Przykład 1. Uzyskiwanie poświadczeń PNS dla konkretnego centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="c270f-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="c270f-111">To polecenie pobiera poświadczenia PNS dla centrum powiadomień o nazwie ContosoInternalHub, które należy do grupy zasobów o nazwie ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="c270f-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="c270f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c270f-112">PARAMETERS</span></span>

### <span data-ttu-id="c270f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c270f-113">-DefaultProfile</span></span>
<span data-ttu-id="c270f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c270f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c270f-115">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="c270f-115">-Namespace</span></span>
<span data-ttu-id="c270f-116">Określa przestrzeń nazw, do której jest przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c270f-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="c270f-117">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c270f-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="c270f-118">- NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c270f-118">-NotificationHub</span></span>
<span data-ttu-id="c270f-119">Określa centrum powiadomień, do których są przypisane poświadczenia PNS.</span><span class="sxs-lookup"><span data-stu-id="c270f-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="c270f-120">Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów bez względu na platformę używaną przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="c270f-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="c270f-121">- ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c270f-121">-ResourceGroup</span></span>
<span data-ttu-id="c270f-122">Określa grupę zasobów, do której jest przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c270f-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="c270f-123">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c270f-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c270f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c270f-124">CommonParameters</span></span>
<span data-ttu-id="c270f-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c270f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c270f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c270f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c270f-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c270f-127">INPUTS</span></span>

### <span data-ttu-id="c270f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c270f-128">System.String</span></span>

## <span data-ttu-id="c270f-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c270f-129">OUTPUTS</span></span>

### <span data-ttu-id="c270f-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="c270f-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="c270f-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c270f-131">NOTES</span></span>

## <span data-ttu-id="c270f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c270f-132">RELATED LINKS</span></span>

[<span data-ttu-id="c270f-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c270f-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


