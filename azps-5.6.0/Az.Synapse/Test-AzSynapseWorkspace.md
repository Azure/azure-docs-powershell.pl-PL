---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: e92b4d20e89df451c483bc0b4bdccb83fdc8a140
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011201"
---
# <span data-ttu-id="14d82-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="14d82-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="14d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14d82-102">SYNOPSIS</span></span>
<span data-ttu-id="14d82-103">Sprawdza, czy istnieje obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="14d82-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="14d82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="14d82-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14d82-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="14d82-105">DESCRIPTION</span></span>
<span data-ttu-id="14d82-106">Polecenie **cmdlet Test-AzSynapseWorkspace** sprawdza, czy istnieje obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="14d82-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="14d82-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="14d82-107">EXAMPLES</span></span>

### <span data-ttu-id="14d82-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14d82-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="14d82-109">To polecenie sprawdza istnienie obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="14d82-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="14d82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14d82-110">PARAMETERS</span></span>

### <span data-ttu-id="14d82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d82-111">-DefaultProfile</span></span>
<span data-ttu-id="14d82-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="14d82-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14d82-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="14d82-113">-Name</span></span>
<span data-ttu-id="14d82-114">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="14d82-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="14d82-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d82-115">-ResourceGroupName</span></span>
<span data-ttu-id="14d82-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14d82-116">Resource group name.</span></span>

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

### <span data-ttu-id="14d82-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d82-117">CommonParameters</span></span>
<span data-ttu-id="14d82-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d82-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d82-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14d82-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d82-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14d82-120">INPUTS</span></span>

### <span data-ttu-id="14d82-121">Brak</span><span class="sxs-lookup"><span data-stu-id="14d82-121">None</span></span>

## <span data-ttu-id="14d82-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14d82-122">OUTPUTS</span></span>

### <span data-ttu-id="14d82-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="14d82-123">System.Object</span></span>
## <span data-ttu-id="14d82-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="14d82-124">NOTES</span></span>

## <span data-ttu-id="14d82-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14d82-125">RELATED LINKS</span></span>
