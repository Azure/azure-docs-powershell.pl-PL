---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: ceeb33615748b7cf11c13441399bbae6a934a56f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383364"
---
# <span data-ttu-id="f87be-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f87be-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="f87be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f87be-102">SYNOPSIS</span></span>
<span data-ttu-id="f87be-103">Usuwa punkt przywracania puli SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f87be-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="f87be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f87be-104">SYNTAX</span></span>

### <span data-ttu-id="f87be-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f87be-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f87be-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f87be-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f87be-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f87be-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f87be-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f87be-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f87be-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f87be-109">DESCRIPTION</span></span>
<span data-ttu-id="f87be-110">Polecenie cmdlet **Remove-AzSynapseSqlPoolRestorePoint** powoduje trwałe usunięcie punktu przywracania puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f87be-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="f87be-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f87be-111">EXAMPLES</span></span>

### <span data-ttu-id="f87be-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f87be-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="f87be-113">To polecenie usuwa punkt przywracania puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f87be-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="f87be-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f87be-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="f87be-115">To polecenie usuwa punkt przywracania puli usługi Azure Synapse analiza SQL przez potok.</span><span class="sxs-lookup"><span data-stu-id="f87be-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="f87be-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f87be-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="f87be-117">To polecenie usuwa punkt przywracania puli usługi Azure Synapse analiza SQL przez potok.</span><span class="sxs-lookup"><span data-stu-id="f87be-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="f87be-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f87be-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="f87be-119">To polecenie usuwa punkt przywracania puli SQL usługi Azure Synapse Analytics z określonym IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="f87be-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="f87be-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f87be-120">PARAMETERS</span></span>

### <span data-ttu-id="f87be-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f87be-121">-AsJob</span></span>
<span data-ttu-id="f87be-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f87be-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f87be-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87be-123">-DefaultProfile</span></span>
<span data-ttu-id="f87be-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f87be-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f87be-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f87be-125">-Force</span></span>
<span data-ttu-id="f87be-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f87be-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f87be-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f87be-127">-InputObject</span></span>
<span data-ttu-id="f87be-128">Obiekt wejściowy czasu tworzenia punktu przywracania puli SQL, przeważnie przekazano go przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f87be-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f87be-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f87be-129">-PassThru</span></span>
<span data-ttu-id="f87be-130">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="f87be-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="f87be-131">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="f87be-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f87be-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f87be-132">-ResourceGroupName</span></span>
<span data-ttu-id="f87be-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f87be-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f87be-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f87be-134">-ResourceId</span></span>
<span data-ttu-id="f87be-135">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f87be-135">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f87be-136">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="f87be-136">-RestorePointCreationDate</span></span>
<span data-ttu-id="f87be-137">Nazwa daty utworzenia punktu przywracania SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f87be-137">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f87be-138">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="f87be-138">-SqlPoolName</span></span>
<span data-ttu-id="f87be-139">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f87be-139">Name of Synapse Sql pool.</span></span>

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

### <span data-ttu-id="f87be-140">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="f87be-140">-SqlPoolObject</span></span>
<span data-ttu-id="f87be-141">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f87be-141">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f87be-142">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f87be-142">-WorkspaceName</span></span>
<span data-ttu-id="f87be-143">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f87be-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f87be-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f87be-144">-Confirm</span></span>
<span data-ttu-id="f87be-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f87be-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f87be-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f87be-146">-WhatIf</span></span>
<span data-ttu-id="f87be-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f87be-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f87be-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f87be-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f87be-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87be-149">CommonParameters</span></span>
<span data-ttu-id="f87be-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87be-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87be-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f87be-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87be-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f87be-152">INPUTS</span></span>

### <span data-ttu-id="f87be-153">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f87be-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f87be-154">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f87be-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="f87be-155">Microsoft. Azure. Commands. Synapse. models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f87be-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="f87be-156">System. String</span><span class="sxs-lookup"><span data-stu-id="f87be-156">System.String</span></span>

## <span data-ttu-id="f87be-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f87be-157">OUTPUTS</span></span>

### <span data-ttu-id="f87be-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f87be-158">System.Boolean</span></span>

## <span data-ttu-id="f87be-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f87be-159">NOTES</span></span>

## <span data-ttu-id="f87be-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f87be-160">RELATED LINKS</span></span>
