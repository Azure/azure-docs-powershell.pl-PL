---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225563"
---
# <span data-ttu-id="83738-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="83738-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="83738-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83738-102">SYNOPSIS</span></span>
<span data-ttu-id="83738-103">Umożliwia zaktualizowanie obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="83738-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="83738-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83738-104">SYNTAX</span></span>

### <span data-ttu-id="83738-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="83738-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83738-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83738-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83738-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83738-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83738-108">Opis</span><span class="sxs-lookup"><span data-stu-id="83738-108">DESCRIPTION</span></span>
<span data-ttu-id="83738-109">Polecenie cmdlet **Update-AzSynapseWorkspace** aktualizuje obszar roboczy funkcji Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="83738-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="83738-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83738-110">EXAMPLES</span></span>

### <span data-ttu-id="83738-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83738-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="83738-112">To polecenie aktualizuje znaczniki w obszarze roboczym analizy specififed Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="83738-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="83738-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="83738-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="83738-114">To polecenie aktualizuje znaczniki w obszarze roboczym specififed Azure Synapse Analytics za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="83738-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="83738-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="83738-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="83738-116">To polecenie aktualizuje znaczniki w obszarze roboczym analizy usługi specififed Azure Synapse za pomocą identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="83738-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="83738-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83738-117">PARAMETERS</span></span>

### <span data-ttu-id="83738-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83738-118">-AsJob</span></span>
<span data-ttu-id="83738-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="83738-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83738-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83738-120">-DefaultProfile</span></span>
<span data-ttu-id="83738-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83738-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83738-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83738-122">-InputObject</span></span>
<span data-ttu-id="83738-123">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="83738-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83738-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="83738-124">-Name</span></span>
<span data-ttu-id="83738-125">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="83738-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83738-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83738-126">-ResourceGroupName</span></span>
<span data-ttu-id="83738-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83738-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83738-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83738-128">-ResourceId</span></span>
<span data-ttu-id="83738-129">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="83738-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83738-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="83738-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="83738-131">Nowe hasło administratora SQL dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="83738-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83738-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="83738-132">-Tag</span></span>
<span data-ttu-id="83738-133">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="83738-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="83738-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83738-134">-Confirm</span></span>
<span data-ttu-id="83738-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83738-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83738-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83738-136">-WhatIf</span></span>
<span data-ttu-id="83738-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83738-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83738-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83738-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83738-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83738-139">CommonParameters</span></span>
<span data-ttu-id="83738-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83738-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83738-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83738-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83738-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83738-142">INPUTS</span></span>

### <span data-ttu-id="83738-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="83738-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="83738-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83738-144">OUTPUTS</span></span>

### <span data-ttu-id="83738-145">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="83738-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="83738-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83738-146">NOTES</span></span>

## <span data-ttu-id="83738-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83738-147">RELATED LINKS</span></span>
