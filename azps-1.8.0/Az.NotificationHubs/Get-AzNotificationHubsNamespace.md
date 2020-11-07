---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: dbb475402ef4068f893cd7d444b5357bf1707578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708870"
---
# <span data-ttu-id="a15ea-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a15ea-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="a15ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a15ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a15ea-103">Pobiera informacje o obszarze nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a15ea-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="a15ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a15ea-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a15ea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a15ea-105">DESCRIPTION</span></span>
<span data-ttu-id="a15ea-106">Polecenie cmdlet **Get-AzNotificationHubsNamespace** pobiera informacje o obszarach nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a15ea-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="a15ea-107">To polecenie cmdlet umożliwia uzyskiwanie informacji dotyczących wszystkich obszarów nazw, informacji o obszarach nazw przypisanych do określonej grupy zasobów; lub zwracania informacji o określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="a15ea-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="a15ea-108">Przestrzenie nazw są kontenerami logicznymi, które pomagają organizować Centra powiadomień i zarządzać nimi.</span><span class="sxs-lookup"><span data-stu-id="a15ea-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="a15ea-109">Musisz mieć co najmniej jeden obszar nazw centrum powiadomień: wszystkie Centra powiadomień muszą być przypisane do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a15ea-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="a15ea-110">Jeden obszar nazw może zawierać wiele koncentratorów, co oznacza, że w organizacji może być potrzebny tylko jeden obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="a15ea-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="a15ea-111">Możesz jednak korzystać z wielu obszarów nazw w celu lepszego organizowania koncentratorów lub nadawać konkretne osobom uprawnienia do zarządzania wybranym podzbiorem koncentratorów.</span><span class="sxs-lookup"><span data-stu-id="a15ea-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="a15ea-112">Polecenie cmdlet **Get-AzNotificationHubsNamespace** zwraca podstawowe informacje o obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="a15ea-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="a15ea-113">Aby uzyskać informacje na temat reguł autoryzacji skojarzonych z obszarem nazw, użyj elementu Get-AzNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="a15ea-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="a15ea-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a15ea-114">EXAMPLES</span></span>

### <span data-ttu-id="a15ea-115">Przykład 1: uzyskiwanie informacji dla wszystkich obszarów nazw centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="a15ea-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="a15ea-116">To polecenie zwraca informacje dotyczące wszystkich obszarów nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a15ea-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="a15ea-117">Przykład 2: uzyskiwanie informacji o jednej przestrzeni nazw centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="a15ea-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="a15ea-118">To polecenie pobiera informacje dotyczące jednej przestrzeni nazw centrum powiadomień: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="a15ea-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="a15ea-119">Przykład 3: uzyskiwanie informacji dla wszystkich koncentratorów powiadomień przypisanych do określonego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="a15ea-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="a15ea-120">To polecenie pobiera informacje dla wszystkich obszarów nazw centrum powiadomień przypisanych do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="a15ea-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="a15ea-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a15ea-121">PARAMETERS</span></span>

### <span data-ttu-id="a15ea-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a15ea-122">-DefaultProfile</span></span>
<span data-ttu-id="a15ea-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a15ea-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a15ea-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a15ea-124">-Namespace</span></span>
<span data-ttu-id="a15ea-125">Określa unikatową nazwę obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a15ea-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="a15ea-126">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="a15ea-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a15ea-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a15ea-127">-ResourceGroup</span></span>
<span data-ttu-id="a15ea-128">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="a15ea-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="a15ea-129">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="a15ea-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a15ea-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a15ea-130">CommonParameters</span></span>
<span data-ttu-id="a15ea-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a15ea-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a15ea-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a15ea-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a15ea-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a15ea-133">INPUTS</span></span>

### <span data-ttu-id="a15ea-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a15ea-134">System.String</span></span>

## <span data-ttu-id="a15ea-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a15ea-135">OUTPUTS</span></span>

### <span data-ttu-id="a15ea-136">Microsoft. Azure. Commands. NotificationHubs. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a15ea-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="a15ea-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a15ea-137">NOTES</span></span>

## <span data-ttu-id="a15ea-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a15ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="a15ea-139">Get-AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a15ea-139">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="a15ea-140">Nowe — AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a15ea-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="a15ea-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a15ea-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="a15ea-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a15ea-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)

