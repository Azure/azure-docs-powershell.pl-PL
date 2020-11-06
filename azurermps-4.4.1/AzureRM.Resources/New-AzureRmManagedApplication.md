---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplication.md
ms.openlocfilehash: 830b1ed91f8e6148886be9fa3d0c49d48d52d369
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553770"
---
# <span data-ttu-id="eda00-101">New-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="eda00-101">New-AzureRmManagedApplication</span></span>

## <span data-ttu-id="eda00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eda00-102">SYNOPSIS</span></span>
<span data-ttu-id="eda00-103">Tworzy aplikację zarządzaną na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="eda00-103">Creates an Azure managed application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eda00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eda00-104">SYNTAX</span></span>

```
New-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eda00-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eda00-105">DESCRIPTION</span></span>
<span data-ttu-id="eda00-106">Polecenie cmdlet **New-AzureRmManagedApplication** umożliwia utworzenie aplikacji zarządzanej na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="eda00-106">The **New-AzureRmManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="eda00-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eda00-107">EXAMPLES</span></span>

### <span data-ttu-id="eda00-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eda00-108">Example 1</span></span>
```
PS C:\>New-AzureRmManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="eda00-109">To polecenie tworzy zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="eda00-109">This command creates a managed application</span></span>

## <span data-ttu-id="eda00-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eda00-110">PARAMETERS</span></span>

### <span data-ttu-id="eda00-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eda00-111">-ApiVersion</span></span>
<span data-ttu-id="eda00-112">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="eda00-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="eda00-113">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="eda00-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="eda00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda00-114">-DefaultProfile</span></span>
<span data-ttu-id="eda00-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eda00-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eda00-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="eda00-116">-Kind</span></span>
<span data-ttu-id="eda00-117">Rodzaj zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eda00-117">The managed application kind.</span></span>
<span data-ttu-id="eda00-118">Jedna z rynków lub usługi katalogowej</span><span class="sxs-lookup"><span data-stu-id="eda00-118">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="eda00-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="eda00-119">-Location</span></span>
<span data-ttu-id="eda00-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="eda00-120">The resource location.</span></span>

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

### <span data-ttu-id="eda00-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="eda00-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="eda00-122">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="eda00-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="eda00-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda00-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="eda00-124">Nazwa grupy zarządzanego zasobu.</span><span class="sxs-lookup"><span data-stu-id="eda00-124">The managed resource group name.</span></span>

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

### <span data-ttu-id="eda00-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eda00-125">-Name</span></span>
<span data-ttu-id="eda00-126">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eda00-126">The managed application name.</span></span>

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

### <span data-ttu-id="eda00-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="eda00-127">-Parameter</span></span>
<span data-ttu-id="eda00-128">Ciąg sformatowany w notacji JSON parametrów dla aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="eda00-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="eda00-129">Może to być ścieżka do nazwy pliku lub identyfikatora URI zawierającego parametry lub parametry jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="eda00-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="eda00-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="eda00-130">-Plan</span></span>
<span data-ttu-id="eda00-131">Tabela skrótów reprezentująca właściwości zarządzanego planu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="eda00-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="eda00-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="eda00-132">-Pre</span></span>
<span data-ttu-id="eda00-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="eda00-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="eda00-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda00-134">-ResourceGroupName</span></span>
<span data-ttu-id="eda00-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eda00-135">The resource group name.</span></span>

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

### <span data-ttu-id="eda00-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="eda00-136">-Tag</span></span>
<span data-ttu-id="eda00-137">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="eda00-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="eda00-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eda00-138">-Confirm</span></span>
<span data-ttu-id="eda00-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eda00-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eda00-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eda00-140">-WhatIf</span></span>
<span data-ttu-id="eda00-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eda00-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eda00-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eda00-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eda00-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda00-143">CommonParameters</span></span>
<span data-ttu-id="eda00-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eda00-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda00-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eda00-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda00-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eda00-146">INPUTS</span></span>

### <span data-ttu-id="eda00-147">System. String</span><span class="sxs-lookup"><span data-stu-id="eda00-147">System.String</span></span>
<span data-ttu-id="eda00-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eda00-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eda00-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eda00-149">OUTPUTS</span></span>

### <span data-ttu-id="eda00-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="eda00-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="eda00-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eda00-151">NOTES</span></span>

## <span data-ttu-id="eda00-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eda00-152">RELATED LINKS</span></span>

