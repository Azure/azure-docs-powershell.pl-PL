---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 3d8445c78ae2f11fef734db0b24319b524f55704
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186330"
---
# <span data-ttu-id="32a85-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="32a85-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="32a85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32a85-102">SYNOPSIS</span></span>
<span data-ttu-id="32a85-103">Aktualizacje aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="32a85-103">Updates managed application</span></span>

## <span data-ttu-id="32a85-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="32a85-104">SYNTAX</span></span>

### <span data-ttu-id="32a85-105">SetByNameAndResourceGroup (domyślne)</span><span class="sxs-lookup"><span data-stu-id="32a85-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32a85-106">SetById</span><span class="sxs-lookup"><span data-stu-id="32a85-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32a85-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="32a85-107">DESCRIPTION</span></span>
<span data-ttu-id="32a85-108">Polecenie **cmdlet Set-AzManagedApplication** aktualizuje aplikacje zarządzane</span><span class="sxs-lookup"><span data-stu-id="32a85-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="32a85-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="32a85-109">EXAMPLES</span></span>

### <span data-ttu-id="32a85-110">Przykład 1. Aktualizowanie opisu zarządzanej definicji aplikacji</span><span class="sxs-lookup"><span data-stu-id="32a85-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="32a85-111">To polecenie aktualizuje opis aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="32a85-111">This command updates the managed application description</span></span>

## <span data-ttu-id="32a85-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32a85-112">PARAMETERS</span></span>

### <span data-ttu-id="32a85-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="32a85-113">-ApiVersion</span></span>
<span data-ttu-id="32a85-114">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="32a85-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="32a85-115">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="32a85-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="32a85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a85-116">-DefaultProfile</span></span>
<span data-ttu-id="32a85-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="32a85-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32a85-118">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="32a85-118">-Id</span></span>
<span data-ttu-id="32a85-119">W pełni kwalifikowany identyfikator aplikacji zarządzanej, łącznie z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="32a85-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="32a85-120">np. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a85-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a85-121">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="32a85-121">-Kind</span></span>
<span data-ttu-id="32a85-122">Zarządzany rodzaj aplikacji.</span><span class="sxs-lookup"><span data-stu-id="32a85-122">The managed application kind.</span></span>
<span data-ttu-id="32a85-123">Jeden z portali handlowych lub serwisowych</span><span class="sxs-lookup"><span data-stu-id="32a85-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="32a85-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="32a85-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="32a85-125">Nazwa grupy zasobów zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="32a85-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="32a85-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a85-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="32a85-127">Nazwa grupy zasobów zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="32a85-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="32a85-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="32a85-128">-Name</span></span>
<span data-ttu-id="32a85-129">Nazwa aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="32a85-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a85-130">- Parametr</span><span class="sxs-lookup"><span data-stu-id="32a85-130">-Parameter</span></span>
<span data-ttu-id="32a85-131">Sformatowany ciąg parametrów JSON dla aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="32a85-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="32a85-132">Może to być ścieżka do nazwy pliku lub uri zawierającej parametry albo parametry jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="32a85-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="32a85-133">— planowanie</span><span class="sxs-lookup"><span data-stu-id="32a85-133">-Plan</span></span>
<span data-ttu-id="32a85-134">Tabela skrótów reprezentująca właściwości planu aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="32a85-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="32a85-135">— Przed</span><span class="sxs-lookup"><span data-stu-id="32a85-135">-Pre</span></span>
<span data-ttu-id="32a85-136">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="32a85-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="32a85-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a85-137">-ResourceGroupName</span></span>
<span data-ttu-id="32a85-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="32a85-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a85-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="32a85-139">-Tag</span></span>
<span data-ttu-id="32a85-140">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="32a85-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="32a85-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="32a85-141">-Confirm</span></span>
<span data-ttu-id="32a85-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="32a85-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32a85-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32a85-143">-WhatIf</span></span>
<span data-ttu-id="32a85-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32a85-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32a85-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="32a85-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32a85-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a85-146">CommonParameters</span></span>
<span data-ttu-id="32a85-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32a85-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a85-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32a85-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a85-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32a85-149">INPUTS</span></span>

### <span data-ttu-id="32a85-150">System.String</span><span class="sxs-lookup"><span data-stu-id="32a85-150">System.String</span></span>

### <span data-ttu-id="32a85-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="32a85-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="32a85-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32a85-152">OUTPUTS</span></span>

### <span data-ttu-id="32a85-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="32a85-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="32a85-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="32a85-154">NOTES</span></span>

## <span data-ttu-id="32a85-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32a85-155">RELATED LINKS</span></span>
