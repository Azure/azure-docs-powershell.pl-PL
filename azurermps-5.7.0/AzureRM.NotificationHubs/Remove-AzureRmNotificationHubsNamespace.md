---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2a728cdae95c117e73f38b16cdea5407c1f4954e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542464"
---
# <span data-ttu-id="436d4-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="436d4-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="436d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="436d4-102">SYNOPSIS</span></span>
<span data-ttu-id="436d4-103">Usuwa obszar nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="436d4-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="436d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="436d4-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="436d4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="436d4-105">DESCRIPTION</span></span>
<span data-ttu-id="436d4-106">Polecenie cmdlet **Remove-AzureRmNotificationHubsNamespace** usuwa obszar nazw centrum powiadomień ze swojego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="436d4-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="436d4-107">Przestrzenie nazw są kontenerami logicznymi, które pomagają organizować Centra powiadomień i zarządzać nimi.</span><span class="sxs-lookup"><span data-stu-id="436d4-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="436d4-108">Polecenie cmdlet **Remove-AzureRmNotificationHubsNamespace** usuwa obszar nazw centrum powiadomień ze swojego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="436d4-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="436d4-109">Po uruchomieniu tego polecenia cmdlet określona przestrzeń nazw zostanie usunięta wraz ze wszystkimi koncentratorami powiadomień skojarzonymi z tym obszarem nazw.</span><span class="sxs-lookup"><span data-stu-id="436d4-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="436d4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="436d4-110">EXAMPLES</span></span>

### <span data-ttu-id="436d4-111">Przykład 1: Usuwanie obszaru nazw centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="436d4-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="436d4-112">To polecenie usuwa obszar nazw o nazwie ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="436d4-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="436d4-113">Musisz określić grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="436d4-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="436d4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="436d4-114">PARAMETERS</span></span>

### <span data-ttu-id="436d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="436d4-115">-DefaultProfile</span></span>
<span data-ttu-id="436d4-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="436d4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="436d4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="436d4-117">-Force</span></span>
<span data-ttu-id="436d4-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="436d4-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436d4-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="436d4-119">-Namespace</span></span>
<span data-ttu-id="436d4-120">Określa obszar nazw, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="436d4-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="436d4-121">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="436d4-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="436d4-122">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="436d4-122">-ResourceGroup</span></span>
<span data-ttu-id="436d4-123">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="436d4-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="436d4-124">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="436d4-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="436d4-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="436d4-125">-Confirm</span></span>
<span data-ttu-id="436d4-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="436d4-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436d4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="436d4-127">-WhatIf</span></span>
<span data-ttu-id="436d4-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="436d4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="436d4-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="436d4-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="436d4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="436d4-130">CommonParameters</span></span>
<span data-ttu-id="436d4-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="436d4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="436d4-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="436d4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="436d4-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="436d4-133">INPUTS</span></span>

### <span data-ttu-id="436d4-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="436d4-134">None</span></span>
<span data-ttu-id="436d4-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="436d4-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="436d4-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="436d4-136">OUTPUTS</span></span>

## <span data-ttu-id="436d4-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="436d4-137">NOTES</span></span>

## <span data-ttu-id="436d4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="436d4-138">RELATED LINKS</span></span>

[<span data-ttu-id="436d4-139">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="436d4-139">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="436d4-140">Nowe — AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="436d4-140">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="436d4-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="436d4-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


