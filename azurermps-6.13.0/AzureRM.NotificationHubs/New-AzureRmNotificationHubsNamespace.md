---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: d4bba9d54dac21a8eb19a4b161bb2fdef29d4bb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553460"
---
# <span data-ttu-id="86ea8-101">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="86ea8-101">New-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="86ea8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="86ea8-103">Tworzy obszar nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="86ea8-103">Creates a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86ea8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86ea8-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86ea8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="86ea8-106">Polecenie cmdlet **New-AzureRmNotificationHubsNamespace** tworzy obszar nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="86ea8-106">The **New-AzureRmNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="86ea8-107">Przestrzenie nazw są kontenerami logicznymi, które pomagają organizować Centra powiadomień i zarządzać nimi.</span><span class="sxs-lookup"><span data-stu-id="86ea8-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="86ea8-108">Musisz mieć co najmniej jeden obszar nazw centrum powiadomień.</span><span class="sxs-lookup"><span data-stu-id="86ea8-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="86ea8-109">Jeden obszar nazw może być jednym z wielu koncentratorów.</span><span class="sxs-lookup"><span data-stu-id="86ea8-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="86ea8-110">Możesz mieć wiele obszarów nazw, aby zorganizować koncentratory lub przekazać konkretne osoby do zarządzania wybranym podzbiorem koncentratorów.</span><span class="sxs-lookup"><span data-stu-id="86ea8-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="86ea8-111">Aby utworzyć obszar nazw, upewnij się, że jest określana unikatowa nazwa obszaru nazw; Określ centrum danych, w którym znajduje się obszar nazw; i określ grupę zasobów, do której zostanie przypisany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="86ea8-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="86ea8-112">Po utworzeniu obszaru nazw możesz użyć polecenia cmdlet New-AzureRmNotificationHubsNamespaceAuthorizationRules, aby przypisać reguły autoryzacji do tego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="86ea8-112">After the namespace has been created you can use the New-AzureRmNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="86ea8-113">Reguły autoryzacji są używane do zarządzania uprawnieniami do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="86ea8-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="86ea8-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86ea8-114">EXAMPLES</span></span>

### <span data-ttu-id="86ea8-115">Przykład 1. Tworzenie centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="86ea8-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="86ea8-116">To polecenie tworzy centrum powiadomień o nazwie ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="86ea8-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="86ea8-117">Obszar nazw znajdzie się na zachodnim centrum danych w Stanach Zjednoczonych i zostanie przypisany do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="86ea8-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="86ea8-118">Przykład 2: tworzenie centrum powiadomień ze znacznikami</span><span class="sxs-lookup"><span data-stu-id="86ea8-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="86ea8-119">To polecenie tworzy centrum powiadomień o nazwie ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="86ea8-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="86ea8-120">Obszar nazw znajdzie się na zachodnim centrum danych w Stanach Zjednoczonych i zostanie przypisany do grupy zasobów ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="86ea8-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="86ea8-121">Ponadto to polecenie tworzy znacznik o nazwie odbiorcy i wartości PartnerOrganizations oraz jest przypisany do obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="86ea8-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="86ea8-122">Zapewnia to, że obszar nazw będzie wyświetlany w dowolnym momencie filtrowania elementów, dla których znacznik odbiorców jest ustawiony na PartnerOrganizations.</span><span class="sxs-lookup"><span data-stu-id="86ea8-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="86ea8-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86ea8-123">PARAMETERS</span></span>

### <span data-ttu-id="86ea8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ea8-124">-DefaultProfile</span></span>
<span data-ttu-id="86ea8-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="86ea8-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86ea8-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="86ea8-126">-Location</span></span>
<span data-ttu-id="86ea8-127">Określa nazwę wyświetlaną centrum danych, które będzie hostem obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="86ea8-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="86ea8-128">Ten parametr można ustawić na dowolną prawidłową lokalizację, co zapewnia optymalną wydajność, które mogą być używane w pobliżu większości użytkowników.</span><span class="sxs-lookup"><span data-stu-id="86ea8-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="86ea8-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="86ea8-129">-Namespace</span></span>
<span data-ttu-id="86ea8-130">Określa nazwę nowego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="86ea8-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="86ea8-131">Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.</span><span class="sxs-lookup"><span data-stu-id="86ea8-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="86ea8-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="86ea8-132">-ResourceGroup</span></span>
<span data-ttu-id="86ea8-133">Określa grupę zasobów, do której zostanie przypisany obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="86ea8-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="86ea8-134">Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób ułatwiający Zarządzanie zapasami i administrację.</span><span class="sxs-lookup"><span data-stu-id="86ea8-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="86ea8-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="86ea8-135">-SkuTier</span></span>
<span data-ttu-id="86ea8-136">Warstwa SKU obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="86ea8-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="86ea8-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="86ea8-137">-Tag</span></span>
<span data-ttu-id="86ea8-138">Określa pary nazwa-wartość, których można użyć do kategoryzowania i organizowania elementów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="86ea8-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="86ea8-139">Funkcja Tagi podobna do słów kluczowych i działa w ramach wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="86ea8-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="86ea8-140">Jeśli na przykład wyszukiwane są wszystkie elementy z działem znaczników: funkcja wyszukiwania zwróci wszystkie elementy platformy Azure, które mają ten tag, niezależnie od tego, jakie elementy są takie jak typ elementu, lokalizacja lub Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="86ea8-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="86ea8-141">Pojedynczy znacznik składa się z dwóch części: *nazwy* i opcjonalnie *wartości*.</span><span class="sxs-lookup"><span data-stu-id="86ea8-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="86ea8-142">Na przykład w dziale: to nazwa znacznika to dział, a jego wartość to znacznik.</span><span class="sxs-lookup"><span data-stu-id="86ea8-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="86ea8-143">Aby dodać znacznik, użyj składni tabeli skrótów podobnej do tego, co spowoduje utworzenie znacznika CalendarYear: 2016:</span><span class="sxs-lookup"><span data-stu-id="86ea8-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ea8-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86ea8-144">-Confirm</span></span>
<span data-ttu-id="86ea8-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86ea8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ea8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ea8-146">-WhatIf</span></span>
<span data-ttu-id="86ea8-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86ea8-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86ea8-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86ea8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86ea8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ea8-149">CommonParameters</span></span>
<span data-ttu-id="86ea8-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ea8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ea8-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ea8-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ea8-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86ea8-152">INPUTS</span></span>

### <span data-ttu-id="86ea8-153">System. String</span><span class="sxs-lookup"><span data-stu-id="86ea8-153">System.String</span></span>

### <span data-ttu-id="86ea8-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="86ea8-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="86ea8-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86ea8-155">OUTPUTS</span></span>

### <span data-ttu-id="86ea8-156">Microsoft. Azure. Commands. NotificationHubs. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="86ea8-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="86ea8-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86ea8-157">NOTES</span></span>

## <span data-ttu-id="86ea8-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86ea8-158">RELATED LINKS</span></span>

[<span data-ttu-id="86ea8-159">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="86ea8-159">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="86ea8-160">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="86ea8-160">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="86ea8-161">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="86ea8-161">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


