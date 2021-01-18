---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498197"
---
# <span data-ttu-id="f661a-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f661a-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="f661a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f661a-102">SYNOPSIS</span></span>
<span data-ttu-id="f661a-103">Aktualizuje bazę danych SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f661a-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f661a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f661a-104">SYNTAX</span></span>

### <span data-ttu-id="f661a-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f661a-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f661a-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f661a-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f661a-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f661a-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f661a-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f661a-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f661a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f661a-109">DESCRIPTION</span></span>
<span data-ttu-id="f661a-110">Polecenie cmdlet **Update-AzSynapseSqlDatabase** aktualizuje bazę danych SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f661a-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f661a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f661a-111">EXAMPLES</span></span>

### <span data-ttu-id="f661a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f661a-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="f661a-113">To polecenie aktualizuje bazę danych SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f661a-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f661a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f661a-114">PARAMETERS</span></span>

### <span data-ttu-id="f661a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f661a-115">-AsJob</span></span>
<span data-ttu-id="f661a-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f661a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f661a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f661a-117">-DefaultProfile</span></span>
<span data-ttu-id="f661a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f661a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f661a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f661a-119">-InputObject</span></span>
<span data-ttu-id="f661a-120">Obiekt wejściowy SQL Database, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f661a-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f661a-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="f661a-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="f661a-122">Określa maksymalny rozmiar bazy danych w bajtach.</span><span class="sxs-lookup"><span data-stu-id="f661a-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f661a-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f661a-123">-Name</span></span>
<span data-ttu-id="f661a-124">Nazwa bazy danych SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f661a-124">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f661a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f661a-125">-PassThru</span></span>
<span data-ttu-id="f661a-126">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="f661a-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f661a-127">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="f661a-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f661a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f661a-128">-ResourceGroupName</span></span>
<span data-ttu-id="f661a-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f661a-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f661a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f661a-130">-ResourceId</span></span>
<span data-ttu-id="f661a-131">Identyfikator zasobu bazy danych SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f661a-131">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f661a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="f661a-132">-Tag</span></span>
<span data-ttu-id="f661a-133">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="f661a-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f661a-134">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f661a-134">-WorkspaceName</span></span>
<span data-ttu-id="f661a-135">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f661a-135">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f661a-136">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f661a-136">-WorkspaceObject</span></span>
<span data-ttu-id="f661a-137">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f661a-137">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f661a-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f661a-138">-Confirm</span></span>
<span data-ttu-id="f661a-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f661a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f661a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f661a-140">-WhatIf</span></span>
<span data-ttu-id="f661a-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f661a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f661a-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f661a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f661a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f661a-143">CommonParameters</span></span>
<span data-ttu-id="f661a-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f661a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f661a-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f661a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f661a-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f661a-146">INPUTS</span></span>

### <span data-ttu-id="f661a-147">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f661a-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f661a-148">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f661a-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="f661a-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f661a-149">OUTPUTS</span></span>

### <span data-ttu-id="f661a-150">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f661a-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="f661a-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f661a-151">NOTES</span></span>

## <span data-ttu-id="f661a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f661a-152">RELATED LINKS</span></span>
