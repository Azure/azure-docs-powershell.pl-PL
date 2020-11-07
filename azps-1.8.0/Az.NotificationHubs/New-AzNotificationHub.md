---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 9c65ec6f4cf1a8b9c6a8e85b196d4b61b62df09a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708866"
---
# <span data-ttu-id="0488d-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0488d-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="0488d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0488d-102">SYNOPSIS</span></span>
<span data-ttu-id="0488d-103">Tworzy centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0488d-103">Creates a notification hub.</span></span>

## <span data-ttu-id="0488d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0488d-104">SYNTAX</span></span>

### <span data-ttu-id="0488d-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0488d-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0488d-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="0488d-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0488d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0488d-107">DESCRIPTION</span></span>
<span data-ttu-id="0488d-108">Polecenie cmdlet **New-AzNotificationHub** tworzy centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0488d-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="0488d-109">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="0488d-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="0488d-110">Koncentratory powiadomień są w przybliżeniu równoważne z poszczególnymi aplikacjami: każdy z Twoich aplikacji ma zwykle swój własny centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0488d-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="0488d-111">Polecenie cmdlet **New-AzNotificationHub** oferuje dwa sposoby tworzenia nowego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0488d-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="0488d-112">Możesz utworzyć wystąpienie obiektu **NotificationHubAttributes** , a następnie skonfigurować ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="0488d-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="0488d-113">Następnie można skopiować te wartości właściwości do nowego koncentratora za pośrednictwem parametru *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="0488d-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="0488d-114">Możesz również utworzyć plik JSON (notacja JavaScript) zawierający odpowiednie wartości konfiguracji, a następnie zastosować te wartości za pomocą parametru *plik_wejściowy* .</span><span class="sxs-lookup"><span data-stu-id="0488d-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="0488d-115">W przypadku użycia w połączeniu z poleceniem cmdlet **New-AzNotificationHub** w powyższym przykładzie JSON jest tworzony centrum powiadomień o nazwie ContosoNotificationHub znajdujący się na zachodnim centrum danych w Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="0488d-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="0488d-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0488d-116">EXAMPLES</span></span>

### <span data-ttu-id="0488d-117">Przykład 1. Tworzenie centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="0488d-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="0488d-118">To polecenie tworzy centrum powiadomień w obszarze nazw ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="0488d-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="0488d-119">Nowy centrum zostanie przypisany do ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="0488d-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="0488d-120">Nie musisz określać nazwy ani żadnych innych informacji konfiguracyjnych koncentratora; te informacje zostaną pobrane z pliku wejściowego C:\Configurations\InternalHub.jsw dniu.</span><span class="sxs-lookup"><span data-stu-id="0488d-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="0488d-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0488d-121">PARAMETERS</span></span>

### <span data-ttu-id="0488d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0488d-122">-DefaultProfile</span></span>
<span data-ttu-id="0488d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0488d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0488d-124">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="0488d-124">-InputFile</span></span>
<span data-ttu-id="0488d-125">Określa ścieżkę do pliku JSON zawierającego wartości konfiguracji dla nowego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0488d-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="0488d-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0488d-126">-Namespace</span></span>
<span data-ttu-id="0488d-127">Określa obszar nazw, do którego zostanie przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0488d-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="0488d-128">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0488d-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="0488d-129">Centra powiadomień muszą być przypisane do istniejącego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="0488d-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="0488d-130">Polecenie cmdlet **New-AzNotificationHub** nie może utworzyć nowego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="0488d-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="0488d-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="0488d-131">-NotificationHubObj</span></span>
<span data-ttu-id="0488d-132">Określa obiekt **NotificationHubAttributes** , który zawiera informacje o konfiguracji dla nowego koncentratora.</span><span class="sxs-lookup"><span data-stu-id="0488d-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="0488d-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0488d-133">-ResourceGroup</span></span>
<span data-ttu-id="0488d-134">Określa grupę zasobów, do której zostanie przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="0488d-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="0488d-135">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="0488d-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="0488d-136">Musisz użyć istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0488d-136">You must use an existing resource group.</span></span>
<span data-ttu-id="0488d-137">Polecenie cmdlet **New-AzNotificationHub** nie może utworzyć nowej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0488d-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="0488d-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0488d-138">-Confirm</span></span>
<span data-ttu-id="0488d-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0488d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0488d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0488d-140">-WhatIf</span></span>
<span data-ttu-id="0488d-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0488d-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0488d-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0488d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0488d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0488d-143">CommonParameters</span></span>
<span data-ttu-id="0488d-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0488d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0488d-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0488d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0488d-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0488d-146">INPUTS</span></span>

### <span data-ttu-id="0488d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0488d-147">System.String</span></span>

## <span data-ttu-id="0488d-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0488d-148">OUTPUTS</span></span>

### <span data-ttu-id="0488d-149">Microsoft. Azure. Commands. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="0488d-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="0488d-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0488d-150">NOTES</span></span>

## <span data-ttu-id="0488d-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0488d-151">RELATED LINKS</span></span>

[<span data-ttu-id="0488d-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0488d-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="0488d-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0488d-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="0488d-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0488d-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


