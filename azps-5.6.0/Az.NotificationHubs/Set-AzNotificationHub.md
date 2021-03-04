---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7f0732225389f5174c2097cea57ed38d9ea2be0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951121"
---
# <span data-ttu-id="fbe95-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fbe95-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="fbe95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe95-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe95-103">Ustawia wartości właściwości centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fbe95-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="fbe95-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fbe95-104">SYNTAX</span></span>

### <span data-ttu-id="fbe95-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbe95-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe95-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbe95-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe95-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fbe95-107">DESCRIPTION</span></span>
<span data-ttu-id="fbe95-108">Polecenie **cmdlet Set-AzNotificationHub** modyfikuje wartości właściwości centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fbe95-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="fbe95-109">Wartość właściwości centrum powiadomień można modyfikować na dwa sposoby.</span><span class="sxs-lookup"><span data-stu-id="fbe95-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="fbe95-110">Na przykład możesz utworzyć wystąpienie obiektu **NotificationHubAttributes,** a następnie skonfigurować ten obiekt przy użyciu wartości właściwości, które ma posiadać nowe centrum.</span><span class="sxs-lookup"><span data-stu-id="fbe95-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="fbe95-111">Można to zrobić za pośrednictwem .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fbe95-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="fbe95-112">Następnie możesz skopiować te wartości właściwości do centrum za pomocą *parametru NotificationHubObj.*</span><span class="sxs-lookup"><span data-stu-id="fbe95-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="fbe95-113">Ewentualnie możesz utworzyć plik JSON (JavaScript Object Notation) zawierający odpowiednie wartości konfiguracyjne, a następnie zastosować te wartości za pomocą *parametru InputFile.*</span><span class="sxs-lookup"><span data-stu-id="fbe95-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="fbe95-114">Plik JSON to plik tekstowy o składni podobnej do następującej: {</span><span class="sxs-lookup"><span data-stu-id="fbe95-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="fbe95-115">"Name": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="fbe95-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="fbe95-116">"Lokalizacja": "Zachód USA",</span><span class="sxs-lookup"><span data-stu-id="fbe95-116">"Location": "West US",</span></span>  
<span data-ttu-id="fbe95-117">} W połączeniu z poleceniem cmdlet **Set-AzNotificationHub** poprzedni przykład JSON ustawia wartość Lokalizacji centrum powiadomień o nazwie ContosoNotificationHub na wartość Zachód STANÓW ZJEDNOCZONYCH.</span><span class="sxs-lookup"><span data-stu-id="fbe95-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="fbe95-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fbe95-118">EXAMPLES</span></span>

### <span data-ttu-id="fbe95-119">Przykład 1. Modyfikowanie wartości właściwości centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="fbe95-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="fbe95-120">To polecenie modyfikuje wartości właściwości centrum powiadomień w przestrzeni nazw ContosoNamespace i przypisało je do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="fbe95-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="fbe95-121">Wartości właściwości, a także nazwa centrum do zmodyfikowania, nie są określone w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="fbe95-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="fbe95-122">Zamiast tego te informacje są zawarte w pliku wejściowym, C:\Configuration\Hubs.jsdalej.</span><span class="sxs-lookup"><span data-stu-id="fbe95-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="fbe95-123">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fbe95-123">Example 2</span></span>

<span data-ttu-id="fbe95-124">Ustawia wartości właściwości centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fbe95-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="fbe95-125">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="fbe95-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="fbe95-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbe95-126">PARAMETERS</span></span>

### <span data-ttu-id="fbe95-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe95-127">-DefaultProfile</span></span>
<span data-ttu-id="fbe95-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fbe95-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbe95-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="fbe95-129">-Force</span></span>
<span data-ttu-id="fbe95-130">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fbe95-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fbe95-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="fbe95-131">-InputFile</span></span>
<span data-ttu-id="fbe95-132">Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fbe95-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="fbe95-133">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="fbe95-133">-Namespace</span></span>
<span data-ttu-id="fbe95-134">Określa przestrzeń nazw, do której jest przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fbe95-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="fbe95-135">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fbe95-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="fbe95-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="fbe95-136">-NotificationHubObj</span></span>
<span data-ttu-id="fbe95-137">Określa obiekt **NotificationHubAttributes** zawierający informacje o konfiguracji centrum, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="fbe95-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fbe95-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fbe95-138">-ResourceGroup</span></span>
<span data-ttu-id="fbe95-139">Określa grupę zasobów, do której jest przypisane centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="fbe95-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="fbe95-140">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe95-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="fbe95-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbe95-141">-Confirm</span></span>
<span data-ttu-id="fbe95-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fbe95-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe95-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe95-143">-WhatIf</span></span>
<span data-ttu-id="fbe95-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbe95-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbe95-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fbe95-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe95-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe95-146">CommonParameters</span></span>
<span data-ttu-id="fbe95-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe95-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe95-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe95-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe95-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbe95-149">INPUTS</span></span>

### <span data-ttu-id="fbe95-150">System.String</span><span class="sxs-lookup"><span data-stu-id="fbe95-150">System.String</span></span>

## <span data-ttu-id="fbe95-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbe95-151">OUTPUTS</span></span>

### <span data-ttu-id="fbe95-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="fbe95-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="fbe95-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fbe95-153">NOTES</span></span>

## <span data-ttu-id="fbe95-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbe95-154">RELATED LINKS</span></span>

[<span data-ttu-id="fbe95-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fbe95-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="fbe95-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fbe95-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="fbe95-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fbe95-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


