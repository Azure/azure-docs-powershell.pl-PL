---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: a278b316a62639c6c33d4f05491e314a2b9a1e85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383350"
---
# <span data-ttu-id="2fdf3-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="2fdf3-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="2fdf3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fdf3-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdf3-103">Usuwa typy informacji i etykiety liter kolumn w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="2fdf3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fdf3-104">SYNTAX</span></span>

### <span data-ttu-id="2fdf3-105">ClassificationObjectParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2fdf3-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fdf3-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fdf3-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fdf3-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fdf3-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fdf3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2fdf3-108">DESCRIPTION</span></span>
<span data-ttu-id="2fdf3-109">Polecenie cmdlet Remove-AzSynapseSqlPoolSensitivityClassification usuwa typy informacji oraz etykiety liter kolumn w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="2fdf3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fdf3-110">EXAMPLES</span></span>

### <span data-ttu-id="2fdf3-111">Przykład 1: usuwanie typu informacji i etykiety wrażliwości kolumny w puli platformy Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="2fdf3-112">Przykład 2: usuwanie bieżących typów informacji i etykiet liter kolumn w puli usługi Azure Synapse SQL przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="2fdf3-113">Przykład 3: usuwanie typu informacji i etykiety wrażliwości kolumny w puli usługi Azure Synapse SQL przy użyciu połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="2fdf3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fdf3-114">PARAMETERS</span></span>

### <span data-ttu-id="2fdf3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fdf3-115">-AsJob</span></span>
<span data-ttu-id="2fdf3-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2fdf3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fdf3-117">-Klasyfikacyjnobject</span><span class="sxs-lookup"><span data-stu-id="2fdf3-117">-ClassificationObject</span></span>
<span data-ttu-id="2fdf3-118">Obiekt reprezentujący klasyfikację wrażliwości puli SQL.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="2fdf3-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="2fdf3-119">-ColumnName</span></span>
<span data-ttu-id="2fdf3-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-120">Name of column.</span></span>

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

### <span data-ttu-id="2fdf3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdf3-121">-DefaultProfile</span></span>
<span data-ttu-id="2fdf3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fdf3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fdf3-123">-PassThru</span></span>
<span data-ttu-id="2fdf3-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2fdf3-125">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2fdf3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fdf3-126">-ResourceGroupName</span></span>
<span data-ttu-id="2fdf3-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-127">Resource group name.</span></span>

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

### <span data-ttu-id="2fdf3-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="2fdf3-128">-SchemaName</span></span>
<span data-ttu-id="2fdf3-129">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-129">Name of schema.</span></span>

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

### <span data-ttu-id="2fdf3-130">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="2fdf3-130">-SqlPoolName</span></span>
<span data-ttu-id="2fdf3-131">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="2fdf3-132">-Sqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="2fdf3-132">-SqlPoolObject</span></span>
<span data-ttu-id="2fdf3-133">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2fdf3-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="2fdf3-134">-TableName</span></span>
<span data-ttu-id="2fdf3-135">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-135">Name of table.</span></span>

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

### <span data-ttu-id="2fdf3-136">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="2fdf3-136">-WorkspaceName</span></span>
<span data-ttu-id="2fdf3-137">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2fdf3-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2fdf3-138">-Confirm</span></span>
<span data-ttu-id="2fdf3-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fdf3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fdf3-140">-WhatIf</span></span>
<span data-ttu-id="2fdf3-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fdf3-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fdf3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdf3-143">CommonParameters</span></span>
<span data-ttu-id="2fdf3-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fdf3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdf3-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fdf3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdf3-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fdf3-146">INPUTS</span></span>

### <span data-ttu-id="2fdf3-147">Microsoft. Azure. Commands. Synapse. models. dataklasyfikacyjn. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="2fdf3-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="2fdf3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2fdf3-148">System.String</span></span>

### <span data-ttu-id="2fdf3-149">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2fdf3-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="2fdf3-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fdf3-150">OUTPUTS</span></span>

### <span data-ttu-id="2fdf3-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2fdf3-151">System.Boolean</span></span>

## <span data-ttu-id="2fdf3-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fdf3-152">NOTES</span></span>

## <span data-ttu-id="2fdf3-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fdf3-153">RELATED LINKS</span></span>
