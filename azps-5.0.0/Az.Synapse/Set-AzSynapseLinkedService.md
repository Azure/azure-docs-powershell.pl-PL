---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225126"
---
# <span data-ttu-id="9e105-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="9e105-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="9e105-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e105-102">SYNOPSIS</span></span>
<span data-ttu-id="9e105-103">Łączy magazyn danych lub usługę w chmurze z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="9e105-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="9e105-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e105-104">SYNTAX</span></span>

### <span data-ttu-id="9e105-105">SetByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9e105-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e105-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="9e105-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e105-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9e105-107">DESCRIPTION</span></span>
<span data-ttu-id="9e105-108">Polecenie cmdlet **Set-AzSynapseLinkedService** łączy magazyn danych lub usługę w chmurze z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="9e105-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="9e105-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e105-109">EXAMPLES</span></span>

### <span data-ttu-id="9e105-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9e105-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="9e105-111">To polecenie tworzy połączoną usługę o nazwie ContosoLinkedService w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9e105-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9e105-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9e105-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="9e105-113">To polecenie tworzy połączoną usługę o nazwie ContosoLinkedService w obszarze roboczym o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="9e105-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9e105-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e105-114">PARAMETERS</span></span>

### <span data-ttu-id="9e105-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e105-115">-AsJob</span></span>
<span data-ttu-id="9e105-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9e105-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e105-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e105-117">-DefaultProfile</span></span>
<span data-ttu-id="9e105-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e105-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e105-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9e105-119">-DefinitionFile</span></span>
<span data-ttu-id="9e105-120">Ścieżka pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="9e105-120">The JSON file path.</span></span>

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

### <span data-ttu-id="9e105-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9e105-121">-Name</span></span>
<span data-ttu-id="9e105-122">Nazwa połączonej usługi.</span><span class="sxs-lookup"><span data-stu-id="9e105-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e105-123">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="9e105-123">-WorkspaceName</span></span>
<span data-ttu-id="9e105-124">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="9e105-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e105-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="9e105-125">-WorkspaceObject</span></span>
<span data-ttu-id="9e105-126">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="9e105-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e105-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e105-127">-Confirm</span></span>
<span data-ttu-id="9e105-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e105-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e105-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e105-129">-WhatIf</span></span>
<span data-ttu-id="9e105-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e105-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e105-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e105-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e105-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e105-132">CommonParameters</span></span>
<span data-ttu-id="9e105-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e105-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e105-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e105-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e105-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e105-135">INPUTS</span></span>

### <span data-ttu-id="9e105-136">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e105-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9e105-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e105-137">OUTPUTS</span></span>

### <span data-ttu-id="9e105-138">Microsoft. Azure. Commands. Synapse. models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="9e105-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="9e105-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e105-139">NOTES</span></span>

## <span data-ttu-id="9e105-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e105-140">RELATED LINKS</span></span>
