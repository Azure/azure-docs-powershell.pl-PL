---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 2a242f7a265efa2dd97f967101074615381d4cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542995"
---
# <span data-ttu-id="4db87-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="4db87-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="4db87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4db87-102">SYNOPSIS</span></span>
<span data-ttu-id="4db87-103">Aktualizuje zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="4db87-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4db87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4db87-104">SYNTAX</span></span>

### <span data-ttu-id="4db87-105">Zestaw parametrów nazwa aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="4db87-105">The managed application name parameter set.</span></span> <span data-ttu-id="4db87-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="4db87-106">(Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4db87-107">Zestaw parametrów zarządzany identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4db87-107">The managed application Id parameter set.</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4db87-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4db87-108">DESCRIPTION</span></span>
<span data-ttu-id="4db87-109">Polecenie cmdlet **Set-AzureRmManagedApplication** aktualizuje zarządzane aplikacje</span><span class="sxs-lookup"><span data-stu-id="4db87-109">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="4db87-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4db87-110">EXAMPLES</span></span>

### <span data-ttu-id="4db87-111">Przykład 1: Opis definicji aplikacji zarządzanej przez aktualizowanie</span><span class="sxs-lookup"><span data-stu-id="4db87-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="4db87-112">To polecenie aktualizuje opis aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="4db87-112">This command updates the managed application description</span></span>

## <span data-ttu-id="4db87-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4db87-113">PARAMETERS</span></span>

### <span data-ttu-id="4db87-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4db87-114">-ApiVersion</span></span>
<span data-ttu-id="4db87-115">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="4db87-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4db87-116">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="4db87-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4db87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db87-117">-DefaultProfile</span></span>
<span data-ttu-id="4db87-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4db87-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4db87-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="4db87-119">-Kind</span></span>
<span data-ttu-id="4db87-120">Rodzaj zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4db87-120">The managed application kind.</span></span>
<span data-ttu-id="4db87-121">Jedna z rynków lub usługi katalogowej</span><span class="sxs-lookup"><span data-stu-id="4db87-121">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="4db87-122">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="4db87-122">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="4db87-123">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="4db87-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="4db87-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db87-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="4db87-125">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="4db87-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="4db87-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4db87-126">-Name</span></span>
<span data-ttu-id="4db87-127">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4db87-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db87-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="4db87-128">-Parameter</span></span>
<span data-ttu-id="4db87-129">Ciąg sformatowany w notacji JSON parametrów dla aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="4db87-129">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="4db87-130">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego parametry lub parametry jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="4db87-130">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="4db87-131">-Plan</span><span class="sxs-lookup"><span data-stu-id="4db87-131">-Plan</span></span>
<span data-ttu-id="4db87-132">Tabela skrótów reprezentująca właściwości zarządzanego planu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4db87-132">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="4db87-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="4db87-133">-Pre</span></span>
<span data-ttu-id="4db87-134">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="4db87-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4db87-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db87-135">-ResourceGroupName</span></span>
<span data-ttu-id="4db87-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4db87-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db87-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="4db87-137">-Tag</span></span>
<span data-ttu-id="4db87-138">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="4db87-138">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4db87-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4db87-139">-Confirm</span></span>
<span data-ttu-id="4db87-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4db87-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db87-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db87-141">-WhatIf</span></span>
<span data-ttu-id="4db87-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4db87-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db87-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4db87-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db87-144">-ID</span><span class="sxs-lookup"><span data-stu-id="4db87-144">-Id</span></span>
<span data-ttu-id="4db87-145">W pełni kwalifikowany identyfikator zarządzanej aplikacji, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="4db87-145">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="4db87-146">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="4db87-146">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db87-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db87-147">CommonParameters</span></span>
<span data-ttu-id="4db87-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db87-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db87-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4db87-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db87-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4db87-150">INPUTS</span></span>

### <span data-ttu-id="4db87-151">System. String</span><span class="sxs-lookup"><span data-stu-id="4db87-151">System.String</span></span>
<span data-ttu-id="4db87-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4db87-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4db87-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4db87-153">OUTPUTS</span></span>

### <span data-ttu-id="4db87-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4db87-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4db87-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4db87-155">NOTES</span></span>

## <span data-ttu-id="4db87-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4db87-156">RELATED LINKS</span></span>

