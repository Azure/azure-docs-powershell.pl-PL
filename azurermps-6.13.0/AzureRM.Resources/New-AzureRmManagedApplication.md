---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplication.md
ms.openlocfilehash: 7764b01070058e8055174d4728c0ea70c194c7ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544831"
---
# <span data-ttu-id="4992f-101">New-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="4992f-101">New-AzureRmManagedApplication</span></span>

## <span data-ttu-id="4992f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4992f-102">SYNOPSIS</span></span>
<span data-ttu-id="4992f-103">Tworzy aplikację zarządzaną na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4992f-103">Creates an Azure managed application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4992f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4992f-104">SYNTAX</span></span>

```
New-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4992f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4992f-105">DESCRIPTION</span></span>
<span data-ttu-id="4992f-106">Polecenie cmdlet **New-AzureRmManagedApplication** umożliwia utworzenie aplikacji zarządzanej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4992f-106">The **New-AzureRmManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="4992f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4992f-107">EXAMPLES</span></span>

### <span data-ttu-id="4992f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4992f-108">Example 1</span></span>
```
PS C:\>New-AzureRmManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="4992f-109">To polecenie tworzy zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="4992f-109">This command creates a managed application</span></span>

## <span data-ttu-id="4992f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4992f-110">PARAMETERS</span></span>

### <span data-ttu-id="4992f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4992f-111">-ApiVersion</span></span>
<span data-ttu-id="4992f-112">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="4992f-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4992f-113">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="4992f-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4992f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4992f-114">-DefaultProfile</span></span>
<span data-ttu-id="4992f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4992f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4992f-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="4992f-116">-Kind</span></span>
<span data-ttu-id="4992f-117">Rodzaj zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4992f-117">The managed application kind.</span></span>
<span data-ttu-id="4992f-118">Jedna z rynków lub usługi katalogowej</span><span class="sxs-lookup"><span data-stu-id="4992f-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4992f-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4992f-119">-Location</span></span>
<span data-ttu-id="4992f-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="4992f-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4992f-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4992f-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="4992f-122">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="4992f-122">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4992f-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4992f-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="4992f-124">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="4992f-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4992f-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4992f-125">-Name</span></span>
<span data-ttu-id="4992f-126">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4992f-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4992f-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="4992f-127">-Parameter</span></span>
<span data-ttu-id="4992f-128">Ciąg sformatowany w notacji JSON parametrów dla aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="4992f-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="4992f-129">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego parametry lub parametry jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="4992f-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4992f-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="4992f-130">-Plan</span></span>
<span data-ttu-id="4992f-131">Tabela skrótów reprezentująca właściwości zarządzanego planu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4992f-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4992f-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="4992f-132">-Pre</span></span>
<span data-ttu-id="4992f-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="4992f-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4992f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4992f-134">-ResourceGroupName</span></span>
<span data-ttu-id="4992f-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4992f-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4992f-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="4992f-136">-Tag</span></span>
<span data-ttu-id="4992f-137">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="4992f-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4992f-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4992f-138">-Confirm</span></span>
<span data-ttu-id="4992f-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4992f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4992f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4992f-140">-WhatIf</span></span>
<span data-ttu-id="4992f-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4992f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4992f-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4992f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4992f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4992f-143">CommonParameters</span></span>
<span data-ttu-id="4992f-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4992f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4992f-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4992f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4992f-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4992f-146">INPUTS</span></span>

### <span data-ttu-id="4992f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4992f-147">System.String</span></span>

### <span data-ttu-id="4992f-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4992f-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4992f-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4992f-149">OUTPUTS</span></span>

### <span data-ttu-id="4992f-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4992f-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4992f-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4992f-151">NOTES</span></span>

## <span data-ttu-id="4992f-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4992f-152">RELATED LINKS</span></span>
