---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223696"
---
# <span data-ttu-id="65693-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="65693-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="65693-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65693-102">SYNOPSIS</span></span>
<span data-ttu-id="65693-103">Pobiera listę dostawców usług komunikacji równorzędnej z partnerem firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="65693-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="65693-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65693-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65693-105">Opis</span><span class="sxs-lookup"><span data-stu-id="65693-105">DESCRIPTION</span></span>
<span data-ttu-id="65693-106">Wyświetlanie dostawców usług równorzędnych</span><span class="sxs-lookup"><span data-stu-id="65693-106">List peering service providers</span></span>

## <span data-ttu-id="65693-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65693-107">EXAMPLES</span></span>

### <span data-ttu-id="65693-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65693-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="65693-109">Pobiera dostępnych dostawców usług komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="65693-109">Gets available peering service providers</span></span>

## <span data-ttu-id="65693-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65693-110">PARAMETERS</span></span>

### <span data-ttu-id="65693-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65693-111">-DefaultProfile</span></span>
<span data-ttu-id="65693-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65693-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65693-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65693-113">CommonParameters</span></span>
<span data-ttu-id="65693-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65693-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65693-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65693-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65693-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65693-116">INPUTS</span></span>

### <span data-ttu-id="65693-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="65693-117">None</span></span>

## <span data-ttu-id="65693-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65693-118">OUTPUTS</span></span>

### <span data-ttu-id="65693-119">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="65693-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="65693-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65693-120">NOTES</span></span>

## <span data-ttu-id="65693-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65693-121">RELATED LINKS</span></span>
