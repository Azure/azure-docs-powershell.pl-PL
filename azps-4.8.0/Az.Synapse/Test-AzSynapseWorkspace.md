---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222422"
---
# <span data-ttu-id="77f85-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="77f85-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="77f85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77f85-102">SYNOPSIS</span></span>
<span data-ttu-id="77f85-103">Sprawdza, czy istnieje obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="77f85-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="77f85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77f85-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77f85-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77f85-105">DESCRIPTION</span></span>
<span data-ttu-id="77f85-106">Polecenie cmdlet **test-AzSynapseWorkspace** sprawdza obecność obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="77f85-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="77f85-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77f85-107">EXAMPLES</span></span>

### <span data-ttu-id="77f85-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77f85-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="77f85-109">To polecenie sprawdza, czy istnieje obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="77f85-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="77f85-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77f85-110">PARAMETERS</span></span>

### <span data-ttu-id="77f85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f85-111">-DefaultProfile</span></span>
<span data-ttu-id="77f85-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77f85-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77f85-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77f85-113">-Name</span></span>
<span data-ttu-id="77f85-114">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="77f85-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="77f85-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f85-115">-ResourceGroupName</span></span>
<span data-ttu-id="77f85-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="77f85-116">Resource group name.</span></span>

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

### <span data-ttu-id="77f85-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f85-117">CommonParameters</span></span>
<span data-ttu-id="77f85-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f85-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f85-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77f85-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f85-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77f85-120">INPUTS</span></span>

### <span data-ttu-id="77f85-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="77f85-121">None</span></span>

## <span data-ttu-id="77f85-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77f85-122">OUTPUTS</span></span>

### <span data-ttu-id="77f85-123">System. Object</span><span class="sxs-lookup"><span data-stu-id="77f85-123">System.Object</span></span>
## <span data-ttu-id="77f85-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77f85-124">NOTES</span></span>

## <span data-ttu-id="77f85-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77f85-125">RELATED LINKS</span></span>
