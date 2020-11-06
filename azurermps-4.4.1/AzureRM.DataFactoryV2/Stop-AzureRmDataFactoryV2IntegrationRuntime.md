---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 181d63a41853105b21826353fabfca83cddf1bd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554376"
---
# <span data-ttu-id="426c9-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="426c9-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="426c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="426c9-102">SYNOPSIS</span></span>
<span data-ttu-id="426c9-103">Zatrzymuje zarządzane dedykowane środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="426c9-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="426c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="426c9-104">SYNTAX</span></span>

### <span data-ttu-id="426c9-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="426c9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="426c9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="426c9-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="426c9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="426c9-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="426c9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="426c9-108">DESCRIPTION</span></span>
<span data-ttu-id="426c9-109">Polecenie cmdlet **stop-AzureRmDataFactoryV2IntegrationRuntime** zatrzymuje zarządzane dedykowane środowisko uruchomieniowe integracji w stanie uruchomionym, który został uruchomiony przez polecenie cmdlet Start-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="426c9-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="426c9-110">Zasoby są zwalniane i przetransferowano stan do "Zatrzymano".</span><span class="sxs-lookup"><span data-stu-id="426c9-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="426c9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="426c9-111">EXAMPLES</span></span>

### <span data-ttu-id="426c9-112">Przykład 1: zatrzymanie zarządzanego środowiska uruchomieniowego integracji, które jest w stanie uruchomionym.</span><span class="sxs-lookup"><span data-stu-id="426c9-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="426c9-113">Stan programu Managed Integration Runtime "test-reserlved-IR" jest w stanie "uruchomiony".</span><span class="sxs-lookup"><span data-stu-id="426c9-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="426c9-114">Po uruchomieniu polecenia cmdlet Stop-AzureRmDataFactoryV2IntegrationRuntime zasoby są zwalniane, a transfery stanowe są przekazywane do "zatrzymane".</span><span class="sxs-lookup"><span data-stu-id="426c9-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="426c9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="426c9-115">PARAMETERS</span></span>

### <span data-ttu-id="426c9-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="426c9-116">-Confirm</span></span>
<span data-ttu-id="426c9-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="426c9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="426c9-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="426c9-118">-DataFactoryName</span></span>
<span data-ttu-id="426c9-119">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="426c9-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426c9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="426c9-120">-Force</span></span>
<span data-ttu-id="426c9-121">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="426c9-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="426c9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="426c9-122">-InputObject</span></span>
<span data-ttu-id="426c9-123">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="426c9-123">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="426c9-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="426c9-124">-Name</span></span>
<span data-ttu-id="426c9-125">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="426c9-125">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426c9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="426c9-126">-ResourceGroupName</span></span>
<span data-ttu-id="426c9-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="426c9-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426c9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="426c9-128">-ResourceId</span></span>
<span data-ttu-id="426c9-129">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="426c9-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426c9-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="426c9-130">-Confirm</span></span>
<span data-ttu-id="426c9-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="426c9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="426c9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="426c9-132">-WhatIf</span></span>
<span data-ttu-id="426c9-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="426c9-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="426c9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426c9-134">CommonParameters</span></span>
<span data-ttu-id="426c9-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="426c9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426c9-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="426c9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426c9-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="426c9-137">INPUTS</span></span>

### <span data-ttu-id="426c9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="426c9-138">System.String</span></span>
<span data-ttu-id="426c9-139">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="426c9-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="426c9-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="426c9-140">OUTPUTS</span></span>

### <span data-ttu-id="426c9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="426c9-141">System.Boolean</span></span>

## <span data-ttu-id="426c9-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="426c9-142">NOTES</span></span>
<span data-ttu-id="426c9-143">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki, kopiowanie, działania, środowisko uruchomieniowe integracji</span><span class="sxs-lookup"><span data-stu-id="426c9-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="426c9-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="426c9-144">RELATED LINKS</span></span>
[<span data-ttu-id="426c9-145">Start — AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="426c9-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
