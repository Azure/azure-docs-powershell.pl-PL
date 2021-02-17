---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202282"
---
# <span data-ttu-id="0ba3e-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="0ba3e-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="0ba3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ba3e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba3e-103">Pobiera listę dostawców usług komunikacji równorzędnej współpracuje z firmą Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="0ba3e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0ba3e-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ba3e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0ba3e-105">DESCRIPTION</span></span>
<span data-ttu-id="0ba3e-106">Lista dostawców usług komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="0ba3e-106">List peering service providers</span></span>

## <span data-ttu-id="0ba3e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0ba3e-107">EXAMPLES</span></span>

### <span data-ttu-id="0ba3e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ba3e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="0ba3e-109">Pobiera dostępnych dostawców usług komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="0ba3e-109">Gets available peering service providers</span></span>

## <span data-ttu-id="0ba3e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ba3e-110">PARAMETERS</span></span>

### <span data-ttu-id="0ba3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba3e-111">-DefaultProfile</span></span>
<span data-ttu-id="0ba3e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ba3e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba3e-113">CommonParameters</span></span>
<span data-ttu-id="0ba3e-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ba3e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba3e-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ba3e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba3e-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ba3e-116">INPUTS</span></span>

### <span data-ttu-id="0ba3e-117">Brak</span><span class="sxs-lookup"><span data-stu-id="0ba3e-117">None</span></span>

## <span data-ttu-id="0ba3e-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ba3e-118">OUTPUTS</span></span>

### <span data-ttu-id="0ba3e-119">Microsoft.Azure.PowerShell.Cmdlet.Peering.Models.PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="0ba3e-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="0ba3e-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0ba3e-120">NOTES</span></span>

## <span data-ttu-id="0ba3e-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ba3e-121">RELATED LINKS</span></span>
