---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 52abddf2db18a6e70a1b876629feff0761bed014
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197402"
---
# <span data-ttu-id="3fd3d-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="3fd3d-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="3fd3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd3d-103">Umożliwia wyświetlanie rekomendacji wrażliwości dotyczących kolumn (zalecenia są domyślnie włączone we wszystkich kolumnach) w puli SQL.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="3fd3d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3fd3d-104">SYNTAX</span></span>

### <span data-ttu-id="3fd3d-105">InputObjectParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3fd3d-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fd3d-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fd3d-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fd3d-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fd3d-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fd3d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3fd3d-108">DESCRIPTION</span></span>
<span data-ttu-id="3fd3d-109">Polecenie Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet umożliwia wyświetlanie rekomendacji wrażliwości dotyczących kolumn w puli sql.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="3fd3d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3fd3d-110">EXAMPLES</span></span>

### <span data-ttu-id="3fd3d-111">Przykład 1. Włączanie rekomendacji wrażliwości dla danej kolumny w puli SQL Synapse Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="3fd3d-112">Przykład 2. Włączanie rekomendacji wrażliwości dla danej kolumny Pula SQL Azure Synapse przy użyciu połączenia pipingowego.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="3fd3d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fd3d-113">PARAMETERS</span></span>

### <span data-ttu-id="3fd3d-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3fd3d-114">-AsJob</span></span>
<span data-ttu-id="3fd3d-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3fd3d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fd3d-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="3fd3d-116">-ColumnName</span></span>
<span data-ttu-id="3fd3d-117">Nazwa kolumny.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-117">Name of column.</span></span>

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

### <span data-ttu-id="3fd3d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd3d-118">-DefaultProfile</span></span>
<span data-ttu-id="3fd3d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fd3d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fd3d-120">-InputObject</span></span>
<span data-ttu-id="3fd3d-121">Obiekt reprezentujący klasyfikację wrażliwości puli języka SQL.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="3fd3d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fd3d-122">-PassThru</span></span>
<span data-ttu-id="3fd3d-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3fd3d-124">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3fd3d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd3d-125">-ResourceGroupName</span></span>
<span data-ttu-id="3fd3d-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-126">Resource group name.</span></span>

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

### <span data-ttu-id="3fd3d-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3fd3d-127">-SchemaName</span></span>
<span data-ttu-id="3fd3d-128">Nazwa schematu.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-128">Name of schema.</span></span>

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

### <span data-ttu-id="3fd3d-129">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="3fd3d-129">-SqlPoolName</span></span>
<span data-ttu-id="3fd3d-130">Nazwa puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="3fd3d-131">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="3fd3d-131">-SqlPoolObject</span></span>
<span data-ttu-id="3fd3d-132">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-132">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3fd3d-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="3fd3d-133">-TableName</span></span>
<span data-ttu-id="3fd3d-134">Nazwa tabeli.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-134">Name of table.</span></span>

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

### <span data-ttu-id="3fd3d-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3fd3d-135">-WorkspaceName</span></span>
<span data-ttu-id="3fd3d-136">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3fd3d-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3fd3d-137">-Confirm</span></span>
<span data-ttu-id="3fd3d-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fd3d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd3d-139">-WhatIf</span></span>
<span data-ttu-id="3fd3d-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fd3d-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fd3d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd3d-142">CommonParameters</span></span>
<span data-ttu-id="3fd3d-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd3d-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fd3d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd3d-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fd3d-145">INPUTS</span></span>

### <span data-ttu-id="3fd3d-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="3fd3d-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="3fd3d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3fd3d-147">System.String</span></span>

### <span data-ttu-id="3fd3d-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="3fd3d-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="3fd3d-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3fd3d-149">OUTPUTS</span></span>

### <span data-ttu-id="3fd3d-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3fd3d-150">System.Boolean</span></span>

## <span data-ttu-id="3fd3d-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3fd3d-151">NOTES</span></span>

## <span data-ttu-id="3fd3d-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fd3d-152">RELATED LINKS</span></span>
