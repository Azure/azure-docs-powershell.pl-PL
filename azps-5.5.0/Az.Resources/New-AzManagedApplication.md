---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 06ff54b8f5a247f3035d0eda0be5c474f9a9576b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186419"
---
# <span data-ttu-id="e76df-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="e76df-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="e76df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e76df-102">SYNOPSIS</span></span>
<span data-ttu-id="e76df-103">Tworzy aplikację zarządzaną na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e76df-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="e76df-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e76df-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e76df-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e76df-105">DESCRIPTION</span></span>
<span data-ttu-id="e76df-106">Polecenie **cmdlet New-AzManagedApplication** tworzy aplikację zarządzaną azure.</span><span class="sxs-lookup"><span data-stu-id="e76df-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="e76df-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e76df-107">EXAMPLES</span></span>

### <span data-ttu-id="e76df-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e76df-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="e76df-109">To polecenie tworzy aplikację zarządzaną</span><span class="sxs-lookup"><span data-stu-id="e76df-109">This command creates a managed application</span></span>

## <span data-ttu-id="e76df-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e76df-110">PARAMETERS</span></span>

### <span data-ttu-id="e76df-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e76df-111">-ApiVersion</span></span>
<span data-ttu-id="e76df-112">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="e76df-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e76df-113">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="e76df-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e76df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e76df-114">-DefaultProfile</span></span>
<span data-ttu-id="e76df-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e76df-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e76df-116">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="e76df-116">-Kind</span></span>
<span data-ttu-id="e76df-117">Zarządzany rodzaj aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e76df-117">The managed application kind.</span></span>
<span data-ttu-id="e76df-118">Jeden z portali handlowych lub serwisowych</span><span class="sxs-lookup"><span data-stu-id="e76df-118">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="e76df-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e76df-119">-Location</span></span>
<span data-ttu-id="e76df-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e76df-120">The resource location.</span></span>

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

### <span data-ttu-id="e76df-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e76df-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="e76df-122">Nazwa grupy zasobów zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="e76df-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="e76df-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e76df-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="e76df-124">Nazwa grupy zasobów zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="e76df-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="e76df-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e76df-125">-Name</span></span>
<span data-ttu-id="e76df-126">Nazwa aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e76df-126">The managed application name.</span></span>

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

### <span data-ttu-id="e76df-127">- Parametr</span><span class="sxs-lookup"><span data-stu-id="e76df-127">-Parameter</span></span>
<span data-ttu-id="e76df-128">Sformatowany ciąg parametrów JSON dla aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e76df-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="e76df-129">Może to być ścieżka do nazwy pliku lub uri zawierającej parametry albo parametry jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="e76df-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="e76df-130">— planowanie</span><span class="sxs-lookup"><span data-stu-id="e76df-130">-Plan</span></span>
<span data-ttu-id="e76df-131">Tabela skrótów reprezentująca właściwości planu aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="e76df-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="e76df-132">— Przed</span><span class="sxs-lookup"><span data-stu-id="e76df-132">-Pre</span></span>
<span data-ttu-id="e76df-133">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e76df-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e76df-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e76df-134">-ResourceGroupName</span></span>
<span data-ttu-id="e76df-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e76df-135">The resource group name.</span></span>

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

### <span data-ttu-id="e76df-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="e76df-136">-Tag</span></span>
<span data-ttu-id="e76df-137">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="e76df-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e76df-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e76df-138">-Confirm</span></span>
<span data-ttu-id="e76df-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e76df-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e76df-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e76df-140">-WhatIf</span></span>
<span data-ttu-id="e76df-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e76df-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e76df-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e76df-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e76df-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76df-143">CommonParameters</span></span>
<span data-ttu-id="e76df-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e76df-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76df-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e76df-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76df-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e76df-146">INPUTS</span></span>

### <span data-ttu-id="e76df-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e76df-147">System.String</span></span>

### <span data-ttu-id="e76df-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e76df-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e76df-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e76df-149">OUTPUTS</span></span>

### <span data-ttu-id="e76df-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e76df-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e76df-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e76df-151">NOTES</span></span>

## <span data-ttu-id="e76df-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e76df-152">RELATED LINKS</span></span>
