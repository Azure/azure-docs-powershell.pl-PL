---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 996904a68e8cb55aa4964a6c776064722c63dbab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545519"
---
# <span data-ttu-id="ee000-101">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ee000-101">Get-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="ee000-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee000-102">SYNOPSIS</span></span>
<span data-ttu-id="ee000-103">Pobiera informacje o obszarze nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ee000-103">Gets information about a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee000-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee000-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee000-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee000-105">DESCRIPTION</span></span>
<span data-ttu-id="ee000-106">Polecenie cmdlet **Get-AzureRmNotificationHubsNamespace** pobiera informacje o obszarach nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ee000-106">**The Get-AzureRmNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="ee000-107">To polecenie cmdlet umożliwia uzyskiwanie informacji dotyczących wszystkich obszarów nazw, informacji o obszarach nazw przypisanych do określonej grupy zasobów; lub zwracania informacji o określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="ee000-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>

<span data-ttu-id="ee000-108">Przestrzenie nazw są kontenerami logicznymi, które pomagają organizować Centra powiadomień i zarządzać nimi.</span><span class="sxs-lookup"><span data-stu-id="ee000-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="ee000-109">Musisz mieć co najmniej jeden obszar nazw centrum powiadomień: wszystkie Centra powiadomień muszą być przypisane do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="ee000-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="ee000-110">Jeden obszar nazw może zawierać wiele koncentratorów, co oznacza, że w organizacji może być potrzebny tylko jeden obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="ee000-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="ee000-111">Możesz jednak korzystać z wielu obszarów nazw w celu lepszego organizowania koncentratorów lub nadawać konkretne osobom uprawnienia do zarządzania wybranym podzbiorem koncentratorów.</span><span class="sxs-lookup"><span data-stu-id="ee000-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>

<span data-ttu-id="ee000-112">Polecenie cmdlet **Get-AzureRmNotificationHubsNamespace** zwraca podstawowe informacje o obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="ee000-112">The **Get-AzureRmNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="ee000-113">Aby uzyskać informacje na temat reguł autoryzacji skojarzonych z obszarem nazw, użyj elementu Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="ee000-113">To get information about the authorization rules associated with a namespace use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="ee000-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee000-114">EXAMPLES</span></span>

### <span data-ttu-id="ee000-115">Przykład 1: uzyskiwanie informacji dla wszystkich obszarów nazw centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="ee000-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

<span data-ttu-id="ee000-116">To polecenie zwraca informacje dotyczące wszystkich obszarów nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ee000-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="ee000-117">Przykład 2: uzyskiwanie informacji o jednej przestrzeni nazw centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="ee000-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="ee000-118">To polecenie pobiera informacje dotyczące jednej przestrzeni nazw centrum powiadomień: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="ee000-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="ee000-119">Przykład 3: uzyskiwanie informacji dla wszystkich koncentratorów powiadomień przypisanych do określonego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="ee000-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="ee000-120">To polecenie pobiera informacje dla wszystkich obszarów nazw centrum powiadomień przypisanych do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="ee000-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="ee000-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee000-121">PARAMETERS</span></span>

### <span data-ttu-id="ee000-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee000-122">-DefaultProfile</span></span>
<span data-ttu-id="ee000-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ee000-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee000-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ee000-124">-Namespace</span></span>
<span data-ttu-id="ee000-125">Określa unikatową nazwę obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="ee000-125">Specifies a unique name for the namespace.</span></span>

<span data-ttu-id="ee000-126">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ee000-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee000-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ee000-127">-ResourceGroup</span></span>
<span data-ttu-id="ee000-128">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="ee000-128">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="ee000-129">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="ee000-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee000-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee000-130">CommonParameters</span></span>
<span data-ttu-id="ee000-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee000-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee000-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee000-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee000-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee000-133">INPUTS</span></span>

### <span data-ttu-id="ee000-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ee000-134">None</span></span>
<span data-ttu-id="ee000-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ee000-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee000-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee000-136">OUTPUTS</span></span>

### <span data-ttu-id="ee000-137">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. NotificationHubs. modele. NamespaceAttributes]</span><span class="sxs-lookup"><span data-stu-id="ee000-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes]</span></span>

## <span data-ttu-id="ee000-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee000-138">NOTES</span></span>

## <span data-ttu-id="ee000-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee000-139">RELATED LINKS</span></span>

[<span data-ttu-id="ee000-140">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ee000-140">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="ee000-141">Nowe — AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ee000-141">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="ee000-142">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ee000-142">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="ee000-143">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ee000-143">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


