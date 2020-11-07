---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 870769c6bb2557b2a654b4625d3f2c7ea1b4293e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542323"
---
# <span data-ttu-id="e77a2-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="e77a2-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="e77a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e77a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e77a2-103">Aktualizuje zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="e77a2-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e77a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e77a2-104">SYNTAX</span></span>

### <span data-ttu-id="e77a2-105">SetByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e77a2-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77a2-106">SetById</span><span class="sxs-lookup"><span data-stu-id="e77a2-106">SetById</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e77a2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e77a2-107">DESCRIPTION</span></span>
<span data-ttu-id="e77a2-108">Polecenie cmdlet **Set-AzureRmManagedApplication** aktualizuje zarządzane aplikacje</span><span class="sxs-lookup"><span data-stu-id="e77a2-108">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="e77a2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e77a2-109">EXAMPLES</span></span>

### <span data-ttu-id="e77a2-110">Przykład 1: Opis definicji aplikacji zarządzanej przez aktualizowanie</span><span class="sxs-lookup"><span data-stu-id="e77a2-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="e77a2-111">To polecenie aktualizuje opis aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="e77a2-111">This command updates the managed application description</span></span>

## <span data-ttu-id="e77a2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e77a2-112">PARAMETERS</span></span>

### <span data-ttu-id="e77a2-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e77a2-113">-ApiVersion</span></span>
<span data-ttu-id="e77a2-114">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="e77a2-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e77a2-115">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="e77a2-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e77a2-116">-DefaultProfile</span></span>
<span data-ttu-id="e77a2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e77a2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e77a2-118">-ID</span><span class="sxs-lookup"><span data-stu-id="e77a2-118">-Id</span></span>
<span data-ttu-id="e77a2-119">W pełni kwalifikowany identyfikator zarządzanej aplikacji, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="e77a2-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="e77a2-120">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e77a2-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e77a2-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="e77a2-121">-Kind</span></span>
<span data-ttu-id="e77a2-122">Rodzaj zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e77a2-122">The managed application kind.</span></span>
<span data-ttu-id="e77a2-123">Jedna z rynków lub usługi katalogowej</span><span class="sxs-lookup"><span data-stu-id="e77a2-123">One of marketplace or servicecatalog</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77a2-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e77a2-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="e77a2-125">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="e77a2-125">The managed resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e77a2-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e77a2-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="e77a2-127">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="e77a2-127">The managed resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e77a2-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e77a2-128">-Name</span></span>
<span data-ttu-id="e77a2-129">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e77a2-129">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e77a2-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e77a2-130">-Parameter</span></span>
<span data-ttu-id="e77a2-131">Ciąg sformatowany w notacji JSON parametrów dla aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e77a2-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="e77a2-132">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego parametry lub parametry jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="e77a2-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e77a2-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="e77a2-133">-Plan</span></span>
<span data-ttu-id="e77a2-134">Tabela skrótów reprezentująca właściwości zarządzanego planu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e77a2-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77a2-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="e77a2-135">-Pre</span></span>
<span data-ttu-id="e77a2-136">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="e77a2-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e77a2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e77a2-137">-ResourceGroupName</span></span>
<span data-ttu-id="e77a2-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e77a2-138">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e77a2-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="e77a2-139">-Tag</span></span>
<span data-ttu-id="e77a2-140">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="e77a2-140">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e77a2-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e77a2-141">-Confirm</span></span>
<span data-ttu-id="e77a2-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e77a2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e77a2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e77a2-143">-WhatIf</span></span>
<span data-ttu-id="e77a2-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e77a2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e77a2-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e77a2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e77a2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e77a2-146">CommonParameters</span></span>
<span data-ttu-id="e77a2-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e77a2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e77a2-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e77a2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e77a2-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e77a2-149">INPUTS</span></span>

### <span data-ttu-id="e77a2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e77a2-150">System.String</span></span>
<span data-ttu-id="e77a2-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e77a2-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e77a2-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e77a2-152">OUTPUTS</span></span>

### <span data-ttu-id="e77a2-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e77a2-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e77a2-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e77a2-154">NOTES</span></span>

## <span data-ttu-id="e77a2-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e77a2-155">RELATED LINKS</span></span>