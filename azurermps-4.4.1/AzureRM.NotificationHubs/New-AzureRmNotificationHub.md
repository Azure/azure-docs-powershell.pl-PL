---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 33dfd5a8c4bde0405351315543078558a5832aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527366"
---
# <span data-ttu-id="f47da-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f47da-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="f47da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f47da-102">SYNOPSIS</span></span>
<span data-ttu-id="f47da-103">Tworzy centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f47da-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f47da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f47da-104">SYNTAX</span></span>

### <span data-ttu-id="f47da-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f47da-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f47da-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="f47da-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f47da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f47da-107">DESCRIPTION</span></span>
<span data-ttu-id="f47da-108">Polecenie cmdlet **New-AzureRmNotificationHub** tworzy centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f47da-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="f47da-109">Centra powiadomień służą do wysyłania powiadomień wypychanych do wielu klientów niezależnie od platformy używanej przez tych klientów.</span><span class="sxs-lookup"><span data-stu-id="f47da-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="f47da-110">Koncentratory powiadomień są w przybliżeniu równoważne z poszczególnymi aplikacjami: każdy z Twoich aplikacji ma zwykle swój własny centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f47da-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="f47da-111">Polecenie cmdlet **New-AzureRmNotificationHub** oferuje dwa sposoby tworzenia nowego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f47da-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="f47da-112">Możesz utworzyć wystąpienie obiektu **NotificationHubAttributes** , a następnie skonfigurować ten obiekt.</span><span class="sxs-lookup"><span data-stu-id="f47da-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="f47da-113">Następnie można skopiować te wartości właściwości do nowego koncentratora za pośrednictwem parametru *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="f47da-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="f47da-114">Możesz również utworzyć plik JSON (notacja JavaScript) zawierający odpowiednie wartości konfiguracji, a następnie zastosować te wartości za pomocą parametru *plik_wejściowy* .</span><span class="sxs-lookup"><span data-stu-id="f47da-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>

<span data-ttu-id="f47da-115">W przypadku użycia w połączeniu z poleceniem cmdlet **New-AzureRmNotificationHub** w powyższym przykładzie JSON jest tworzony centrum powiadomień o nazwie ContosoNotificationHub znajdujący się na zachodnim centrum danych w Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="f47da-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="f47da-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f47da-116">EXAMPLES</span></span>

### <span data-ttu-id="f47da-117">Przykład 1. Tworzenie centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="f47da-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="f47da-118">To polecenie tworzy centrum powiadomień w obszarze nazw ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="f47da-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="f47da-119">Nowy centrum zostanie przypisany do ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="f47da-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="f47da-120">Nie musisz określać nazwy ani żadnych innych informacji konfiguracyjnych koncentratora; te informacje zostaną pobrane z pliku wejściowego C:\Configurations\InternalHub.jsw dniu.</span><span class="sxs-lookup"><span data-stu-id="f47da-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="f47da-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f47da-121">PARAMETERS</span></span>

### <span data-ttu-id="f47da-122">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="f47da-122">-InputFile</span></span>
<span data-ttu-id="f47da-123">Określa ścieżkę do pliku JSON zawierającego wartości konfiguracji dla nowego centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f47da-123">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="f47da-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f47da-124">-Namespace</span></span>
<span data-ttu-id="f47da-125">Określa obszar nazw, do którego zostanie przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f47da-125">Specifies the namespace to which the notification hub will be assigned.</span></span>

<span data-ttu-id="f47da-126">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f47da-126">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="f47da-127">Centra powiadomień muszą być przypisane do istniejącego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f47da-127">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="f47da-128">Polecenie cmdlet **New-AzureRmNotificationHub** nie może utworzyć nowego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f47da-128">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="f47da-129">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="f47da-129">-NotificationHubObj</span></span>
<span data-ttu-id="f47da-130">Określa obiekt **NotificationHubAttributes** , który zawiera informacje o konfiguracji dla nowego koncentratora.</span><span class="sxs-lookup"><span data-stu-id="f47da-130">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="f47da-131">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f47da-131">-ResourceGroup</span></span>
<span data-ttu-id="f47da-132">Określa grupę zasobów, do której zostanie przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f47da-132">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="f47da-133">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="f47da-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="f47da-134">Musisz użyć istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f47da-134">You must use an existing resource group.</span></span>
<span data-ttu-id="f47da-135">Polecenie cmdlet **New-AzureRmNotificationHub** nie może utworzyć nowej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f47da-135">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="f47da-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f47da-136">-Confirm</span></span>
<span data-ttu-id="f47da-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f47da-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f47da-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f47da-138">-WhatIf</span></span>
<span data-ttu-id="f47da-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f47da-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f47da-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f47da-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f47da-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47da-141">-DefaultProfile</span></span>
<span data-ttu-id="f47da-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f47da-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f47da-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47da-143">CommonParameters</span></span>
<span data-ttu-id="f47da-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f47da-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47da-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f47da-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47da-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f47da-146">INPUTS</span></span>

## <span data-ttu-id="f47da-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f47da-147">OUTPUTS</span></span>

### <span data-ttu-id="f47da-148">Microsoft. Azure. Commands. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f47da-148">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="f47da-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f47da-149">NOTES</span></span>

## <span data-ttu-id="f47da-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f47da-150">RELATED LINKS</span></span>

[<span data-ttu-id="f47da-151">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f47da-151">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="f47da-152">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f47da-152">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="f47da-153">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f47da-153">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


