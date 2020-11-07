---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 440eb112ea49465863b53f705c6b90a8b2e4be74
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708873"
---
# <span data-ttu-id="ba8be-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="ba8be-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="ba8be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba8be-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8be-103">Pobiera poświadczenia PNS dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ba8be-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="ba8be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba8be-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba8be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba8be-105">DESCRIPTION</span></span>
<span data-ttu-id="ba8be-106">Polecenie cmdlet **Get-AzNotificationHubPNSCredential** Pobiera poświadczenia usługi powiadamiania platformy (PNS) dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ba8be-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="ba8be-107">Każdy z centrum powiadomień ma jeden zestaw poświadczeń PNS.</span><span class="sxs-lookup"><span data-stu-id="ba8be-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="ba8be-108">Te poświadczenia są stosowane do poszczególnych usług powiadomień WNS, takich jak, ale bez ograniczeń. Usługa powiadomień WNS, Usługa powiadomienia push w systemie Android i Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="ba8be-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="ba8be-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba8be-109">EXAMPLES</span></span>

### <span data-ttu-id="ba8be-110">Przykład 1: Uzyskaj poświadczenia PNS dla określonego centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="ba8be-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="ba8be-111">To polecenie pobiera poświadczenia PNS dla centrum powiadomień o nazwie ContosoInternalHub należącego do grupy zasobów o nazwie ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="ba8be-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="ba8be-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba8be-112">PARAMETERS</span></span>

### <span data-ttu-id="ba8be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8be-113">-DefaultProfile</span></span>
<span data-ttu-id="ba8be-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ba8be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba8be-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ba8be-115">-Namespace</span></span>
<span data-ttu-id="ba8be-116">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ba8be-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="ba8be-117">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ba8be-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ba8be-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="ba8be-118">-NotificationHub</span></span>
<span data-ttu-id="ba8be-119">Określa centrum powiadomień, do którego przypisano poświadczenia PNS.</span><span class="sxs-lookup"><span data-stu-id="ba8be-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="ba8be-120">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="ba8be-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="ba8be-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ba8be-121">-ResourceGroup</span></span>
<span data-ttu-id="ba8be-122">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ba8be-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="ba8be-123">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="ba8be-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ba8be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8be-124">CommonParameters</span></span>
<span data-ttu-id="ba8be-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba8be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8be-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba8be-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8be-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba8be-127">INPUTS</span></span>

### <span data-ttu-id="ba8be-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ba8be-128">System.String</span></span>

## <span data-ttu-id="ba8be-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba8be-129">OUTPUTS</span></span>

### <span data-ttu-id="ba8be-130">Microsoft. Azure. Commands. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="ba8be-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="ba8be-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba8be-131">NOTES</span></span>

## <span data-ttu-id="ba8be-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba8be-132">RELATED LINKS</span></span>

[<span data-ttu-id="ba8be-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="ba8be-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

