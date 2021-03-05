---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 30e3e7f7b6ace383a2c492f4dcc088f65dfea08b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999825"
---
# <span data-ttu-id="3e21a-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="3e21a-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="3e21a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e21a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e21a-103">Tworzy aplikację zarządzaną na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="3e21a-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="3e21a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3e21a-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e21a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3e21a-105">DESCRIPTION</span></span>
<span data-ttu-id="3e21a-106">Polecenie **cmdlet New-AzManagedApplication** tworzy aplikację zarządzaną azure.</span><span class="sxs-lookup"><span data-stu-id="3e21a-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="3e21a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3e21a-107">EXAMPLES</span></span>

### <span data-ttu-id="3e21a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3e21a-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="3e21a-109">To polecenie tworzy aplikację zarządzaną</span><span class="sxs-lookup"><span data-stu-id="3e21a-109">This command creates a managed application</span></span>

## <span data-ttu-id="3e21a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e21a-110">PARAMETERS</span></span>

### <span data-ttu-id="3e21a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3e21a-111">-ApiVersion</span></span>
<span data-ttu-id="3e21a-112">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="3e21a-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3e21a-113">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="3e21a-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3e21a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e21a-114">-DefaultProfile</span></span>
<span data-ttu-id="3e21a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e21a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e21a-116">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="3e21a-116">-Kind</span></span>
<span data-ttu-id="3e21a-117">Zarządzany rodzaj aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3e21a-117">The managed application kind.</span></span>
<span data-ttu-id="3e21a-118">Jeden z portali handlowych lub serwisowych</span><span class="sxs-lookup"><span data-stu-id="3e21a-118">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="3e21a-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3e21a-119">-Location</span></span>
<span data-ttu-id="3e21a-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3e21a-120">The resource location.</span></span>

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

### <span data-ttu-id="3e21a-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3e21a-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="3e21a-122">Nazwa grupy zasobów zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="3e21a-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="3e21a-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e21a-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="3e21a-124">Nazwa grupy zasobów zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="3e21a-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="3e21a-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3e21a-125">-Name</span></span>
<span data-ttu-id="3e21a-126">Nazwa aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="3e21a-126">The managed application name.</span></span>

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

### <span data-ttu-id="3e21a-127">- Parametr</span><span class="sxs-lookup"><span data-stu-id="3e21a-127">-Parameter</span></span>
<span data-ttu-id="3e21a-128">Sformatowany ciąg parametrów JSON dla aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="3e21a-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="3e21a-129">Może to być ścieżka do nazwy pliku lub uri zawierającej parametry albo parametry jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="3e21a-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="3e21a-130">— planowanie</span><span class="sxs-lookup"><span data-stu-id="3e21a-130">-Plan</span></span>
<span data-ttu-id="3e21a-131">Tabela skrótów reprezentująca właściwości planu aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="3e21a-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="3e21a-132">— Przed</span><span class="sxs-lookup"><span data-stu-id="3e21a-132">-Pre</span></span>
<span data-ttu-id="3e21a-133">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="3e21a-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3e21a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e21a-134">-ResourceGroupName</span></span>
<span data-ttu-id="3e21a-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e21a-135">The resource group name.</span></span>

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

### <span data-ttu-id="3e21a-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="3e21a-136">-Tag</span></span>
<span data-ttu-id="3e21a-137">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e21a-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3e21a-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e21a-138">-Confirm</span></span>
<span data-ttu-id="3e21a-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3e21a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e21a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e21a-140">-WhatIf</span></span>
<span data-ttu-id="3e21a-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e21a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e21a-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3e21a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e21a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e21a-143">CommonParameters</span></span>
<span data-ttu-id="3e21a-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e21a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e21a-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e21a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e21a-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e21a-146">INPUTS</span></span>

### <span data-ttu-id="3e21a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3e21a-147">System.String</span></span>

### <span data-ttu-id="3e21a-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3e21a-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3e21a-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e21a-149">OUTPUTS</span></span>

### <span data-ttu-id="3e21a-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="3e21a-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3e21a-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3e21a-151">NOTES</span></span>

## <span data-ttu-id="3e21a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e21a-152">RELATED LINKS</span></span>
