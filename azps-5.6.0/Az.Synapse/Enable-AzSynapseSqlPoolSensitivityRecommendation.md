---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 40d1fe07db7720bfb9fdad061ac3d57298d86a8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977953"
---
# <span data-ttu-id="7c86a-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="7c86a-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="7c86a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c86a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c86a-103">Włącza zalecenia wrażliwości dla kolumn (zalecenia są domyślnie włączone we wszystkich kolumnach) w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="7c86a-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="7c86a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7c86a-104">SYNTAX</span></span>

### <span data-ttu-id="7c86a-105">InputObjectParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7c86a-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c86a-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c86a-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c86a-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c86a-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c86a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7c86a-108">DESCRIPTION</span></span>
<span data-ttu-id="7c86a-109">Polecenie Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet umożliwia wyświetlanie rekomendacji wrażliwości kolumn w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="7c86a-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="7c86a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7c86a-110">EXAMPLES</span></span>

### <span data-ttu-id="7c86a-111">Przykład 1. Włączanie rekomendacji wrażliwości dla danej kolumny w puli SQL Synapse Azure.</span><span class="sxs-lookup"><span data-stu-id="7c86a-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="7c86a-112">Przykład 2. Włączanie rekomendacji wrażliwości dla danej kolumny Pula SQL Azure Synapse przy użyciu połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="7c86a-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="7c86a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c86a-113">PARAMETERS</span></span>

### <span data-ttu-id="7c86a-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7c86a-114">-AsJob</span></span>
<span data-ttu-id="7c86a-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7c86a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c86a-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="7c86a-116">-ColumnName</span></span>
<span data-ttu-id="7c86a-117">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="7c86a-117">Name of column.</span></span>

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

### <span data-ttu-id="7c86a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c86a-118">-DefaultProfile</span></span>
<span data-ttu-id="7c86a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c86a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c86a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c86a-120">-InputObject</span></span>
<span data-ttu-id="7c86a-121">Obiekt reprezentujący klasyfikację wrażliwości puli języka SQL.</span><span class="sxs-lookup"><span data-stu-id="7c86a-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c86a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c86a-122">-PassThru</span></span>
<span data-ttu-id="7c86a-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="7c86a-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7c86a-124">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="7c86a-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7c86a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c86a-125">-ResourceGroupName</span></span>
<span data-ttu-id="7c86a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7c86a-126">Resource group name.</span></span>

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

### <span data-ttu-id="7c86a-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7c86a-127">-SchemaName</span></span>
<span data-ttu-id="7c86a-128">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="7c86a-128">Name of schema.</span></span>

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

### <span data-ttu-id="7c86a-129">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="7c86a-129">-SqlPoolName</span></span>
<span data-ttu-id="7c86a-130">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="7c86a-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="7c86a-131">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="7c86a-131">-SqlPoolObject</span></span>
<span data-ttu-id="7c86a-132">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="7c86a-132">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7c86a-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="7c86a-133">-TableName</span></span>
<span data-ttu-id="7c86a-134">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="7c86a-134">Name of table.</span></span>

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

### <span data-ttu-id="7c86a-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7c86a-135">-WorkspaceName</span></span>
<span data-ttu-id="7c86a-136">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="7c86a-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7c86a-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c86a-137">-Confirm</span></span>
<span data-ttu-id="7c86a-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7c86a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c86a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c86a-139">-WhatIf</span></span>
<span data-ttu-id="7c86a-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c86a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c86a-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7c86a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c86a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c86a-142">CommonParameters</span></span>
<span data-ttu-id="7c86a-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c86a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c86a-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c86a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c86a-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c86a-145">INPUTS</span></span>

### <span data-ttu-id="7c86a-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7c86a-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="7c86a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7c86a-147">System.String</span></span>

### <span data-ttu-id="7c86a-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7c86a-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7c86a-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c86a-149">OUTPUTS</span></span>

### <span data-ttu-id="7c86a-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c86a-150">System.Boolean</span></span>

## <span data-ttu-id="7c86a-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7c86a-151">NOTES</span></span>

## <span data-ttu-id="7c86a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c86a-152">RELATED LINKS</span></span>
