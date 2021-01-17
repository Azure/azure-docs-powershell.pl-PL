---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383700"
---
# <span data-ttu-id="27a4c-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="27a4c-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="27a4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="27a4c-103">Pobiera obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="27a4c-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="27a4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27a4c-104">SYNTAX</span></span>

### <span data-ttu-id="27a4c-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="27a4c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27a4c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27a4c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27a4c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="27a4c-107">DESCRIPTION</span></span>
<span data-ttu-id="27a4c-108">Polecenie cmdlet **Get-AzSynapseWorkspace** pobiera informacje o obszarze roboczym analizy Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="27a4c-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="27a4c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27a4c-109">EXAMPLES</span></span>

### <span data-ttu-id="27a4c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="27a4c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="27a4c-111">To polecenie pobiera wszystkie obszary robocze funkcji Azure Synapse Analytics w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="27a4c-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="27a4c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="27a4c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="27a4c-113">To polecenie pobiera wszystkie obszary robocze funkcji Azure Synapse Analytics w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="27a4c-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="27a4c-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="27a4c-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="27a4c-115">To polecenie pobiera obszar roboczy funkcji Azure Synapse Analytics o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="27a4c-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="27a4c-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="27a4c-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="27a4c-117">To polecenie pobiera obszar roboczy funkcji Azure Synapse Analytics o określonym IDENTYFIKATORze zasobu.</span><span class="sxs-lookup"><span data-stu-id="27a4c-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="27a4c-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27a4c-118">PARAMETERS</span></span>

### <span data-ttu-id="27a4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a4c-119">-DefaultProfile</span></span>
<span data-ttu-id="27a4c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="27a4c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27a4c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="27a4c-121">-Name</span></span>
<span data-ttu-id="27a4c-122">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="27a4c-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a4c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a4c-123">-ResourceGroupName</span></span>
<span data-ttu-id="27a4c-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="27a4c-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a4c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27a4c-125">-ResourceId</span></span>
<span data-ttu-id="27a4c-126">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="27a4c-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a4c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a4c-127">CommonParameters</span></span>
<span data-ttu-id="27a4c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27a4c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a4c-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27a4c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a4c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27a4c-130">INPUTS</span></span>

### <span data-ttu-id="27a4c-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="27a4c-131">None</span></span>

## <span data-ttu-id="27a4c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27a4c-132">OUTPUTS</span></span>

### <span data-ttu-id="27a4c-133">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="27a4c-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="27a4c-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27a4c-134">NOTES</span></span>

## <span data-ttu-id="27a4c-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27a4c-135">RELATED LINKS</span></span>
