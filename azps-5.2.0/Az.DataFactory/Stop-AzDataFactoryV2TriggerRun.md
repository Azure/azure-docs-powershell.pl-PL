---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330346"
---
# <span data-ttu-id="1ee67-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="1ee67-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="1ee67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ee67-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee67-103">Zatrzymuje działanie wyzwalacza w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="1ee67-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="1ee67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ee67-104">SYNTAX</span></span>

### <span data-ttu-id="1ee67-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1ee67-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ee67-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1ee67-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ee67-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1ee67-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ee67-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1ee67-108">DESCRIPTION</span></span>
<span data-ttu-id="1ee67-109">Polecenie cmdlet **stop-AzDataFactoryV2TriggerRun** zatrzymuje uruchamianie wyzwalacza w fabryce danych określonej przy użyciu nazwy wyzwalacza i identyfikatora uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="1ee67-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="1ee67-110">Obecnie obsługiwane tylko dla TumblingWindowTriggers w stanie WaitingOnDependency.</span><span class="sxs-lookup"><span data-stu-id="1ee67-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="1ee67-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ee67-111">EXAMPLES</span></span>

### <span data-ttu-id="1ee67-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ee67-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="1ee67-113">To polecenie zatrzymuje uruchamianie wyzwalacza z identyfikatorem "08586002468005888497807248799CU16" w WikiADF fabryki.</span><span class="sxs-lookup"><span data-stu-id="1ee67-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="1ee67-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ee67-114">PARAMETERS</span></span>

### <span data-ttu-id="1ee67-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1ee67-115">-DataFactory</span></span>
<span data-ttu-id="1ee67-116">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1ee67-116">The data factory object.</span></span>

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

### <span data-ttu-id="1ee67-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1ee67-117">-DataFactoryName</span></span>
<span data-ttu-id="1ee67-118">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="1ee67-118">The data factory name.</span></span>

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

### <span data-ttu-id="1ee67-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee67-119">-DefaultProfile</span></span>
<span data-ttu-id="1ee67-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee67-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ee67-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1ee67-121">-InputObject</span></span>
<span data-ttu-id="1ee67-122">Informacje na temat uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="1ee67-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="1ee67-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ee67-123">-PassThru</span></span>
<span data-ttu-id="1ee67-124">Jeśli określono polecenie cmdlet Write-in polecenia "in" w przypadku powodzenia.</span><span class="sxs-lookup"><span data-stu-id="1ee67-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="1ee67-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ee67-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ee67-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ee67-126">The resource group name.</span></span>

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

### <span data-ttu-id="1ee67-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="1ee67-127">-TriggerName</span></span>
<span data-ttu-id="1ee67-128">Nazwa wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="1ee67-128">The trigger name.</span></span>

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

### <span data-ttu-id="1ee67-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="1ee67-129">-TriggerRunId</span></span>
<span data-ttu-id="1ee67-130">Identyfikator uruchomienia wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="1ee67-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="1ee67-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ee67-131">-Confirm</span></span>
<span data-ttu-id="1ee67-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee67-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ee67-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee67-133">-WhatIf</span></span>
<span data-ttu-id="1ee67-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ee67-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ee67-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ee67-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ee67-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee67-136">CommonParameters</span></span>
<span data-ttu-id="1ee67-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ee67-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee67-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ee67-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee67-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ee67-139">INPUTS</span></span>

### <span data-ttu-id="1ee67-140">Microsoft. Azure. Commands. DataFactoryV2. models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="1ee67-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="1ee67-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1ee67-141">System.String</span></span>

### <span data-ttu-id="1ee67-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1ee67-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1ee67-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ee67-143">OUTPUTS</span></span>

### <span data-ttu-id="1ee67-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ee67-144">System.Boolean</span></span>

## <span data-ttu-id="1ee67-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ee67-145">NOTES</span></span>

## <span data-ttu-id="1ee67-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ee67-146">RELATED LINKS</span></span>
