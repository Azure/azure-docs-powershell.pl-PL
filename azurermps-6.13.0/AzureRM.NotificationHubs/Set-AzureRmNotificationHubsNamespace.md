---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2fb349628a686bb96df5685bff8a4329c0173212
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544971"
---
# <span data-ttu-id="c4594-101">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c4594-101">Set-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="c4594-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4594-102">SYNOPSIS</span></span>
<span data-ttu-id="c4594-103">Ustawia wartości właściwości dla obszaru nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c4594-103">Sets property values for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4594-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4594-104">SYNTAX</span></span>

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4594-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c4594-105">DESCRIPTION</span></span>
<span data-ttu-id="c4594-106">Polecenie cmdlet **Set-AzureRmNotificationHubsNamespace** ustawia wartości właściwości istniejącej przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c4594-106">The **Set-AzureRmNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="c4594-107">Przestrzenie nazw są kontenerami logicznymi, które pomagają organizować Centra powiadomień i zarządzać nimi.</span><span class="sxs-lookup"><span data-stu-id="c4594-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="c4594-108">Musisz mieć co najmniej jeden obszar nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c4594-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="c4594-109">Ponadto wszystkie Centra powiadomień muszą mieć przypisany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="c4594-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="c4594-110">To polecenie cmdlet służy głównie do włączania i wyłączania obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="c4594-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="c4594-111">Gdy obszar nazw jest wyłączony, użytkownicy nie mogą nawiązywać połączeń z żadnymi koncentratorami powiadomień w obszarze nazw ani Administratorzy mogą używać tych koncentratorów do wysyłania powiadomień wypychanych.</span><span class="sxs-lookup"><span data-stu-id="c4594-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="c4594-112">Aby ponownie włączyć wyłączony obszar nazw, użyj tego polecenia cmdlet w celu ustawienia właściwości **State** obszaru nazw na wartość aktywny.</span><span class="sxs-lookup"><span data-stu-id="c4594-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="c4594-113">Możesz również użyć tego polecenia cmdlet, aby oznaczyć obszar nazw jako krytyczny.</span><span class="sxs-lookup"><span data-stu-id="c4594-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="c4594-114">Uniemożliwia to usunięcie przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="c4594-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="c4594-115">Aby usunąć krytyczny obszar nazw, należy najpierw usunąć znacznik krytyczne.</span><span class="sxs-lookup"><span data-stu-id="c4594-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="c4594-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4594-116">EXAMPLES</span></span>

### <span data-ttu-id="c4594-117">Przykład 1. wyłączenie obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="c4594-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="c4594-118">To polecenie wyłącza obszar nazw o nazwie ContosoPartners, który znajduje się na zachodnim centrum danych w Stanach Zjednoczonych i jest przypisany do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="c4594-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="c4594-119">Przykład 2: Włączanie obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="c4594-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="c4594-120">To polecenie umożliwia włączenie obszaru nazw o nazwie ContosoPartners, który znajduje się w zachodnim centrum danych w Stanach Zjednoczonych i przypisany do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="c4594-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="c4594-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4594-121">PARAMETERS</span></span>

### <span data-ttu-id="c4594-122">— Krytyczne</span><span class="sxs-lookup"><span data-stu-id="c4594-122">-Critical</span></span>
<span data-ttu-id="c4594-123">Wskazuje, czy obszar nazw jest krytycznym obszarem nazw.</span><span class="sxs-lookup"><span data-stu-id="c4594-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="c4594-124">Nie można usuwać krytycznych obszarów nazw.</span><span class="sxs-lookup"><span data-stu-id="c4594-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="c4594-125">Aby usunąć krytyczny obszar nazw, należy ustawić wartość FAŁSZ dla tej właściwości w celu oznaczenia obszaru nazw jako niekrytycznego.</span><span class="sxs-lookup"><span data-stu-id="c4594-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4594-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4594-126">-DefaultProfile</span></span>
<span data-ttu-id="c4594-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c4594-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4594-128">-Force</span><span class="sxs-lookup"><span data-stu-id="c4594-128">-Force</span></span>
<span data-ttu-id="c4594-129">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c4594-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c4594-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c4594-130">-Location</span></span>
<span data-ttu-id="c4594-131">Określa nazwę wyświetlaną centrum danych, w którym znajduje się obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="c4594-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="c4594-132">Ten parametr można ustawić na dowolną prawidłową lokalizację platformy Azure, co zapewnia optymalną wydajność, dlatego należy korzystać z centrum danych w pobliżu większości użytkowników.</span><span class="sxs-lookup"><span data-stu-id="c4594-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="c4594-133">Aby uzyskać aktualną listę lokalizacji na platformie Azure, uruchom następujące polecenie: `Get-AzureLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="c4594-133">To get an up-to-date list of Azure locations run the following command: `Get-AzureLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="c4594-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c4594-134">-Namespace</span></span>
<span data-ttu-id="c4594-135">Określa obszar nazw, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4594-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="c4594-136">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="c4594-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="c4594-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c4594-137">-ResourceGroup</span></span>
<span data-ttu-id="c4594-138">Określa grupę zasobów, do której przypisano obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="c4594-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="c4594-139">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.</span><span class="sxs-lookup"><span data-stu-id="c4594-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c4594-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c4594-140">-SkuTier</span></span>
<span data-ttu-id="c4594-141">Warstwa SKU obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="c4594-141">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4594-142">-State</span><span class="sxs-lookup"><span data-stu-id="c4594-142">-State</span></span>
<span data-ttu-id="c4594-143">Określa bieżący stan obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="c4594-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="c4594-144">Dopuszczalne wartości tego parametru to: aktywny i wyłączony.</span><span class="sxs-lookup"><span data-stu-id="c4594-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4594-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4594-145">-Tag</span></span>
<span data-ttu-id="c4594-146">Określa pary nazwa-wartość, których można użyć do kategoryzowania i organizowania elementów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c4594-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="c4594-147">Funkcja Tagi podobna do słów kluczowych i działa w ramach wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c4594-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="c4594-148">Jeśli na przykład wyszukiwane są wszystkie elementy z działem znaczników: funkcja wyszukiwania zwróci wszystkie elementy platformy Azure, które mają ten tag, niezależnie od tego, jakie elementy są takie jak typ elementu, lokalizacja lub Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4594-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="c4594-149">Pojedynczy znacznik składa się z dwóch części: *nazwy* i (opcjonalnie) *wartości*.</span><span class="sxs-lookup"><span data-stu-id="c4594-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="c4594-150">Na przykład w dziale:, nazwa znacznika to dział, a jego wartość to znacznik.</span><span class="sxs-lookup"><span data-stu-id="c4594-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="c4594-151">Aby dodać znacznik, użyj składni tabeli skrótów podobnej do tego, co spowoduje utworzenie znacznika CalendarYear: 2016:-Tagi @ {Name = "CalendarYear"; Value = "2016"} aby dodać wiele tagów w tym samym poleceniu, oddziel poszczególne Tagi za pomocą przecinków:-tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "FiscalYear"; Wartość = "2017"}</span><span class="sxs-lookup"><span data-stu-id="c4594-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4594-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4594-152">-Confirm</span></span>
<span data-ttu-id="c4594-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4594-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4594-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4594-154">-WhatIf</span></span>
<span data-ttu-id="c4594-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4594-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4594-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4594-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4594-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4594-157">CommonParameters</span></span>
<span data-ttu-id="c4594-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4594-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4594-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4594-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4594-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4594-160">INPUTS</span></span>

### <span data-ttu-id="c4594-161">System. String</span><span class="sxs-lookup"><span data-stu-id="c4594-161">System.String</span></span>

### <span data-ttu-id="c4594-162">Microsoft. Azure. Commands. NotificationHubs. models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="c4594-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="c4594-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4594-163">System.Boolean</span></span>

### <span data-ttu-id="c4594-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c4594-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c4594-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4594-165">OUTPUTS</span></span>

### <span data-ttu-id="c4594-166">Microsoft. Azure. Commands. NotificationHubs. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c4594-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="c4594-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4594-167">NOTES</span></span>

## <span data-ttu-id="c4594-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4594-168">RELATED LINKS</span></span>

[<span data-ttu-id="c4594-169">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c4594-169">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="c4594-170">Nowe — AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c4594-170">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="c4594-171">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="c4594-171">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)


