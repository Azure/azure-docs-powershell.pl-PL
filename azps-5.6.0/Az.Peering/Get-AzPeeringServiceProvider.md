---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: cfc25f735d2785a688f29fd3eb3064337b5c6e8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989465"
---
# <span data-ttu-id="de63e-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="de63e-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="de63e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de63e-102">SYNOPSIS</span></span>
<span data-ttu-id="de63e-103">Pobiera listę dostawców usług komunikacji równorzędnej współpracuje z firmą Microsoft.</span><span class="sxs-lookup"><span data-stu-id="de63e-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="de63e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de63e-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de63e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="de63e-105">DESCRIPTION</span></span>
<span data-ttu-id="de63e-106">Lista dostawców usług komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="de63e-106">List peering service providers</span></span>

## <span data-ttu-id="de63e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de63e-107">EXAMPLES</span></span>

### <span data-ttu-id="de63e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de63e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="de63e-109">Pobiera dostępnych dostawców usług komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="de63e-109">Gets available peering service providers</span></span>

## <span data-ttu-id="de63e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de63e-110">PARAMETERS</span></span>

### <span data-ttu-id="de63e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de63e-111">-DefaultProfile</span></span>
<span data-ttu-id="de63e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de63e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de63e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de63e-113">CommonParameters</span></span>
<span data-ttu-id="de63e-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de63e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de63e-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de63e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de63e-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de63e-116">INPUTS</span></span>

### <span data-ttu-id="de63e-117">Brak</span><span class="sxs-lookup"><span data-stu-id="de63e-117">None</span></span>

## <span data-ttu-id="de63e-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de63e-118">OUTPUTS</span></span>

### <span data-ttu-id="de63e-119">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="de63e-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="de63e-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de63e-120">NOTES</span></span>

## <span data-ttu-id="de63e-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de63e-121">RELATED LINKS</span></span>
