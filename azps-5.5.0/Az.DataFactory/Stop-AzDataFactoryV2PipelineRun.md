---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238250"
---
# <span data-ttu-id="bb01a-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="bb01a-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="bb01a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb01a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb01a-103">Zatrzymuje uruchomienie potoku w fabrycznej układzie danych.</span><span class="sxs-lookup"><span data-stu-id="bb01a-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="bb01a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb01a-104">SYNTAX</span></span>

### <span data-ttu-id="bb01a-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="bb01a-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb01a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bb01a-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb01a-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bb01a-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb01a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb01a-108">DESCRIPTION</span></span>
<span data-ttu-id="bb01a-109">Polecenie **cmdlet Stop-AzDataFactoryV2PipelineRun** zatrzymuje uruchomienie potoku w fabrycznej bazie danych określonej przy użyciu identyfikatora uruchamiania potoku.</span><span class="sxs-lookup"><span data-stu-id="bb01a-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="bb01a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb01a-110">EXAMPLES</span></span>

### <span data-ttu-id="bb01a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb01a-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="bb01a-112">To polecenie zatrzymuje uruchomienie potoku o identyfikatorze b9730a13-aa12-4926-a8b3-8e3a974ab0bd w fabrycznej układzie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="bb01a-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="bb01a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb01a-113">PARAMETERS</span></span>

### <span data-ttu-id="bb01a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bb01a-114">-DataFactory</span></span>
<span data-ttu-id="bb01a-115">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="bb01a-115">The data factory object.</span></span>

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

### <span data-ttu-id="bb01a-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bb01a-116">-DataFactoryName</span></span>
<span data-ttu-id="bb01a-117">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="bb01a-117">The data factory name.</span></span>

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

### <span data-ttu-id="bb01a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb01a-118">-DefaultProfile</span></span>
<span data-ttu-id="bb01a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb01a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb01a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb01a-120">-InputObject</span></span>
<span data-ttu-id="bb01a-121">Identyfikator uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="bb01a-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="bb01a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb01a-122">-PassThru</span></span>
<span data-ttu-id="bb01a-123">Jeśli określono polecenie cmdlet write true (zapisz na wypadek, gdyby operacja zakończyła się powodzeniem).</span><span class="sxs-lookup"><span data-stu-id="bb01a-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="bb01a-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="bb01a-124">-PipelineRunId</span></span>
<span data-ttu-id="bb01a-125">Identyfikator uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="bb01a-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="bb01a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb01a-126">-ResourceGroupName</span></span>
<span data-ttu-id="bb01a-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb01a-127">The resource group name.</span></span>

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

### <span data-ttu-id="bb01a-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb01a-128">-Confirm</span></span>
<span data-ttu-id="bb01a-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb01a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb01a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb01a-130">-WhatIf</span></span>
<span data-ttu-id="bb01a-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb01a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb01a-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb01a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb01a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb01a-133">CommonParameters</span></span>
<span data-ttu-id="bb01a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb01a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb01a-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb01a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb01a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb01a-136">INPUTS</span></span>

### <span data-ttu-id="bb01a-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="bb01a-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="bb01a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bb01a-138">System.String</span></span>

### <span data-ttu-id="bb01a-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bb01a-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bb01a-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb01a-140">OUTPUTS</span></span>

### <span data-ttu-id="bb01a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb01a-141">System.Boolean</span></span>

## <span data-ttu-id="bb01a-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb01a-142">NOTES</span></span>

## <span data-ttu-id="bb01a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb01a-143">RELATED LINKS</span></span>
