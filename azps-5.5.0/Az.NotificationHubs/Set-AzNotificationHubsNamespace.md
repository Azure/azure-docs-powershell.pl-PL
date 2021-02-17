---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191490"
---
# <span data-ttu-id="f74be-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f74be-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="f74be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f74be-102">SYNOPSIS</span></span>
<span data-ttu-id="f74be-103">Ustawia wartości właściwości przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f74be-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="f74be-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f74be-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f74be-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f74be-105">DESCRIPTION</span></span>
<span data-ttu-id="f74be-106">Polecenie **cmdlet Set-AzNotificationHubsNamespace** ustawia wartości właściwości istniejącej przestrzeni nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f74be-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="f74be-107">Przestrzenie nazw to kontenery logiczne, które ułatwiają organizowanie centrum powiadomień i zarządzanie nimi.</span><span class="sxs-lookup"><span data-stu-id="f74be-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="f74be-108">Musisz mieć co najmniej jedną przestrzeń nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f74be-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="f74be-109">Ponadto wszystkie centra powiadomień muszą mieć przypisaną przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="f74be-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="f74be-110">To polecenie cmdlet służy głównie do włączania i wyłączania przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f74be-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="f74be-111">Gdy przestrzeń nazw jest wyłączona, użytkownicy nie mogą łączyć się z żadnymi centrum powiadomień w przestrzeni nazw ani za pomocą tych centrum nie mogą wysyłać powiadomień wypychanych.</span><span class="sxs-lookup"><span data-stu-id="f74be-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="f74be-112">Aby ponownie włączyć wyłączną przestrzeń nazw, użyj tego polecenia cmdlet, aby ustawić właściwość **Województwo** przestrzeni nazw na Wartość aktywna.</span><span class="sxs-lookup"><span data-stu-id="f74be-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="f74be-113">To polecenie cmdlet umożliwia również otagowanie przestrzeni nazw jako krytycznej.</span><span class="sxs-lookup"><span data-stu-id="f74be-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="f74be-114">Zapobiega to usunięciu przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f74be-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="f74be-115">Aby usunąć krytyczną przestrzeń nazw, należy najpierw usunąć tag Krytyczne.</span><span class="sxs-lookup"><span data-stu-id="f74be-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="f74be-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f74be-116">EXAMPLES</span></span>

### <span data-ttu-id="f74be-117">Przykład 1. Wyłączanie przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="f74be-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="f74be-118">To polecenie wyłącza przestrzeń nazw o nazwie ContosoPartners znajdującą się w centrum danych Stanów Zjednoczonych Zachód i przypisaną do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="f74be-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="f74be-119">Przykład 2. Włączanie przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="f74be-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="f74be-120">To polecenie umożliwia przestrzeni nazw o nazwie ContosoPartners znajdującej się w centrum danych Stanów Zjednoczonych Zachód i przypisanej do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="f74be-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="f74be-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f74be-121">PARAMETERS</span></span>

### <span data-ttu-id="f74be-122">— Krytyczne</span><span class="sxs-lookup"><span data-stu-id="f74be-122">-Critical</span></span>
<span data-ttu-id="f74be-123">Wskazuje, czy przestrzeń nazw jest krytyczną przestrzenią nazw.</span><span class="sxs-lookup"><span data-stu-id="f74be-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="f74be-124">Krytycznych przestrzeni nazw nie można usunąć.</span><span class="sxs-lookup"><span data-stu-id="f74be-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="f74be-125">Aby usunąć krytyczną przestrzeń nazw, należy ustawić wartość tej właściwości na Fałsz, aby oznaczyć przestrzeń nazw jako niekrytykową.</span><span class="sxs-lookup"><span data-stu-id="f74be-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

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

### <span data-ttu-id="f74be-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74be-126">-DefaultProfile</span></span>
<span data-ttu-id="f74be-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f74be-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f74be-128">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f74be-128">-Force</span></span>
<span data-ttu-id="f74be-129">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f74be-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f74be-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f74be-130">-Location</span></span>
<span data-ttu-id="f74be-131">Określa nazwę wyświetlaną centrum danych hostatora przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f74be-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="f74be-132">Ten parametr można ustawić na dowolną prawidłową lokalizację na platformie Azure, ale w celu uzyskania optymalnej wydajności należy użyć centrum danych znajdującego się w pobliżu większości użytkowników.</span><span class="sxs-lookup"><span data-stu-id="f74be-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="f74be-133">Aby uzyskać dostęp do aktualnej listy lokalizacji platformy Azure, uruchom następujące polecenie: `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="f74be-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="f74be-134">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="f74be-134">-Namespace</span></span>
<span data-ttu-id="f74be-135">Określa przestrzeń nazw, która jest zmieniana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f74be-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="f74be-136">Przestrzenie nazw zapewniają sposób grupowania i kategoryzowania centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="f74be-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f74be-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f74be-137">-ResourceGroup</span></span>
<span data-ttu-id="f74be-138">Określa grupę zasobów, do której jest przypisana przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="f74be-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="f74be-139">Grupy zasobów organizują elementy, takie jak przestrzenie nazw, centra powiadomień i reguły autoryzacji, w sposób ułatwiający po prostu zarządzanie zapasami i administrowanie platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f74be-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f74be-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f74be-140">-SkuTier</span></span>
<span data-ttu-id="f74be-141">Warstwa SKU przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="f74be-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="f74be-142">— województwo</span><span class="sxs-lookup"><span data-stu-id="f74be-142">-State</span></span>
<span data-ttu-id="f74be-143">Określa bieżący stan przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="f74be-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="f74be-144">Dopuszczalne wartości dla tego parametru to: Aktywny i Wyłączony.</span><span class="sxs-lookup"><span data-stu-id="f74be-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

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

### <span data-ttu-id="f74be-145">— Tag</span><span class="sxs-lookup"><span data-stu-id="f74be-145">-Tag</span></span>
<span data-ttu-id="f74be-146">Określa pary nazwa-wartość, których można używać do kategoryzowania i organizowania elementów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f74be-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="f74be-147">Tagi działają podobnie do słów kluczowych i działają we wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="f74be-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="f74be-148">Jeśli na przykład wyszukuje się wszystkie elementy z tagiem Department:IT, wyszukiwanie zwróci wszystkie elementy platformy Azure, które mają ten tag, bez względu na elementy, takie jak typ elementu, lokalizacja lub grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="f74be-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="f74be-149">Pojedynczy tag składa się z dwóch części: *nazwa* i (opcjonalnie) *wartość.*</span><span class="sxs-lookup"><span data-stu-id="f74be-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="f74be-150">Na przykład w dziale dział:IT nazwa tagu to Dział, a wartością tagu jest IT.</span><span class="sxs-lookup"><span data-stu-id="f74be-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="f74be-151">Aby dodać tag, użyj składni tabeli skrótów podobnej do tej, co powoduje utworzenie tagu Rok_kalendarza:2016: -Tagi @{Name="Rok_kalendarza"; Value="2016"} Aby dodać wiele tagów za pomocą tego samego polecenia, oddziel poszczególne tagi przecinkami: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="Rok Obrachunkowy"; Value="2017"}</span><span class="sxs-lookup"><span data-stu-id="f74be-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

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

### <span data-ttu-id="f74be-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f74be-152">-Confirm</span></span>
<span data-ttu-id="f74be-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f74be-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f74be-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f74be-154">-WhatIf</span></span>
<span data-ttu-id="f74be-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f74be-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f74be-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f74be-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f74be-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74be-157">CommonParameters</span></span>
<span data-ttu-id="f74be-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f74be-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74be-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f74be-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74be-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f74be-160">INPUTS</span></span>

### <span data-ttu-id="f74be-161">System.String</span><span class="sxs-lookup"><span data-stu-id="f74be-161">System.String</span></span>

### <span data-ttu-id="f74be-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span><span class="sxs-lookup"><span data-stu-id="f74be-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="f74be-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f74be-163">System.Boolean</span></span>

### <span data-ttu-id="f74be-164">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f74be-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f74be-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f74be-165">OUTPUTS</span></span>

### <span data-ttu-id="f74be-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f74be-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="f74be-167">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f74be-167">NOTES</span></span>

## <span data-ttu-id="f74be-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f74be-168">RELATED LINKS</span></span>

[<span data-ttu-id="f74be-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f74be-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="f74be-170">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f74be-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="f74be-171">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f74be-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


