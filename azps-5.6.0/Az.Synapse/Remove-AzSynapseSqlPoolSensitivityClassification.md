---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 58ef691f5f109f301ffae2636d739405000754ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959969"
---
# <span data-ttu-id="cae43-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="cae43-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="cae43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cae43-102">SYNOPSIS</span></span>
<span data-ttu-id="cae43-103">Usuwa typy informacji i etykiety wrażliwości kolumn w puli sql.</span><span class="sxs-lookup"><span data-stu-id="cae43-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="cae43-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cae43-104">SYNTAX</span></span>

### <span data-ttu-id="cae43-105">ClassificationObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cae43-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae43-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="cae43-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae43-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="cae43-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae43-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cae43-108">DESCRIPTION</span></span>
<span data-ttu-id="cae43-109">Polecenie Remove-AzSynapseSqlPoolSensitivityClassification cmdlet usuwa typy informacji i etykiety wrażliwości kolumn w puli sql.</span><span class="sxs-lookup"><span data-stu-id="cae43-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="cae43-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cae43-110">EXAMPLES</span></span>

### <span data-ttu-id="cae43-111">Przykład 1. Usuwanie typu informacji i etykiety wrażliwości kolumny w puli języka SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="cae43-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="cae43-112">Przykład 2. Usuwanie bieżących typów informacji i etykiet wrażliwości kolumn w puli sql Synapse Azure przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="cae43-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="cae43-113">Przykład 3. Usuwanie typu informacji i etykiety wrażliwości kolumny w puli sql Synapse Azure przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="cae43-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="cae43-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cae43-114">PARAMETERS</span></span>

### <span data-ttu-id="cae43-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cae43-115">-AsJob</span></span>
<span data-ttu-id="cae43-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cae43-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cae43-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="cae43-117">-ClassificationObject</span></span>
<span data-ttu-id="cae43-118">Obiekt reprezentujący klasyfikację wrażliwości puli języka SQL.</span><span class="sxs-lookup"><span data-stu-id="cae43-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae43-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="cae43-119">-ColumnName</span></span>
<span data-ttu-id="cae43-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="cae43-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae43-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae43-121">-DefaultProfile</span></span>
<span data-ttu-id="cae43-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cae43-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cae43-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cae43-123">-PassThru</span></span>
<span data-ttu-id="cae43-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="cae43-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cae43-125">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="cae43-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cae43-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae43-126">-ResourceGroupName</span></span>
<span data-ttu-id="cae43-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cae43-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae43-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="cae43-128">-SchemaName</span></span>
<span data-ttu-id="cae43-129">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="cae43-129">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae43-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="cae43-130">-SqlPoolName</span></span>
<span data-ttu-id="cae43-131">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="cae43-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae43-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="cae43-132">-SqlPoolObject</span></span>
<span data-ttu-id="cae43-133">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="cae43-133">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae43-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="cae43-134">-TableName</span></span>
<span data-ttu-id="cae43-135">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="cae43-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae43-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cae43-136">-WorkspaceName</span></span>
<span data-ttu-id="cae43-137">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="cae43-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae43-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cae43-138">-Confirm</span></span>
<span data-ttu-id="cae43-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cae43-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae43-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae43-140">-WhatIf</span></span>
<span data-ttu-id="cae43-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae43-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cae43-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cae43-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae43-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae43-143">CommonParameters</span></span>
<span data-ttu-id="cae43-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae43-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae43-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cae43-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae43-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cae43-146">INPUTS</span></span>

### <span data-ttu-id="cae43-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="cae43-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="cae43-148">System.String</span><span class="sxs-lookup"><span data-stu-id="cae43-148">System.String</span></span>

### <span data-ttu-id="cae43-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="cae43-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="cae43-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cae43-150">OUTPUTS</span></span>

### <span data-ttu-id="cae43-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cae43-151">System.Boolean</span></span>

## <span data-ttu-id="cae43-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cae43-152">NOTES</span></span>

## <span data-ttu-id="cae43-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cae43-153">RELATED LINKS</span></span>
