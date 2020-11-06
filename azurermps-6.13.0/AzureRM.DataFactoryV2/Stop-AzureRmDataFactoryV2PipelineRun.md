---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: d93cd05122d0a2c321ef4ab6d858f975e84bc9a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545399"
---
# <span data-ttu-id="8500d-101">Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="8500d-101">Stop-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="8500d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8500d-102">SYNOPSIS</span></span>
<span data-ttu-id="8500d-103">Zatrzymuje działanie pieline w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="8500d-103">Stops a pieline run in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8500d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8500d-104">SYNTAX</span></span>

### <span data-ttu-id="8500d-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8500d-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8500d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8500d-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8500d-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8500d-107">ByFactoryObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8500d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8500d-108">DESCRIPTION</span></span>
<span data-ttu-id="8500d-109">Polecenie cmdlet **stop-AzureRmDataFactoryV2PipelineRun** zatrzymuje potok w fabryce danych określonym przy użyciu pieline identyfikatora uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="8500d-109">The **Stop-AzureRmDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="8500d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8500d-110">EXAMPLES</span></span>

### <span data-ttu-id="8500d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8500d-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="8500d-112">To polecenie zatrzymuje potok uruchomiony z identyfikatorem b9730a13-AA12-4926-a8b3-8e3a974ab0bd w WikiADF fabrycznej.</span><span class="sxs-lookup"><span data-stu-id="8500d-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="8500d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8500d-113">PARAMETERS</span></span>

### <span data-ttu-id="8500d-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8500d-114">-DataFactory</span></span>
<span data-ttu-id="8500d-115">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="8500d-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8500d-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8500d-116">-DataFactoryName</span></span>
<span data-ttu-id="8500d-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="8500d-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8500d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8500d-118">-DefaultProfile</span></span>
<span data-ttu-id="8500d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8500d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8500d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8500d-120">-InputObject</span></span>
<span data-ttu-id="8500d-121">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="8500d-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8500d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8500d-122">-PassThru</span></span>
<span data-ttu-id="8500d-123">Jeśli określono polecenie cmdlet Write-in polecenia "in" w przypadku powodzenia.</span><span class="sxs-lookup"><span data-stu-id="8500d-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="8500d-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="8500d-124">-PipelineRunId</span></span>
<span data-ttu-id="8500d-125">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="8500d-125">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8500d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8500d-126">-ResourceGroupName</span></span>
<span data-ttu-id="8500d-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8500d-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8500d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8500d-128">-Confirm</span></span>
<span data-ttu-id="8500d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8500d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8500d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8500d-130">-WhatIf</span></span>
<span data-ttu-id="8500d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8500d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8500d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8500d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8500d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8500d-133">CommonParameters</span></span>
<span data-ttu-id="8500d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8500d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8500d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8500d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8500d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8500d-136">INPUTS</span></span>

### <span data-ttu-id="8500d-137">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="8500d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>
<span data-ttu-id="8500d-138">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8500d-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8500d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8500d-139">System.String</span></span>

### <span data-ttu-id="8500d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8500d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="8500d-141">Parametry: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8500d-141">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="8500d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8500d-142">OUTPUTS</span></span>

### <span data-ttu-id="8500d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8500d-143">System.Boolean</span></span>

## <span data-ttu-id="8500d-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8500d-144">NOTES</span></span>

## <span data-ttu-id="8500d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8500d-145">RELATED LINKS</span></span>
