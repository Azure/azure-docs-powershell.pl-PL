---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 88ed662dc9938e6d4c9c3caa07ce733530dff6b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951290"
---
# <span data-ttu-id="8c81b-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8c81b-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="8c81b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c81b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c81b-103">Tworzy centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8c81b-103">Creates a notification hub.</span></span>

## <span data-ttu-id="8c81b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c81b-104">SYNTAX</span></span>

### <span data-ttu-id="8c81b-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c81b-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c81b-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c81b-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c81b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c81b-107">DESCRIPTION</span></span>
<span data-ttu-id="8c81b-108">Polecenie **cmdlet New-AzNotificationHub** tworzy centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8c81b-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="8c81b-109">Centra powiadomień są używane do wysyłania powiadomień wypychanych do wielu klientów, niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="8c81b-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="8c81b-110">Centra powiadomień są mniej więcej równoważne poszczególnym aplikacjom: każda z Twoich aplikacji zazwyczaj ma własne centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8c81b-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="8c81b-111">Polecenie **cmdlet New-AzNotificationHub** zapewnia dwa sposoby tworzenia nowego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8c81b-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="8c81b-112">Możesz utworzyć wystąpienie obiektu **NotificationHubAttributes,** a następnie skonfigurować ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="8c81b-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="8c81b-113">Następnie możesz skopiować te wartości właściwości do nowego centrum za pomocą *parametru NotificationHubObj.*</span><span class="sxs-lookup"><span data-stu-id="8c81b-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="8c81b-114">Ewentualnie możesz utworzyć plik JSON (JavaScript Object Notation) zawierający odpowiednie wartości konfiguracyjne, a następnie zastosować te wartości, używając *parametru InputFile.*</span><span class="sxs-lookup"><span data-stu-id="8c81b-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="8c81b-115">W połączeniu z poleceniem cmdlet **New-AzNotificationHub** poprzedni przykład JSON tworzy centrum powiadomień o nazwie ContosoNotificationHub znajdujące się w centrum danych Stanów Zjednoczonych Zachód.</span><span class="sxs-lookup"><span data-stu-id="8c81b-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="8c81b-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c81b-116">EXAMPLES</span></span>

### <span data-ttu-id="8c81b-117">Przykład 1. Tworzenie centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="8c81b-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="8c81b-118">To polecenie tworzy centrum powiadomień w przestrzeni nazw ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="8c81b-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="8c81b-119">Nowe centrum zostanie przypisane do grupy ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="8c81b-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="8c81b-120">Nie trzeba określać nazwy ani żadnych innych informacji o konfiguracji centrum; te informacje zostaną z pliku wejściowego C:\Configurations\InternalHub.jsdalej.</span><span class="sxs-lookup"><span data-stu-id="8c81b-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="8c81b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c81b-121">PARAMETERS</span></span>

### <span data-ttu-id="8c81b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c81b-122">-DefaultProfile</span></span>
<span data-ttu-id="8c81b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8c81b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c81b-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="8c81b-124">-InputFile</span></span>
<span data-ttu-id="8c81b-125">Określa ścieżkę do pliku JSON zawierającego wartości konfiguracyjne dla nowego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8c81b-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c81b-126">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="8c81b-126">-Namespace</span></span>
<span data-ttu-id="8c81b-127">Określa przestrzeń nazw, do której zostanie przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8c81b-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="8c81b-128">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8c81b-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="8c81b-129">Centra powiadomień muszą być przypisane do istniejącej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="8c81b-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="8c81b-130">Polecenie **cmdlet New-AzNotificationHub** nie może utworzyć nowej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="8c81b-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="8c81b-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="8c81b-131">-NotificationHubObj</span></span>
<span data-ttu-id="8c81b-132">Określa obiekt **NotificationHubAttributes** zawierający informacje o konfiguracji dla nowego centrum.</span><span class="sxs-lookup"><span data-stu-id="8c81b-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c81b-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c81b-133">-ResourceGroup</span></span>
<span data-ttu-id="8c81b-134">Określa grupę zasobów, do której zostanie przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8c81b-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="8c81b-135">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c81b-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="8c81b-136">Należy użyć istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c81b-136">You must use an existing resource group.</span></span>
<span data-ttu-id="8c81b-137">Polecenie **cmdlet New-AzNotificationHub** nie może utworzyć nowej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c81b-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="8c81b-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c81b-138">-Confirm</span></span>
<span data-ttu-id="8c81b-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c81b-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c81b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c81b-140">-WhatIf</span></span>
<span data-ttu-id="8c81b-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c81b-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c81b-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c81b-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c81b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c81b-143">CommonParameters</span></span>
<span data-ttu-id="8c81b-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c81b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c81b-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c81b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c81b-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c81b-146">INPUTS</span></span>

### <span data-ttu-id="8c81b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="8c81b-147">System.String</span></span>

## <span data-ttu-id="8c81b-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c81b-148">OUTPUTS</span></span>

### <span data-ttu-id="8c81b-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="8c81b-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="8c81b-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c81b-150">NOTES</span></span>

## <span data-ttu-id="8c81b-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c81b-151">RELATED LINKS</span></span>

[<span data-ttu-id="8c81b-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8c81b-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="8c81b-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8c81b-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="8c81b-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="8c81b-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


