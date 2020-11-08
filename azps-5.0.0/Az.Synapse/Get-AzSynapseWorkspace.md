---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232386"
---
# <span data-ttu-id="905f6-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="905f6-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="905f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="905f6-102">SYNOPSIS</span></span>
<span data-ttu-id="905f6-103">Pobiera obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="905f6-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="905f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="905f6-104">SYNTAX</span></span>

### <span data-ttu-id="905f6-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="905f6-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="905f6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="905f6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="905f6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="905f6-107">DESCRIPTION</span></span>
<span data-ttu-id="905f6-108">Polecenie cmdlet **Get-AzSynapseWorkspace** pobiera informacje o obszarze roboczym analizy Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="905f6-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="905f6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="905f6-109">EXAMPLES</span></span>

### <span data-ttu-id="905f6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="905f6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="905f6-111">To polecenie pobiera wszystkie obszary robocze funkcji Azure Synapse Analytics w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="905f6-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="905f6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="905f6-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="905f6-113">To polecenie pobiera wszystkie obszary robocze funkcji Azure Synapse Analytics w ramach bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="905f6-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="905f6-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="905f6-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="905f6-115">To polecenie pobiera obszar roboczy funkcji Azure Synapse Analytics o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="905f6-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="905f6-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="905f6-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="905f6-117">To polecenie pobiera obszar roboczy funkcji Azure Synapse Analytics o określonym IDENTYFIKATORze zasobu.</span><span class="sxs-lookup"><span data-stu-id="905f6-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="905f6-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="905f6-118">PARAMETERS</span></span>

### <span data-ttu-id="905f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905f6-119">-DefaultProfile</span></span>
<span data-ttu-id="905f6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="905f6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="905f6-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="905f6-121">-Name</span></span>
<span data-ttu-id="905f6-122">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="905f6-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="905f6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="905f6-123">-ResourceGroupName</span></span>
<span data-ttu-id="905f6-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="905f6-124">Resource group name.</span></span>

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

### <span data-ttu-id="905f6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="905f6-125">-ResourceId</span></span>
<span data-ttu-id="905f6-126">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="905f6-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="905f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905f6-127">CommonParameters</span></span>
<span data-ttu-id="905f6-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905f6-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="905f6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905f6-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="905f6-130">INPUTS</span></span>

### <span data-ttu-id="905f6-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="905f6-131">None</span></span>

## <span data-ttu-id="905f6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="905f6-132">OUTPUTS</span></span>

### <span data-ttu-id="905f6-133">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="905f6-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="905f6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="905f6-134">NOTES</span></span>

## <span data-ttu-id="905f6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="905f6-135">RELATED LINKS</span></span>
