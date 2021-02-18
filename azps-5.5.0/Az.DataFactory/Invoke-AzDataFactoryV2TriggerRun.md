---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181051"
---
# <span data-ttu-id="c48f7-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="c48f7-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="c48f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48f7-102">SYNOPSIS</span></span>
 <span data-ttu-id="c48f7-103">Wywołuje kolejne wystąpienie uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c48f7-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="c48f7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c48f7-104">SYNTAX</span></span>

### <span data-ttu-id="c48f7-105">ByFactoryNameByParameterFile (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c48f7-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c48f7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c48f7-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c48f7-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="c48f7-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c48f7-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c48f7-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c48f7-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="c48f7-109">DESCRIPTION</span></span>
<span data-ttu-id="c48f7-110">Polecenie **Invoke-AzDataFactoryV2TriggerRun** uruchamia kolejne wystąpienie uruchomienia wyzwalacza z nowym identyfikatorem uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c48f7-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="c48f7-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c48f7-111">EXAMPLES</span></span>

### <span data-ttu-id="c48f7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c48f7-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="c48f7-113">Uruchamia kolejne wystąpienie wyzwalacza z nowym identyfikatorem uruchomienia wyzwalacza, zachowując ten sam windowStartTime i windowEndTime co oryginalne uruchomienie wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c48f7-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="c48f7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c48f7-114">PARAMETERS</span></span>

### <span data-ttu-id="c48f7-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c48f7-115">-DataFactory</span></span>
<span data-ttu-id="c48f7-116">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="c48f7-116">The data factory object.</span></span>

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

### <span data-ttu-id="c48f7-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c48f7-117">-DataFactoryName</span></span>
<span data-ttu-id="c48f7-118">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="c48f7-118">The data factory name.</span></span>

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

### <span data-ttu-id="c48f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48f7-119">-DefaultProfile</span></span>
<span data-ttu-id="c48f7-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c48f7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c48f7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c48f7-121">-InputObject</span></span>
<span data-ttu-id="c48f7-122">Informacje o uruchomieniu wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c48f7-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c48f7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c48f7-123">-PassThru</span></span>
<span data-ttu-id="c48f7-124">Jeśli określono polecenie cmdlet write true (zapisz na wypadek, gdyby operacja zakończyła się powodzeniem).</span><span class="sxs-lookup"><span data-stu-id="c48f7-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="c48f7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48f7-125">-ResourceGroupName</span></span>
<span data-ttu-id="c48f7-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c48f7-126">The resource group name.</span></span>

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

### <span data-ttu-id="c48f7-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="c48f7-127">-TriggerName</span></span>
<span data-ttu-id="c48f7-128">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c48f7-128">The trigger name.</span></span>

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

### <span data-ttu-id="c48f7-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="c48f7-129">-TriggerRunId</span></span>
<span data-ttu-id="c48f7-130">Identyfikator uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="c48f7-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48f7-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c48f7-131">-Confirm</span></span>
<span data-ttu-id="c48f7-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c48f7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c48f7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c48f7-133">-WhatIf</span></span>
<span data-ttu-id="c48f7-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c48f7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c48f7-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c48f7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c48f7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48f7-136">CommonParameters</span></span>
<span data-ttu-id="c48f7-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48f7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48f7-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c48f7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48f7-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c48f7-139">INPUTS</span></span>

### <span data-ttu-id="c48f7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="c48f7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="c48f7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c48f7-141">System.String</span></span>

### <span data-ttu-id="c48f7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c48f7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="c48f7-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c48f7-143">OUTPUTS</span></span>

### <span data-ttu-id="c48f7-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="c48f7-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="c48f7-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c48f7-145">NOTES</span></span>

## <span data-ttu-id="c48f7-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c48f7-146">RELATED LINKS</span></span>
