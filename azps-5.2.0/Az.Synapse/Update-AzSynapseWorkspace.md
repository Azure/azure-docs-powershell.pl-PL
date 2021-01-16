---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363279"
---
# <span data-ttu-id="deb8f-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="deb8f-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="deb8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="deb8f-102">SYNOPSIS</span></span>
<span data-ttu-id="deb8f-103">Umożliwia zaktualizowanie obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="deb8f-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="deb8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="deb8f-104">SYNTAX</span></span>

### <span data-ttu-id="deb8f-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="deb8f-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deb8f-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="deb8f-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deb8f-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="deb8f-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deb8f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="deb8f-108">DESCRIPTION</span></span>
<span data-ttu-id="deb8f-109">Polecenie cmdlet **Update-AzSynapseWorkspace** aktualizuje obszar roboczy funkcji Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="deb8f-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="deb8f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="deb8f-110">EXAMPLES</span></span>

### <span data-ttu-id="deb8f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="deb8f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="deb8f-112">To polecenie aktualizuje znaczniki w obszarze roboczym analizy specififed Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="deb8f-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="deb8f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="deb8f-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="deb8f-114">To polecenie aktualizuje znaczniki w obszarze roboczym specififed Azure Synapse Analytics za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="deb8f-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="deb8f-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="deb8f-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="deb8f-116">To polecenie aktualizuje znaczniki w obszarze roboczym analizy usługi specififed Azure Synapse za pomocą identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="deb8f-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="deb8f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="deb8f-117">PARAMETERS</span></span>

### <span data-ttu-id="deb8f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="deb8f-118">-AsJob</span></span>
<span data-ttu-id="deb8f-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="deb8f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="deb8f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deb8f-120">-DefaultProfile</span></span>
<span data-ttu-id="deb8f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="deb8f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="deb8f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="deb8f-122">-InputObject</span></span>
<span data-ttu-id="deb8f-123">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="deb8f-123">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="deb8f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="deb8f-124">-Name</span></span>
<span data-ttu-id="deb8f-125">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="deb8f-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="deb8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="deb8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="deb8f-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="deb8f-127">Resource group name.</span></span>

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

### <span data-ttu-id="deb8f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="deb8f-128">-ResourceId</span></span>
<span data-ttu-id="deb8f-129">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="deb8f-129">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="deb8f-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="deb8f-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="deb8f-131">Nowe hasło administratora SQL dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="deb8f-131">The new SQL administrator password for the workspace.</span></span>

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

### <span data-ttu-id="deb8f-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="deb8f-132">-Tag</span></span>
<span data-ttu-id="deb8f-133">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="deb8f-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="deb8f-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="deb8f-134">-Confirm</span></span>
<span data-ttu-id="deb8f-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deb8f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deb8f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deb8f-136">-WhatIf</span></span>
<span data-ttu-id="deb8f-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deb8f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deb8f-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="deb8f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deb8f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deb8f-139">CommonParameters</span></span>
<span data-ttu-id="deb8f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deb8f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deb8f-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="deb8f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deb8f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="deb8f-142">INPUTS</span></span>

### <span data-ttu-id="deb8f-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="deb8f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="deb8f-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="deb8f-144">OUTPUTS</span></span>

### <span data-ttu-id="deb8f-145">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="deb8f-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="deb8f-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="deb8f-146">NOTES</span></span>

## <span data-ttu-id="deb8f-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="deb8f-147">RELATED LINKS</span></span>
