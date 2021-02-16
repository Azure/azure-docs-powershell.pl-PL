---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 21d7169f18a999f84adbc568da18c90cb2aa2424
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182707"
---
# <span data-ttu-id="f35bd-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f35bd-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="f35bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f35bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f35bd-103">Usuwa administratora usługi Azure AD dla obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="f35bd-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="f35bd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f35bd-104">SYNTAX</span></span>

### <span data-ttu-id="f35bd-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f35bd-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f35bd-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f35bd-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f35bd-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f35bd-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f35bd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f35bd-108">DESCRIPTION</span></span>
<span data-ttu-id="f35bd-109">Polecenie cmdlet **Remove-AzSynapseSqlActiveDirectoryAdministrator** usuwa administratora usługi Azure Active Directory (Azure AD) dla obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="f35bd-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="f35bd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f35bd-110">EXAMPLES</span></span>

### <span data-ttu-id="f35bd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f35bd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f35bd-112">To polecenie usuwa administratora usługi Azure AD dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f35bd-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f35bd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f35bd-113">PARAMETERS</span></span>

### <span data-ttu-id="f35bd-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f35bd-114">-AsJob</span></span>
<span data-ttu-id="f35bd-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f35bd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f35bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f35bd-116">-DefaultProfile</span></span>
<span data-ttu-id="f35bd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f35bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f35bd-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f35bd-118">-Force</span></span>
<span data-ttu-id="f35bd-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f35bd-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f35bd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f35bd-120">-InputObject</span></span>
<span data-ttu-id="f35bd-121">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="f35bd-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f35bd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f35bd-122">-PassThru</span></span>
<span data-ttu-id="f35bd-123">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="f35bd-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f35bd-124">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="f35bd-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f35bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f35bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="f35bd-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f35bd-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f35bd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f35bd-127">-ResourceId</span></span>
<span data-ttu-id="f35bd-128">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="f35bd-128">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f35bd-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f35bd-129">-WorkspaceName</span></span>
<span data-ttu-id="f35bd-130">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="f35bd-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f35bd-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f35bd-131">-Confirm</span></span>
<span data-ttu-id="f35bd-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f35bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f35bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f35bd-133">-WhatIf</span></span>
<span data-ttu-id="f35bd-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f35bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f35bd-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f35bd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f35bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f35bd-136">CommonParameters</span></span>
<span data-ttu-id="f35bd-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f35bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f35bd-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f35bd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f35bd-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f35bd-139">INPUTS</span></span>

### <span data-ttu-id="f35bd-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f35bd-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f35bd-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f35bd-141">OUTPUTS</span></span>

### <span data-ttu-id="f35bd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f35bd-142">System.Boolean</span></span>

## <span data-ttu-id="f35bd-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f35bd-143">NOTES</span></span>

## <span data-ttu-id="f35bd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f35bd-144">RELATED LINKS</span></span>
