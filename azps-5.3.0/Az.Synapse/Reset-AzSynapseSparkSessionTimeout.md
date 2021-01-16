---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: cccc0d3cffd9eb313e2983d81a3492bdf89e9e44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383313"
---
# <span data-ttu-id="7d532-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="7d532-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="7d532-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d532-102">SYNOPSIS</span></span>
<span data-ttu-id="7d532-103">Resetuje limit czasu sesji usługi Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="7d532-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="7d532-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d532-104">SYNTAX</span></span>

### <span data-ttu-id="7d532-105">ResetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7d532-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d532-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d532-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d532-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d532-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d532-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7d532-108">DESCRIPTION</span></span>
<span data-ttu-id="7d532-109">Polecenie cmdlet **Remove-AzSynapseSparkSessionTimeout** resetuje limit czasu sesji usługi Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="7d532-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="7d532-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d532-110">EXAMPLES</span></span>

### <span data-ttu-id="7d532-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d532-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="7d532-112">To polecenie resetuje limit czasu sesji Synapse analiz Spark z określonym IDENTYFIKATORem livy.</span><span class="sxs-lookup"><span data-stu-id="7d532-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="7d532-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7d532-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="7d532-114">To polecenie resetuje limit czasu sesji Synapse Analytics Spark z określonym IDENTYFIKATORem livy za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="7d532-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="7d532-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7d532-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="7d532-116">To polecenie resetuje limit czasu sesji Synapse Analytics Spark z określonym IDENTYFIKATORem livy za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="7d532-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="7d532-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d532-117">PARAMETERS</span></span>

### <span data-ttu-id="7d532-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d532-118">-AsJob</span></span>
<span data-ttu-id="7d532-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7d532-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d532-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d532-120">-DefaultProfile</span></span>
<span data-ttu-id="7d532-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d532-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d532-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7d532-122">-InputObject</span></span>
<span data-ttu-id="7d532-123">Obiekt wejściowy sesji usługi Spark, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="7d532-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: ResetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d532-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="7d532-124">-LivyId</span></span>
<span data-ttu-id="7d532-125">Identyfikator sesji usługi Spark.</span><span class="sxs-lookup"><span data-stu-id="7d532-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResetByNameParameterSet, ResetByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d532-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d532-126">-PassThru</span></span>
<span data-ttu-id="7d532-127">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="7d532-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="7d532-128">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="7d532-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7d532-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="7d532-129">-SparkPoolName</span></span>
<span data-ttu-id="7d532-130">Nazwa puli Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="7d532-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d532-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="7d532-131">-SparkPoolObject</span></span>
<span data-ttu-id="7d532-132">Obiekt wejściowy usługi Spark Pool, zazwyczaj przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="7d532-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: ResetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d532-133">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="7d532-133">-WorkspaceName</span></span>
<span data-ttu-id="7d532-134">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="7d532-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d532-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d532-135">-Confirm</span></span>
<span data-ttu-id="7d532-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d532-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d532-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d532-137">-WhatIf</span></span>
<span data-ttu-id="7d532-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d532-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d532-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7d532-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d532-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d532-140">CommonParameters</span></span>
<span data-ttu-id="7d532-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d532-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d532-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d532-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d532-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d532-143">INPUTS</span></span>

### <span data-ttu-id="7d532-144">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="7d532-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="7d532-145">Microsoft. Azure. Commands. Synapse. models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="7d532-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="7d532-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d532-146">OUTPUTS</span></span>

### <span data-ttu-id="7d532-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d532-147">System.Boolean</span></span>

## <span data-ttu-id="7d532-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d532-148">NOTES</span></span>

## <span data-ttu-id="7d532-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d532-149">RELATED LINKS</span></span>
