---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
ms.openlocfilehash: 29f4871b6299685ae5791f82498083956a7e4048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543179"
---
# <span data-ttu-id="df7b4-101">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="df7b4-101">Get-AzureRmNotificationHubPNSCredentials</span></span>

## <span data-ttu-id="df7b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df7b4-102">SYNOPSIS</span></span>
<span data-ttu-id="df7b4-103">Pobiera poświadczenia PNS dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="df7b4-103">Gets the PNS credentials for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df7b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df7b4-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubPNSCredentials [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df7b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="df7b4-105">DESCRIPTION</span></span>
<span data-ttu-id="df7b4-106">Polecenie cmdlet **Get-AzureRmNotificationHubPNSCredentials** Pobiera poświadczenia usługi powiadamiania platformy (PNS) dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="df7b4-106">The **Get-AzureRmNotificationHubPNSCredentials** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="df7b4-107">Każdy z centrum powiadomień ma jeden zestaw poświadczeń PNS.</span><span class="sxs-lookup"><span data-stu-id="df7b4-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="df7b4-108">Te poświadczenia są stosowane do poszczególnych usług powiadomień WNS, takich jak, ale bez ograniczeń. Usługa powiadomień WNS, Usługa powiadomienia push w systemie Android i Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="df7b4-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="df7b4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df7b4-109">EXAMPLES</span></span>

### <span data-ttu-id="df7b4-110">Przykład 1: Uzyskaj poświadczenia PNS dla określonego centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="df7b4-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzureRmNotificationHubPNSCredentials -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="df7b4-111">To polecenie pobiera poświadczenia PNS dla centrum powiadomień o nazwie ContosoInternalHub należącego do grupy zasobów o nazwie ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="df7b4-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="df7b4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df7b4-112">PARAMETERS</span></span>

### <span data-ttu-id="df7b4-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="df7b4-113">-Namespace</span></span>
<span data-ttu-id="df7b4-114">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="df7b4-114">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="df7b4-115">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="df7b4-115">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="df7b4-116">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="df7b4-116">-NotificationHub</span></span>
<span data-ttu-id="df7b4-117">Określa centrum powiadomień, do którego przypisano poświadczenia PNS.</span><span class="sxs-lookup"><span data-stu-id="df7b4-117">Specifies the notification hub that the PNS credentials are assigned to.</span></span>

<span data-ttu-id="df7b4-118">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="df7b4-118">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="df7b4-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="df7b4-119">-ResourceGroup</span></span>
<span data-ttu-id="df7b4-120">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="df7b4-120">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="df7b4-121">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="df7b4-121">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="df7b4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7b4-122">-DefaultProfile</span></span>
<span data-ttu-id="df7b4-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df7b4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df7b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7b4-124">CommonParameters</span></span>
<span data-ttu-id="df7b4-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7b4-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7b4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7b4-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df7b4-127">INPUTS</span></span>

## <span data-ttu-id="df7b4-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df7b4-128">OUTPUTS</span></span>

### <span data-ttu-id="df7b4-129">Microsoft. Azure. Commands. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="df7b4-129">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="df7b4-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df7b4-130">NOTES</span></span>

## <span data-ttu-id="df7b4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df7b4-131">RELATED LINKS</span></span>

[<span data-ttu-id="df7b4-132">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="df7b4-132">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)


