---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223784"
---
# <span data-ttu-id="6d70a-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="6d70a-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="6d70a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d70a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d70a-103">Utwórz obiekt zasad podgrupa ruchu pakietu Office 365.</span><span class="sxs-lookup"><span data-stu-id="6d70a-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="6d70a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d70a-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d70a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d70a-105">DESCRIPTION</span></span>
<span data-ttu-id="6d70a-106">Utwórz zasady podgrupa pakietu Office 365, które mają być używane z poleceniami cmdlet New-AzVpnSite i Update-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="6d70a-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="6d70a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d70a-107">EXAMPLES</span></span>

### <span data-ttu-id="6d70a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d70a-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="6d70a-109">Utwórz zasady podgrupa ruchu pakietu Office 365 z podgrupa dozwolonym dla dozwolonych i optymalizowanych kategorii ruchu.</span><span class="sxs-lookup"><span data-stu-id="6d70a-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="6d70a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d70a-110">PARAMETERS</span></span>

### <span data-ttu-id="6d70a-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="6d70a-111">-Allow</span></span>
<span data-ttu-id="6d70a-112">Podgrupa ruch kategorii Zezwól.</span><span class="sxs-lookup"><span data-stu-id="6d70a-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d70a-113">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="6d70a-113">-Default</span></span>
<span data-ttu-id="6d70a-114">Podgrupa domyślny ruch kategorii.</span><span class="sxs-lookup"><span data-stu-id="6d70a-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d70a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d70a-115">-DefaultProfile</span></span>
<span data-ttu-id="6d70a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d70a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d70a-117">— Optymalizuj</span><span class="sxs-lookup"><span data-stu-id="6d70a-117">-Optimize</span></span>
<span data-ttu-id="6d70a-118">Podgrupa ruch kategorii.</span><span class="sxs-lookup"><span data-stu-id="6d70a-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d70a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d70a-119">CommonParameters</span></span>
<span data-ttu-id="6d70a-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d70a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d70a-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d70a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d70a-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d70a-122">INPUTS</span></span>

### <span data-ttu-id="6d70a-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6d70a-123">None</span></span>

## <span data-ttu-id="6d70a-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d70a-124">OUTPUTS</span></span>

### <span data-ttu-id="6d70a-125">Microsoft. Azure. Commands. Network. models. PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="6d70a-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="6d70a-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d70a-126">NOTES</span></span>

## <span data-ttu-id="6d70a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d70a-127">RELATED LINKS</span></span>
