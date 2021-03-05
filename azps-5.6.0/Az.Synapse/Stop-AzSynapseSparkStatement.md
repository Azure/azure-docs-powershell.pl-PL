---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: a14079c92a59864b98dd086d8e65a340e2a277d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991964"
---
# <span data-ttu-id="efd73-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="efd73-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="efd73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efd73-102">SYNOPSIS</span></span>
<span data-ttu-id="efd73-103">Anulowanie instrukcji Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="efd73-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="efd73-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="efd73-104">SYNTAX</span></span>

### <span data-ttu-id="efd73-105">StopSparkStatementByIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="efd73-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd73-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efd73-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efd73-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="efd73-107">DESCRIPTION</span></span>
<span data-ttu-id="efd73-108">Polecenie **cmdlet Stop-AzSynapseSparkStatement** anuluje instrukcja Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="efd73-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="efd73-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="efd73-109">EXAMPLES</span></span>

### <span data-ttu-id="efd73-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="efd73-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="efd73-111">To polecenie anuluje instrukcja Spark z określonym identyfikatorem przebiegu w czasie.</span><span class="sxs-lookup"><span data-stu-id="efd73-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="efd73-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="efd73-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="efd73-113">To polecenie anuluje instrukcja Spark z określonym identyfikatorem przebiegu w potoku.</span><span class="sxs-lookup"><span data-stu-id="efd73-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="efd73-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efd73-114">PARAMETERS</span></span>

### <span data-ttu-id="efd73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd73-115">-DefaultProfile</span></span>
<span data-ttu-id="efd73-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="efd73-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efd73-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="efd73-117">-Force</span></span>
<span data-ttu-id="efd73-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="efd73-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="efd73-119">- Natłok</span><span class="sxs-lookup"><span data-stu-id="efd73-119">-LivyId</span></span>
<span data-ttu-id="efd73-120">Identyfikator instrukcji Spark.</span><span class="sxs-lookup"><span data-stu-id="efd73-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd73-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efd73-121">-PassThru</span></span>
<span data-ttu-id="efd73-122">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="efd73-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="efd73-123">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="efd73-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="efd73-124">- SessionId</span><span class="sxs-lookup"><span data-stu-id="efd73-124">-SessionId</span></span>
<span data-ttu-id="efd73-125">Identyfikator sesji przebiegu w przebiegu w trakcie.</span><span class="sxs-lookup"><span data-stu-id="efd73-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd73-126">- SessionObject</span><span class="sxs-lookup"><span data-stu-id="efd73-126">-SessionObject</span></span>
<span data-ttu-id="efd73-127">Obiekt wprowadzania sesji przebiegu w przebiegu w trakcie przebiegu w trakcie potoku.</span><span class="sxs-lookup"><span data-stu-id="efd73-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efd73-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="efd73-128">-SparkPoolName</span></span>
<span data-ttu-id="efd73-129">Nazwa puli przebiegu w czasie synpsy.</span><span class="sxs-lookup"><span data-stu-id="efd73-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd73-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="efd73-130">-WorkspaceName</span></span>
<span data-ttu-id="efd73-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="efd73-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd73-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efd73-132">-Confirm</span></span>
<span data-ttu-id="efd73-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="efd73-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efd73-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efd73-134">-WhatIf</span></span>
<span data-ttu-id="efd73-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efd73-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efd73-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="efd73-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efd73-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd73-137">CommonParameters</span></span>
<span data-ttu-id="efd73-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efd73-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd73-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efd73-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd73-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efd73-140">INPUTS</span></span>

### <span data-ttu-id="efd73-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="efd73-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="efd73-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efd73-142">OUTPUTS</span></span>

### <span data-ttu-id="efd73-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="efd73-143">System.Boolean</span></span>

## <span data-ttu-id="efd73-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="efd73-144">NOTES</span></span>

## <span data-ttu-id="efd73-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efd73-145">RELATED LINKS</span></span>
