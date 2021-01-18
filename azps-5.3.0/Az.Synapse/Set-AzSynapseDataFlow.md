---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501303"
---
# <span data-ttu-id="7762c-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="7762c-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="7762c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7762c-102">SYNOPSIS</span></span>
<span data-ttu-id="7762c-103">Tworzenie lub aktualizowanie przepływu danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="7762c-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="7762c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7762c-104">SYNTAX</span></span>

### <span data-ttu-id="7762c-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7762c-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7762c-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="7762c-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7762c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7762c-107">DESCRIPTION</span></span>
<span data-ttu-id="7762c-108">Polecenie cmdlet **Set-AzSynapseDataFlow** umożliwia utworzenie przepływu danych lub zaktualizowanie istniejącego przepływu danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="7762c-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="7762c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7762c-109">EXAMPLES</span></span>

### <span data-ttu-id="7762c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7762c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="7762c-111">To polecenie tworzy przepływ danych o nazwie ContosoDataFlow w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7762c-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="7762c-112">Polecenie opiera się na przeniesieniu przepływu danych na informacjach w DataFlow.jspliku.</span><span class="sxs-lookup"><span data-stu-id="7762c-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="7762c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7762c-113">PARAMETERS</span></span>

### <span data-ttu-id="7762c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7762c-114">-AsJob</span></span>
<span data-ttu-id="7762c-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7762c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7762c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7762c-116">-DefaultProfile</span></span>
<span data-ttu-id="7762c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7762c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7762c-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7762c-118">-DefinitionFile</span></span>
<span data-ttu-id="7762c-119">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="7762c-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7762c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7762c-120">-Name</span></span>
<span data-ttu-id="7762c-121">Nazwa przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="7762c-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7762c-122">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="7762c-122">-WorkspaceName</span></span>
<span data-ttu-id="7762c-123">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="7762c-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7762c-124">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="7762c-124">-WorkspaceObject</span></span>
<span data-ttu-id="7762c-125">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="7762c-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7762c-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7762c-126">-Confirm</span></span>
<span data-ttu-id="7762c-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7762c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7762c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7762c-128">-WhatIf</span></span>
<span data-ttu-id="7762c-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7762c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7762c-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7762c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7762c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7762c-131">CommonParameters</span></span>
<span data-ttu-id="7762c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7762c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7762c-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7762c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7762c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7762c-134">INPUTS</span></span>

### <span data-ttu-id="7762c-135">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7762c-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7762c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7762c-136">OUTPUTS</span></span>

### <span data-ttu-id="7762c-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="7762c-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="7762c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7762c-138">NOTES</span></span>

## <span data-ttu-id="7762c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7762c-139">RELATED LINKS</span></span>
