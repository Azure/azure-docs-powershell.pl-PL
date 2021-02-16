---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: bb47d791f23df044e5a4677835f85b6f107f2822
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182674"
---
# <span data-ttu-id="94864-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="94864-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="94864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94864-102">SYNOPSIS</span></span>
<span data-ttu-id="94864-103">Ustawia typy informacji i etykiety wrażliwości kolumn w puli sql.</span><span class="sxs-lookup"><span data-stu-id="94864-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="94864-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94864-104">SYNTAX</span></span>

### <span data-ttu-id="94864-105">ClassificationObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="94864-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94864-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="94864-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94864-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="94864-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94864-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="94864-108">DESCRIPTION</span></span>
<span data-ttu-id="94864-109">Polecenie Set-AzSynapseSqlPoolSensitivityClassification cmdlet ustawia typy informacji i etykiety wrażliwości kolumn w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="94864-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="94864-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94864-110">EXAMPLES</span></span>

### <span data-ttu-id="94864-111">Przykład 1. Ustawianie typu informacji i etykiety wrażliwości kolumny w puli sql Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="94864-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="94864-112">Przykład 2. Ustawianie zalecanych typów informacji i etykiet wrażliwości kolumn w puli języka SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="94864-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="94864-113">Przykład 3. Ustawianie typu informacji i etykiety wrażliwości kolumny w puli SQL Synapse Azure przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="94864-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="94864-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94864-114">PARAMETERS</span></span>

### <span data-ttu-id="94864-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="94864-115">-AsJob</span></span>
<span data-ttu-id="94864-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="94864-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94864-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="94864-117">-ClassificationObject</span></span>
<span data-ttu-id="94864-118">Obiekt reprezentujący klasyfikację wrażliwości puli języka SQL.</span><span class="sxs-lookup"><span data-stu-id="94864-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="94864-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="94864-119">-ColumnName</span></span>
<span data-ttu-id="94864-120">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="94864-120">Name of column.</span></span>

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

### <span data-ttu-id="94864-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94864-121">-DefaultProfile</span></span>
<span data-ttu-id="94864-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94864-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94864-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="94864-123">-InformationType</span></span>
<span data-ttu-id="94864-124">Nazwa opisującą typ informacji przechowywanych w kolumnie.</span><span class="sxs-lookup"><span data-stu-id="94864-124">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94864-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94864-125">-PassThru</span></span>
<span data-ttu-id="94864-126">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="94864-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="94864-127">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="94864-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="94864-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94864-128">-ResourceGroupName</span></span>
<span data-ttu-id="94864-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94864-129">Resource group name.</span></span>

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

### <span data-ttu-id="94864-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="94864-130">-SchemaName</span></span>
<span data-ttu-id="94864-131">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="94864-131">Name of schema.</span></span>

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

### <span data-ttu-id="94864-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="94864-132">-SensitivityLabel</span></span>
<span data-ttu-id="94864-133">Nazwa opisującą charakter danych przechowywanych w kolumnie.</span><span class="sxs-lookup"><span data-stu-id="94864-133">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94864-134">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="94864-134">-SqlPoolName</span></span>
<span data-ttu-id="94864-135">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="94864-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="94864-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="94864-136">-SqlPoolObject</span></span>
<span data-ttu-id="94864-137">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="94864-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="94864-138">-TableName</span><span class="sxs-lookup"><span data-stu-id="94864-138">-TableName</span></span>
<span data-ttu-id="94864-139">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="94864-139">Name of table.</span></span>

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

### <span data-ttu-id="94864-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="94864-140">-WorkspaceName</span></span>
<span data-ttu-id="94864-141">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="94864-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="94864-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94864-142">-Confirm</span></span>
<span data-ttu-id="94864-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="94864-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94864-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94864-144">-WhatIf</span></span>
<span data-ttu-id="94864-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94864-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94864-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="94864-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94864-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94864-147">CommonParameters</span></span>
<span data-ttu-id="94864-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94864-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94864-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94864-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94864-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94864-150">INPUTS</span></span>

### <span data-ttu-id="94864-151">System.String</span><span class="sxs-lookup"><span data-stu-id="94864-151">System.String</span></span>

### <span data-ttu-id="94864-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="94864-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="94864-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="94864-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="94864-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94864-154">OUTPUTS</span></span>

### <span data-ttu-id="94864-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94864-155">System.Boolean</span></span>

## <span data-ttu-id="94864-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94864-156">NOTES</span></span>

## <span data-ttu-id="94864-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94864-157">RELATED LINKS</span></span>
