---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220184"
---
# <span data-ttu-id="cdbae-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cdbae-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="cdbae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdbae-102">SYNOPSIS</span></span>
<span data-ttu-id="cdbae-103">Pobiera obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="cdbae-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="cdbae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdbae-104">SYNTAX</span></span>

### <span data-ttu-id="cdbae-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cdbae-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdbae-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdbae-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdbae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cdbae-107">DESCRIPTION</span></span>
<span data-ttu-id="cdbae-108">Polecenie cmdlet **Get-AzSynapseWorkspace** pobiera informacje o obszarze roboczym analizy Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="cdbae-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="cdbae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdbae-109">EXAMPLES</span></span>

### <span data-ttu-id="cdbae-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cdbae-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="cdbae-111">To polecenie pobiera wszystkie obszary robocze funkcji Azure Synapse Analytics w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="cdbae-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="cdbae-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cdbae-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="cdbae-113">To polecenie pobiera wszystkie obszary robocze funkcji Azure Synapse Analytics w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="cdbae-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="cdbae-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cdbae-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="cdbae-115">To polecenie pobiera obszar roboczy funkcji Azure Synapse Analytics o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="cdbae-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="cdbae-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="cdbae-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="cdbae-117">To polecenie pobiera obszar roboczy funkcji Azure Synapse Analytics o określonym IDENTYFIKATORze zasobu.</span><span class="sxs-lookup"><span data-stu-id="cdbae-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="cdbae-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdbae-118">PARAMETERS</span></span>

### <span data-ttu-id="cdbae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdbae-119">-DefaultProfile</span></span>
<span data-ttu-id="cdbae-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdbae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdbae-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cdbae-121">-Name</span></span>
<span data-ttu-id="cdbae-122">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="cdbae-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cdbae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdbae-123">-ResourceGroupName</span></span>
<span data-ttu-id="cdbae-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cdbae-124">Resource group name.</span></span>

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

### <span data-ttu-id="cdbae-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdbae-125">-ResourceId</span></span>
<span data-ttu-id="cdbae-126">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="cdbae-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="cdbae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdbae-127">CommonParameters</span></span>
<span data-ttu-id="cdbae-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdbae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdbae-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdbae-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdbae-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdbae-130">INPUTS</span></span>

### <span data-ttu-id="cdbae-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="cdbae-131">None</span></span>

## <span data-ttu-id="cdbae-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdbae-132">OUTPUTS</span></span>

### <span data-ttu-id="cdbae-133">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cdbae-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cdbae-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdbae-134">NOTES</span></span>

## <span data-ttu-id="cdbae-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdbae-135">RELATED LINKS</span></span>
