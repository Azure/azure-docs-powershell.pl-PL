---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 3d8445c78ae2f11fef734db0b24319b524f55704
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220380"
---
# <span data-ttu-id="f4ecd-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="f4ecd-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="f4ecd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ecd-103">Aktualizuje zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="f4ecd-103">Updates managed application</span></span>

## <span data-ttu-id="f4ecd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4ecd-104">SYNTAX</span></span>

### <span data-ttu-id="f4ecd-105">SetByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f4ecd-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ecd-106">SetById</span><span class="sxs-lookup"><span data-stu-id="f4ecd-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ecd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f4ecd-107">DESCRIPTION</span></span>
<span data-ttu-id="f4ecd-108">Polecenie cmdlet **Set-AzManagedApplication** aktualizuje zarządzane aplikacje</span><span class="sxs-lookup"><span data-stu-id="f4ecd-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="f4ecd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4ecd-109">EXAMPLES</span></span>

### <span data-ttu-id="f4ecd-110">Przykład 1: Opis definicji aplikacji zarządzanej przez aktualizowanie</span><span class="sxs-lookup"><span data-stu-id="f4ecd-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="f4ecd-111">To polecenie aktualizuje opis aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="f4ecd-111">This command updates the managed application description</span></span>

## <span data-ttu-id="f4ecd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4ecd-112">PARAMETERS</span></span>

### <span data-ttu-id="f4ecd-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f4ecd-113">-ApiVersion</span></span>
<span data-ttu-id="f4ecd-114">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f4ecd-115">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f4ecd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ecd-116">-DefaultProfile</span></span>
<span data-ttu-id="f4ecd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4ecd-118">-ID</span><span class="sxs-lookup"><span data-stu-id="f4ecd-118">-Id</span></span>
<span data-ttu-id="f4ecd-119">W pełni kwalifikowany identyfikator zarządzanej aplikacji, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="f4ecd-120">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ecd-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="f4ecd-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="f4ecd-121">-Kind</span></span>
<span data-ttu-id="f4ecd-122">Rodzaj zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-122">The managed application kind.</span></span>
<span data-ttu-id="f4ecd-123">Jedna z rynków lub usługi katalogowej</span><span class="sxs-lookup"><span data-stu-id="f4ecd-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="f4ecd-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f4ecd-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="f4ecd-125">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="f4ecd-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ecd-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="f4ecd-127">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="f4ecd-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4ecd-128">-Name</span></span>
<span data-ttu-id="f4ecd-129">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-129">The managed application name.</span></span>

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

### <span data-ttu-id="f4ecd-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f4ecd-130">-Parameter</span></span>
<span data-ttu-id="f4ecd-131">Ciąg sformatowany w notacji JSON parametrów dla aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="f4ecd-132">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego parametry lub parametry jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="f4ecd-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="f4ecd-133">-Plan</span></span>
<span data-ttu-id="f4ecd-134">Tabela skrótów reprezentująca właściwości zarządzanego planu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="f4ecd-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="f4ecd-135">-Pre</span></span>
<span data-ttu-id="f4ecd-136">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f4ecd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ecd-137">-ResourceGroupName</span></span>
<span data-ttu-id="f4ecd-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-138">The resource group name.</span></span>

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

### <span data-ttu-id="f4ecd-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4ecd-139">-Tag</span></span>
<span data-ttu-id="f4ecd-140">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="f4ecd-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f4ecd-141">-Confirm</span></span>
<span data-ttu-id="f4ecd-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ecd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ecd-143">-WhatIf</span></span>
<span data-ttu-id="f4ecd-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4ecd-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ecd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ecd-146">CommonParameters</span></span>
<span data-ttu-id="f4ecd-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ecd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ecd-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4ecd-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ecd-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4ecd-149">INPUTS</span></span>

### <span data-ttu-id="f4ecd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f4ecd-150">System.String</span></span>

### <span data-ttu-id="f4ecd-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4ecd-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f4ecd-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4ecd-152">OUTPUTS</span></span>

### <span data-ttu-id="f4ecd-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f4ecd-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f4ecd-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4ecd-154">NOTES</span></span>

## <span data-ttu-id="f4ecd-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4ecd-155">RELATED LINKS</span></span>
