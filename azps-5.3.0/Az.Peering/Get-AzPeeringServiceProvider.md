---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceProvider.md
ms.openlocfilehash: 8341f465bab88f8d8a60e5f171f883dbb9a2467e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384848"
---
# <span data-ttu-id="b423f-101">Get-AzPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b423f-101">Get-AzPeeringServiceProvider</span></span>

## <span data-ttu-id="b423f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b423f-102">SYNOPSIS</span></span>
<span data-ttu-id="b423f-103">Pobiera listę dostawców usług komunikacji równorzędnej z partnerem firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b423f-103">Gets a list of peering service providers partnered with Microsoft.</span></span>

## <span data-ttu-id="b423f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b423f-104">SYNTAX</span></span>

```
Get-AzPeeringServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b423f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b423f-105">DESCRIPTION</span></span>
<span data-ttu-id="b423f-106">Wyświetlanie dostawców usług równorzędnych</span><span class="sxs-lookup"><span data-stu-id="b423f-106">List peering service providers</span></span>

## <span data-ttu-id="b423f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b423f-107">EXAMPLES</span></span>

### <span data-ttu-id="b423f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b423f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringServiceProvider

ServiceProviderName Name      Id Type
------------------- ----      -- ----
TestPeer1           TestPeer1    Microsoft.Peering/peeringServiceProviders
```

<span data-ttu-id="b423f-109">Pobiera dostępnych dostawców usług komunikacji równorzędnej</span><span class="sxs-lookup"><span data-stu-id="b423f-109">Gets available peering service providers</span></span>

## <span data-ttu-id="b423f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b423f-110">PARAMETERS</span></span>

### <span data-ttu-id="b423f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b423f-111">-DefaultProfile</span></span>
<span data-ttu-id="b423f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b423f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b423f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b423f-113">CommonParameters</span></span>
<span data-ttu-id="b423f-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b423f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b423f-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b423f-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b423f-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b423f-116">INPUTS</span></span>

### <span data-ttu-id="b423f-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b423f-117">None</span></span>

## <span data-ttu-id="b423f-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b423f-118">OUTPUTS</span></span>

### <span data-ttu-id="b423f-119">Microsoft. Azure. PowerShell. cmdlet. peer. MODELES. PSPeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b423f-119">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceProvider</span></span>

## <span data-ttu-id="b423f-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b423f-120">NOTES</span></span>

## <span data-ttu-id="b423f-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b423f-121">RELATED LINKS</span></span>
