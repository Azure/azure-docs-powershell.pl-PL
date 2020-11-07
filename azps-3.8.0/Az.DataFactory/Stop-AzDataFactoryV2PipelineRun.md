---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896242"
---
# <span data-ttu-id="adf74-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="adf74-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="adf74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="adf74-102">SYNOPSIS</span></span>
<span data-ttu-id="adf74-103">Zatrzymuje działanie rurociągu w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="adf74-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="adf74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="adf74-104">SYNTAX</span></span>

### <span data-ttu-id="adf74-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="adf74-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="adf74-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="adf74-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adf74-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="adf74-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adf74-108">Opis</span><span class="sxs-lookup"><span data-stu-id="adf74-108">DESCRIPTION</span></span>
<span data-ttu-id="adf74-109">Polecenie cmdlet **stop-AzDataFactoryV2PipelineRun** zatrzymuje potok w fabryce danych określonej z identyfikatorem uruchomienia potoku.</span><span class="sxs-lookup"><span data-stu-id="adf74-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="adf74-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="adf74-110">EXAMPLES</span></span>

### <span data-ttu-id="adf74-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="adf74-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="adf74-112">To polecenie zatrzymuje potok uruchomiony z identyfikatorem b9730a13-AA12-4926-a8b3-8e3a974ab0bd w WikiADF fabrycznej.</span><span class="sxs-lookup"><span data-stu-id="adf74-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="adf74-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="adf74-113">PARAMETERS</span></span>

### <span data-ttu-id="adf74-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="adf74-114">-DataFactory</span></span>
<span data-ttu-id="adf74-115">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="adf74-115">The data factory object.</span></span>

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

### <span data-ttu-id="adf74-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="adf74-116">-DataFactoryName</span></span>
<span data-ttu-id="adf74-117">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="adf74-117">The data factory name.</span></span>

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

### <span data-ttu-id="adf74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf74-118">-DefaultProfile</span></span>
<span data-ttu-id="adf74-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="adf74-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adf74-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="adf74-120">-InputObject</span></span>
<span data-ttu-id="adf74-121">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="adf74-121">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="adf74-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adf74-122">-PassThru</span></span>
<span data-ttu-id="adf74-123">Jeśli określono polecenie cmdlet Write-in polecenia "in" w przypadku powodzenia.</span><span class="sxs-lookup"><span data-stu-id="adf74-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="adf74-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="adf74-124">-PipelineRunId</span></span>
<span data-ttu-id="adf74-125">Identyfikator uruchomienia rurociągu.</span><span class="sxs-lookup"><span data-stu-id="adf74-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="adf74-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adf74-126">-ResourceGroupName</span></span>
<span data-ttu-id="adf74-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="adf74-127">The resource group name.</span></span>

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

### <span data-ttu-id="adf74-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="adf74-128">-Confirm</span></span>
<span data-ttu-id="adf74-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adf74-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adf74-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adf74-130">-WhatIf</span></span>
<span data-ttu-id="adf74-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adf74-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adf74-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="adf74-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adf74-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf74-133">CommonParameters</span></span>
<span data-ttu-id="adf74-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adf74-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf74-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adf74-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf74-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adf74-136">INPUTS</span></span>

### <span data-ttu-id="adf74-137">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="adf74-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="adf74-138">System. String</span><span class="sxs-lookup"><span data-stu-id="adf74-138">System.String</span></span>

### <span data-ttu-id="adf74-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="adf74-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="adf74-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="adf74-140">OUTPUTS</span></span>

### <span data-ttu-id="adf74-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="adf74-141">System.Boolean</span></span>

## <span data-ttu-id="adf74-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="adf74-142">NOTES</span></span>

## <span data-ttu-id="adf74-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="adf74-143">RELATED LINKS</span></span>
