---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 73664b619670f17a92bd915f6e4d8501a8ac9f6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976058"
---
# <span data-ttu-id="40380-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="40380-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="40380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40380-102">SYNOPSIS</span></span>
<span data-ttu-id="40380-103">Tworzy bazę danych SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="40380-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="40380-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="40380-104">SYNTAX</span></span>

### <span data-ttu-id="40380-105">CreateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="40380-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40380-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40380-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40380-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="40380-107">DESCRIPTION</span></span>
<span data-ttu-id="40380-108">Polecenie **cmdlet Get-AzSynapseSqlDatabase** pobiera informacje o bazie danych SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="40380-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="40380-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="40380-109">EXAMPLES</span></span>

### <span data-ttu-id="40380-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="40380-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="40380-111">To polecenie tworzy bazę danych Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="40380-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="40380-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40380-112">PARAMETERS</span></span>

### <span data-ttu-id="40380-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="40380-113">-AsJob</span></span>
<span data-ttu-id="40380-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="40380-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40380-115">— sortowanie</span><span class="sxs-lookup"><span data-stu-id="40380-115">-Collation</span></span>
<span data-ttu-id="40380-116">Sortowanie definiuje reguły sortowania i porównywania danych, których nie można zmienić po utworzeniu puli języka SQL.</span><span class="sxs-lookup"><span data-stu-id="40380-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="40380-117">Sortowaniem domyślnym jest SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="40380-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40380-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40380-118">-DefaultProfile</span></span>
<span data-ttu-id="40380-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="40380-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40380-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="40380-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="40380-121">Określa maksymalny rozmiar bazy danych (w bajtach).</span><span class="sxs-lookup"><span data-stu-id="40380-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40380-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="40380-122">-Name</span></span>
<span data-ttu-id="40380-123">Nazwa bazy danych Synapse SQL Database.</span><span class="sxs-lookup"><span data-stu-id="40380-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40380-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40380-124">-ResourceGroupName</span></span>
<span data-ttu-id="40380-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="40380-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40380-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="40380-126">-Tag</span></span>
<span data-ttu-id="40380-127">A string,string dictionary of tags associated with the resource.</span><span class="sxs-lookup"><span data-stu-id="40380-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="40380-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="40380-128">-WorkspaceName</span></span>
<span data-ttu-id="40380-129">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="40380-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40380-130">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="40380-130">-WorkspaceObject</span></span>
<span data-ttu-id="40380-131">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="40380-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40380-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40380-132">-Confirm</span></span>
<span data-ttu-id="40380-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="40380-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40380-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40380-134">-WhatIf</span></span>
<span data-ttu-id="40380-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40380-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40380-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="40380-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40380-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40380-137">CommonParameters</span></span>
<span data-ttu-id="40380-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40380-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40380-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40380-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40380-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40380-140">INPUTS</span></span>

### <span data-ttu-id="40380-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="40380-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="40380-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40380-142">OUTPUTS</span></span>

### <span data-ttu-id="40380-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="40380-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="40380-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="40380-144">NOTES</span></span>

## <span data-ttu-id="40380-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40380-145">RELATED LINKS</span></span>
