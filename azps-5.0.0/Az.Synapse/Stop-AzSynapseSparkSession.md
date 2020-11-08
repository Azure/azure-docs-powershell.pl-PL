---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224708"
---
# <span data-ttu-id="9ca11-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9ca11-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="9ca11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ca11-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca11-103">Zatrzymuje sesję Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9ca11-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9ca11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ca11-104">SYNTAX</span></span>

### <span data-ttu-id="9ca11-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ca11-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca11-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca11-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca11-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca11-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ca11-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9ca11-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca11-109">Polecenie cmdlet **stop-AzSynapseSparkSession** zatrzymuje sesję usługi Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9ca11-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9ca11-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ca11-110">EXAMPLES</span></span>

### <span data-ttu-id="9ca11-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ca11-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="9ca11-112">To polecenie zatrzymuje sesję funkcji Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9ca11-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="9ca11-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9ca11-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="9ca11-114">To polecenie zatrzymuje sesję usługi Synapse Analytics Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="9ca11-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="9ca11-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9ca11-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="9ca11-116">To polecenie zatrzymuje sesję usługi Synapse Analytics Spark za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="9ca11-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="9ca11-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ca11-117">PARAMETERS</span></span>

### <span data-ttu-id="9ca11-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ca11-118">-AsJob</span></span>
<span data-ttu-id="9ca11-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9ca11-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ca11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca11-120">-DefaultProfile</span></span>
<span data-ttu-id="9ca11-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca11-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca11-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ca11-122">-InputObject</span></span>
<span data-ttu-id="9ca11-123">Obiekt wejściowy sesji usługi Spark, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="9ca11-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca11-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="9ca11-124">-LivyId</span></span>
<span data-ttu-id="9ca11-125">Identyfikator sesji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="9ca11-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca11-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ca11-126">-PassThru</span></span>
<span data-ttu-id="9ca11-127">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="9ca11-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9ca11-128">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="9ca11-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9ca11-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9ca11-129">-SparkPoolName</span></span>
<span data-ttu-id="9ca11-130">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="9ca11-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca11-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="9ca11-131">-SparkPoolObject</span></span>
<span data-ttu-id="9ca11-132">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="9ca11-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca11-133">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="9ca11-133">-WorkspaceName</span></span>
<span data-ttu-id="9ca11-134">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="9ca11-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca11-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ca11-135">-Confirm</span></span>
<span data-ttu-id="9ca11-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ca11-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ca11-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca11-137">-WhatIf</span></span>
<span data-ttu-id="9ca11-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ca11-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ca11-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ca11-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ca11-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca11-140">CommonParameters</span></span>
<span data-ttu-id="9ca11-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ca11-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca11-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ca11-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca11-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ca11-143">INPUTS</span></span>

### <span data-ttu-id="9ca11-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9ca11-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="9ca11-145">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9ca11-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="9ca11-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ca11-146">OUTPUTS</span></span>

### <span data-ttu-id="9ca11-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ca11-147">System.Boolean</span></span>

## <span data-ttu-id="9ca11-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ca11-148">NOTES</span></span>

## <span data-ttu-id="9ca11-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ca11-149">RELATED LINKS</span></span>
