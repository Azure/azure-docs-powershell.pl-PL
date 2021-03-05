---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: 485558c47fa8b879999777b79341fc855085b81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973713"
---
# <span data-ttu-id="0aaed-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="0aaed-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="0aaed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aaed-102">SYNOPSIS</span></span>
<span data-ttu-id="0aaed-103">Resetuje limit czasu sesji analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0aaed-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="0aaed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0aaed-104">SYNTAX</span></span>

### <span data-ttu-id="0aaed-105">ResetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0aaed-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aaed-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aaed-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aaed-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aaed-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aaed-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0aaed-108">DESCRIPTION</span></span>
<span data-ttu-id="0aaed-109">Polecenie **cmdlet Remove-AzSynapseSparkSessionTimeout** resetuje limit czasu sesji analizy Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="0aaed-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="0aaed-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0aaed-110">EXAMPLES</span></span>

### <span data-ttu-id="0aaed-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0aaed-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="0aaed-112">To polecenie resetuje limit czasu sesji Analizy Synpsy z określonym identyfikatorem użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0aaed-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="0aaed-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0aaed-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="0aaed-114">To polecenie resetuje limit czasu sesji Analizy Synapse (Spark) z określonym identyfikatorem identyfikacyjnym w potoku.</span><span class="sxs-lookup"><span data-stu-id="0aaed-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="0aaed-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0aaed-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="0aaed-116">To polecenie resetuje limit czasu sesji Analizy Synapse (Spark) z określonym identyfikatorem identyfikacyjnym w potoku.</span><span class="sxs-lookup"><span data-stu-id="0aaed-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="0aaed-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0aaed-117">PARAMETERS</span></span>

### <span data-ttu-id="0aaed-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0aaed-118">-AsJob</span></span>
<span data-ttu-id="0aaed-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0aaed-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0aaed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aaed-120">-DefaultProfile</span></span>
<span data-ttu-id="0aaed-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0aaed-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aaed-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aaed-122">-InputObject</span></span>
<span data-ttu-id="0aaed-123">Obiekt wprowadzania sesji przebiegu w przebiegu w trakcie przebiegu w trakcie potoku.</span><span class="sxs-lookup"><span data-stu-id="0aaed-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0aaed-124">- Natłok</span><span class="sxs-lookup"><span data-stu-id="0aaed-124">-LivyId</span></span>
<span data-ttu-id="0aaed-125">Identyfikator sesji przebiegu w przebiegu w trakcie.</span><span class="sxs-lookup"><span data-stu-id="0aaed-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="0aaed-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0aaed-126">-PassThru</span></span>
<span data-ttu-id="0aaed-127">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="0aaed-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="0aaed-128">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="0aaed-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0aaed-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="0aaed-129">-SparkPoolName</span></span>
<span data-ttu-id="0aaed-130">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="0aaed-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="0aaed-131">— SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="0aaed-131">-SparkPoolObject</span></span>
<span data-ttu-id="0aaed-132">Obiekt wejściowy puli przebiegu w przebiegu w przebiegu, który zwykle przeszedł przez potok.</span><span class="sxs-lookup"><span data-stu-id="0aaed-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0aaed-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0aaed-133">-WorkspaceName</span></span>
<span data-ttu-id="0aaed-134">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="0aaed-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0aaed-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0aaed-135">-Confirm</span></span>
<span data-ttu-id="0aaed-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0aaed-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aaed-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aaed-137">-WhatIf</span></span>
<span data-ttu-id="0aaed-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aaed-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aaed-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0aaed-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aaed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aaed-140">CommonParameters</span></span>
<span data-ttu-id="0aaed-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aaed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aaed-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0aaed-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aaed-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0aaed-143">INPUTS</span></span>

### <span data-ttu-id="0aaed-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="0aaed-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="0aaed-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="0aaed-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="0aaed-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0aaed-146">OUTPUTS</span></span>

### <span data-ttu-id="0aaed-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0aaed-147">System.Boolean</span></span>

## <span data-ttu-id="0aaed-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0aaed-148">NOTES</span></span>

## <span data-ttu-id="0aaed-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0aaed-149">RELATED LINKS</span></span>
