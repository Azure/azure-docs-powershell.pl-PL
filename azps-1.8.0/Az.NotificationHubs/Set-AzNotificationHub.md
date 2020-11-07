---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: f59ac6a2e1431c3ba04ff0ac9cf9cafbfdfe367e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708848"
---
# <span data-ttu-id="978f3-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="978f3-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="978f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="978f3-102">SYNOPSIS</span></span>
<span data-ttu-id="978f3-103">Ustawia wartości właściwości dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="978f3-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="978f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="978f3-104">SYNTAX</span></span>

### <span data-ttu-id="978f3-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="978f3-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="978f3-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="978f3-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="978f3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="978f3-107">DESCRIPTION</span></span>
<span data-ttu-id="978f3-108">Polecenie cmdlet **Set-AzNotificationHub** modyfikuje wartości właściwości centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="978f3-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="978f3-109">Wartość właściwości centrum powiadomień można zmodyfikować na dwa sposoby.</span><span class="sxs-lookup"><span data-stu-id="978f3-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="978f3-110">W przypadku jednej z nich można utworzyć wystąpienie obiektu **NotificationHubAttributes** , a następnie skonfigurować te obiekty za pomocą wartości właściwości, które ma mieć nowy koncentrator.</span><span class="sxs-lookup"><span data-stu-id="978f3-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="978f3-111">Można to zrobić za pomocą platformy .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="978f3-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="978f3-112">Następnie można skopiować te wartości właściwości do koncentratora za pośrednictwem parametru *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="978f3-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="978f3-113">Możesz też utworzyć plik JSON (notacja JavaScript) zawierający odpowiednie wartości konfiguracji, a następnie zastosować te wartości za pośrednictwem parametru *plik_wejściowy* .</span><span class="sxs-lookup"><span data-stu-id="978f3-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="978f3-114">Plik JSON jest plikiem tekstowym używającym składni podobnej do następującej: {</span><span class="sxs-lookup"><span data-stu-id="978f3-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="978f3-115">"Nazwa": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="978f3-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="978f3-116">"Lokalizacja": "Zachodnia USA";</span><span class="sxs-lookup"><span data-stu-id="978f3-116">"Location": "West US",</span></span>  
<span data-ttu-id="978f3-117">} Gdy jest używana w połączeniu z poleceniem cmdlet **Set-AzNotificationHub** , poprzednia przykład JSON ustawia wartość lokalizacji centrum powiadomień o nazwie ContosoNotificationHub na zachodni stan USA.</span><span class="sxs-lookup"><span data-stu-id="978f3-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="978f3-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="978f3-118">EXAMPLES</span></span>

### <span data-ttu-id="978f3-119">Przykład 1: modyfikowanie wartości właściwości dla centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="978f3-119">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="978f3-120">To polecenie modyfikuje wartości właściwości dla centrum powiadomień znalezionego w przestrzeni nazw ContosoNamespace i przypisał je do ContosoNotificationsGroup grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="978f3-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="978f3-121">Wartości właściwości, a także nazwa koncentratora, który ma zostać zmodyfikowany, nie są określone w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="978f3-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="978f3-122">Zamiast tego informacje te są zawarte w pliku wejściowym C:\Configuration\Hubs.jsna.</span><span class="sxs-lookup"><span data-stu-id="978f3-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="978f3-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="978f3-123">PARAMETERS</span></span>

### <span data-ttu-id="978f3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978f3-124">-DefaultProfile</span></span>
<span data-ttu-id="978f3-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="978f3-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="978f3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="978f3-126">-Force</span></span>
<span data-ttu-id="978f3-127">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="978f3-127">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978f3-128">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="978f3-128">-InputFile</span></span>
<span data-ttu-id="978f3-129">Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="978f3-129">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="978f3-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="978f3-130">-Namespace</span></span>
<span data-ttu-id="978f3-131">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="978f3-131">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="978f3-132">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="978f3-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="978f3-133">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="978f3-133">-NotificationHubObj</span></span>
<span data-ttu-id="978f3-134">Określa obiekt **NotificationHubAttributes** , który zawiera informacje o konfiguracji centrum, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="978f3-134">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="978f3-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="978f3-135">-ResourceGroup</span></span>
<span data-ttu-id="978f3-136">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="978f3-136">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="978f3-137">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="978f3-137">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="978f3-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="978f3-138">-Confirm</span></span>
<span data-ttu-id="978f3-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="978f3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978f3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978f3-140">-WhatIf</span></span>
<span data-ttu-id="978f3-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="978f3-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="978f3-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="978f3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978f3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978f3-143">CommonParameters</span></span>
<span data-ttu-id="978f3-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978f3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978f3-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="978f3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978f3-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="978f3-146">INPUTS</span></span>

### <span data-ttu-id="978f3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="978f3-147">System.String</span></span>

## <span data-ttu-id="978f3-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="978f3-148">OUTPUTS</span></span>

### <span data-ttu-id="978f3-149">Microsoft. Azure. Commands. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="978f3-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="978f3-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="978f3-150">NOTES</span></span>

## <span data-ttu-id="978f3-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="978f3-151">RELATED LINKS</span></span>

[<span data-ttu-id="978f3-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="978f3-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="978f3-153">Nowe — AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="978f3-153">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="978f3-154">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="978f3-154">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


