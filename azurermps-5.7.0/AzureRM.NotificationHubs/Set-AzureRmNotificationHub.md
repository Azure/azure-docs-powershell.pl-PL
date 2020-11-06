---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
ms.openlocfilehash: e035cb24c6341eb6d5b3d8aba5cd86b67fdafca2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554109"
---
# <span data-ttu-id="9e897-101">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="9e897-101">Set-AzureRmNotificationHub</span></span>

## <span data-ttu-id="9e897-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e897-102">SYNOPSIS</span></span>
<span data-ttu-id="9e897-103">Ustawia wartości właściwości dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="9e897-103">Sets property values for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e897-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e897-104">SYNTAX</span></span>

### <span data-ttu-id="9e897-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e897-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e897-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e897-106">NotificationHubParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e897-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9e897-107">DESCRIPTION</span></span>
<span data-ttu-id="9e897-108">Polecenie cmdlet **Set-AzureRmNotificationHub** modyfikuje wartości właściwości centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="9e897-108">The **Set-AzureRmNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>

<span data-ttu-id="9e897-109">Wartość właściwości centrum powiadomień można zmodyfikować na dwa sposoby.</span><span class="sxs-lookup"><span data-stu-id="9e897-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="9e897-110">W przypadku jednej z nich można utworzyć wystąpienie obiektu **NotificationHubAttributes** , a następnie skonfigurować te obiekty za pomocą wartości właściwości, które ma mieć nowy koncentrator.</span><span class="sxs-lookup"><span data-stu-id="9e897-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="9e897-111">Można to zrobić za pomocą platformy .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9e897-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="9e897-112">Następnie można skopiować te wartości właściwości do koncentratora za pośrednictwem parametru *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="9e897-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="9e897-113">Możesz też utworzyć plik JSON (notacja JavaScript) zawierający odpowiednie wartości konfiguracji, a następnie zastosować te wartości za pośrednictwem parametru *plik_wejściowy* .</span><span class="sxs-lookup"><span data-stu-id="9e897-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="9e897-114">Plik JSON jest plikiem tekstowym używającym składni podobnej do następującej:</span><span class="sxs-lookup"><span data-stu-id="9e897-114">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="9e897-115">{</span><span class="sxs-lookup"><span data-stu-id="9e897-115">{</span></span>  
    <span data-ttu-id="9e897-116">"Nazwa": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="9e897-116">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="9e897-117">"Lokalizacja": "Zachodnia USA";</span><span class="sxs-lookup"><span data-stu-id="9e897-117">"Location": "West US",</span></span>  
<span data-ttu-id="9e897-118">}</span><span class="sxs-lookup"><span data-stu-id="9e897-118">}</span></span>

<span data-ttu-id="9e897-119">W przypadku użycia w połączeniu z poleceniem cmdlet **Set-AzureRmNotificationHub** Poprzednia przykład JSON ustawia wartość lokalizacji centrum powiadomień o nazwie ContosoNotificationHub na zachodni stan USA.</span><span class="sxs-lookup"><span data-stu-id="9e897-119">When used in conjunction with the **Set-AzureRmNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="9e897-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e897-120">EXAMPLES</span></span>

### <span data-ttu-id="9e897-121">Przykład 1: modyfikowanie wartości właściwości dla centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="9e897-121">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="9e897-122">To polecenie modyfikuje wartości właściwości dla centrum powiadomień znalezionego w przestrzeni nazw ContosoNamespace i przypisał je do ContosoNotificationsGroup grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e897-122">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="9e897-123">Wartości właściwości, a także nazwa koncentratora, który ma zostać zmodyfikowany, nie są określone w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="9e897-123">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="9e897-124">Zamiast tego informacje te są zawarte w pliku wejściowym C:\Configuration\Hubs.jsna.</span><span class="sxs-lookup"><span data-stu-id="9e897-124">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="9e897-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e897-125">PARAMETERS</span></span>

### <span data-ttu-id="9e897-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e897-126">-DefaultProfile</span></span>
<span data-ttu-id="9e897-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9e897-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e897-128">-Force</span><span class="sxs-lookup"><span data-stu-id="9e897-128">-Force</span></span>
<span data-ttu-id="9e897-129">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9e897-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9e897-130">-Plik_wejściowy</span><span class="sxs-lookup"><span data-stu-id="9e897-130">-InputFile</span></span>
<span data-ttu-id="9e897-131">Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji dla centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="9e897-131">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e897-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9e897-132">-Namespace</span></span>
<span data-ttu-id="9e897-133">Określa obszar nazw, do którego jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="9e897-133">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="9e897-134">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="9e897-134">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="9e897-135">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="9e897-135">-NotificationHubObj</span></span>
<span data-ttu-id="9e897-136">Określa obiekt **NotificationHubAttributes** , który zawiera informacje o konfiguracji centrum, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e897-136">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e897-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9e897-137">-ResourceGroup</span></span>
<span data-ttu-id="9e897-138">Określa grupę zasobów, do której jest przypisany centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="9e897-138">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="9e897-139">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="9e897-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="9e897-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e897-140">-Confirm</span></span>
<span data-ttu-id="9e897-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e897-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e897-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e897-142">-WhatIf</span></span>
<span data-ttu-id="9e897-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e897-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e897-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e897-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e897-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e897-145">CommonParameters</span></span>
<span data-ttu-id="9e897-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e897-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e897-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e897-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e897-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e897-148">INPUTS</span></span>

### <span data-ttu-id="9e897-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9e897-149">None</span></span>
<span data-ttu-id="9e897-150">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9e897-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e897-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e897-151">OUTPUTS</span></span>

### <span data-ttu-id="9e897-152">Microsoft. Azure. Commands. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="9e897-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="9e897-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e897-153">NOTES</span></span>

## <span data-ttu-id="9e897-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e897-154">RELATED LINKS</span></span>

[<span data-ttu-id="9e897-155">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="9e897-155">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="9e897-156">Nowe — AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="9e897-156">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="9e897-157">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="9e897-157">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)


