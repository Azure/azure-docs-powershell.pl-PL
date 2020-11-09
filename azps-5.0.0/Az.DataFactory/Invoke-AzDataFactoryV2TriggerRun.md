---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306210"
---
# <span data-ttu-id="e8164-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="e8164-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="e8164-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8164-102">SYNOPSIS</span></span>
 <span data-ttu-id="e8164-103">Wywołuje inne wystąpienie uruchomionego wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e8164-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="e8164-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8164-104">SYNTAX</span></span>

### <span data-ttu-id="e8164-105">ByFactoryNameByParameterFile (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8164-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8164-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8164-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8164-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="e8164-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8164-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e8164-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8164-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e8164-109">DESCRIPTION</span></span>
<span data-ttu-id="e8164-110">Polecenie **Invoke-AzDataFactoryV2TriggerRun** umożliwia uruchomienie kolejnego wystąpienia wyzwalacza z nowym identyfikatorem uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e8164-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="e8164-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8164-111">EXAMPLES</span></span>

### <span data-ttu-id="e8164-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8164-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="e8164-113">Uruchamia kolejne wystąpienie wyzwalacza z nowym identyfikatorem uruchomienia wyzwalacza, zachowując te same windowStartTime i windowEndTime co oryginalny wyzwalacz.</span><span class="sxs-lookup"><span data-stu-id="e8164-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="e8164-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8164-114">PARAMETERS</span></span>

### <span data-ttu-id="e8164-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e8164-115">-DataFactory</span></span>
<span data-ttu-id="e8164-116">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e8164-116">The data factory object.</span></span>

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

### <span data-ttu-id="e8164-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="e8164-117">-DataFactoryName</span></span>
<span data-ttu-id="e8164-118">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="e8164-118">The data factory name.</span></span>

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

### <span data-ttu-id="e8164-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8164-119">-DefaultProfile</span></span>
<span data-ttu-id="e8164-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8164-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8164-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8164-121">-InputObject</span></span>
<span data-ttu-id="e8164-122">Informacje na temat uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e8164-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="e8164-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8164-123">-PassThru</span></span>
<span data-ttu-id="e8164-124">Jeśli określono polecenie cmdlet Write-in polecenia "in" w przypadku powodzenia.</span><span class="sxs-lookup"><span data-stu-id="e8164-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="e8164-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8164-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8164-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8164-126">The resource group name.</span></span>

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

### <span data-ttu-id="e8164-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="e8164-127">-TriggerName</span></span>
<span data-ttu-id="e8164-128">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e8164-128">The trigger name.</span></span>

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

### <span data-ttu-id="e8164-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="e8164-129">-TriggerRunId</span></span>
<span data-ttu-id="e8164-130">Identyfikator uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="e8164-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="e8164-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8164-131">-Confirm</span></span>
<span data-ttu-id="e8164-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8164-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8164-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8164-133">-WhatIf</span></span>
<span data-ttu-id="e8164-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8164-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8164-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8164-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8164-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8164-136">CommonParameters</span></span>
<span data-ttu-id="e8164-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8164-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8164-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8164-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8164-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8164-139">INPUTS</span></span>

### <span data-ttu-id="e8164-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="e8164-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="e8164-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e8164-141">System.String</span></span>

### <span data-ttu-id="e8164-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e8164-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e8164-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8164-143">OUTPUTS</span></span>

### <span data-ttu-id="e8164-144">Microsoft. Azure. Commands. DataFactoryV2. models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e8164-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="e8164-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8164-145">NOTES</span></span>

## <span data-ttu-id="e8164-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8164-146">RELATED LINKS</span></span>
