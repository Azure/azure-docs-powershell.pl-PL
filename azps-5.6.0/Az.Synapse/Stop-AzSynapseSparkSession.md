---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: 204166bc48e01ea186ca18ad5aa95b0dcf05192a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991971"
---
# <span data-ttu-id="9099b-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9099b-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="9099b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9099b-102">SYNOPSIS</span></span>
<span data-ttu-id="9099b-103">Zatrzymuje sesję analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9099b-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9099b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9099b-104">SYNTAX</span></span>

### <span data-ttu-id="9099b-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9099b-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9099b-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9099b-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9099b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9099b-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9099b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9099b-108">DESCRIPTION</span></span>
<span data-ttu-id="9099b-109">Polecenie **cmdlet Stop-AzSynapseSparkSession** zatrzymuje sesję przebiegu w czasie analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9099b-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9099b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9099b-110">EXAMPLES</span></span>

### <span data-ttu-id="9099b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9099b-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="9099b-112">To polecenie zatrzymuje sesję analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9099b-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="9099b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9099b-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="9099b-114">To polecenie zatrzymuje sesję analizy Synapse Analytics na czas w potoku.</span><span class="sxs-lookup"><span data-stu-id="9099b-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="9099b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9099b-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="9099b-116">To polecenie zatrzymuje sesję analizy Synapse Analytics na czas potoku.</span><span class="sxs-lookup"><span data-stu-id="9099b-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="9099b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9099b-117">PARAMETERS</span></span>

### <span data-ttu-id="9099b-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9099b-118">-AsJob</span></span>
<span data-ttu-id="9099b-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9099b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9099b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9099b-120">-DefaultProfile</span></span>
<span data-ttu-id="9099b-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9099b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9099b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9099b-122">-InputObject</span></span>
<span data-ttu-id="9099b-123">Obiekt wprowadzania sesji przebiegu w przebiegu w trakcie przebiegu w trakcie potoku.</span><span class="sxs-lookup"><span data-stu-id="9099b-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9099b-124">- Natłok</span><span class="sxs-lookup"><span data-stu-id="9099b-124">-LivyId</span></span>
<span data-ttu-id="9099b-125">Identyfikator sesji przebiegu w przebiegu w trakcie.</span><span class="sxs-lookup"><span data-stu-id="9099b-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="9099b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9099b-126">-PassThru</span></span>
<span data-ttu-id="9099b-127">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="9099b-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9099b-128">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="9099b-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9099b-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9099b-129">-SparkPoolName</span></span>
<span data-ttu-id="9099b-130">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="9099b-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="9099b-131">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="9099b-131">-SparkPoolObject</span></span>
<span data-ttu-id="9099b-132">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="9099b-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9099b-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9099b-133">-WorkspaceName</span></span>
<span data-ttu-id="9099b-134">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="9099b-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9099b-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9099b-135">-Confirm</span></span>
<span data-ttu-id="9099b-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9099b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9099b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9099b-137">-WhatIf</span></span>
<span data-ttu-id="9099b-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9099b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9099b-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9099b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9099b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9099b-140">CommonParameters</span></span>
<span data-ttu-id="9099b-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9099b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9099b-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9099b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9099b-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9099b-143">INPUTS</span></span>

### <span data-ttu-id="9099b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9099b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="9099b-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9099b-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="9099b-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9099b-146">OUTPUTS</span></span>

### <span data-ttu-id="9099b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9099b-147">System.Boolean</span></span>

## <span data-ttu-id="9099b-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9099b-148">NOTES</span></span>

## <span data-ttu-id="9099b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9099b-149">RELATED LINKS</span></span>
