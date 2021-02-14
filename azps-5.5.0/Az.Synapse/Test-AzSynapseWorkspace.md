---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241651"
---
# <span data-ttu-id="e5fe4-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e5fe4-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="e5fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fe4-103">Sprawdza, czy istnieje obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="e5fe4-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e5fe4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e5fe4-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5fe4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e5fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="e5fe4-106">Polecenie **cmdlet Test-AzSynapseWorkspace** sprawdza, czy istnieje obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="e5fe4-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e5fe4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e5fe4-107">EXAMPLES</span></span>

### <span data-ttu-id="e5fe4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5fe4-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="e5fe4-109">To polecenie sprawdza istnienie obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="e5fe4-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e5fe4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5fe4-110">PARAMETERS</span></span>

### <span data-ttu-id="e5fe4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fe4-111">-DefaultProfile</span></span>
<span data-ttu-id="e5fe4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5fe4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5fe4-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e5fe4-113">-Name</span></span>
<span data-ttu-id="e5fe4-114">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="e5fe4-114">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5fe4-115">-ResourceGroupName</span></span>
<span data-ttu-id="e5fe4-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e5fe4-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fe4-117">CommonParameters</span></span>
<span data-ttu-id="e5fe4-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fe4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fe4-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5fe4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fe4-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5fe4-120">INPUTS</span></span>

### <span data-ttu-id="e5fe4-121">Brak</span><span class="sxs-lookup"><span data-stu-id="e5fe4-121">None</span></span>

## <span data-ttu-id="e5fe4-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5fe4-122">OUTPUTS</span></span>

### <span data-ttu-id="e5fe4-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="e5fe4-123">System.Object</span></span>
## <span data-ttu-id="e5fe4-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e5fe4-124">NOTES</span></span>

## <span data-ttu-id="e5fe4-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5fe4-125">RELATED LINKS</span></span>
