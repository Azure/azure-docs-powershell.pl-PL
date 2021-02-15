---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193595"
---
# <span data-ttu-id="32e4f-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="32e4f-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="32e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="32e4f-103">Tworzenie obiektu zasad podziału ruchu usługi Office 365.</span><span class="sxs-lookup"><span data-stu-id="32e4f-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="32e4f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="32e4f-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32e4f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="32e4f-105">DESCRIPTION</span></span>
<span data-ttu-id="32e4f-106">Utwórz zasady podziału usługi Office 365, które będą używane z New-AzVpnSite i Update-AzVpnSite cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e4f-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="32e4f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="32e4f-107">EXAMPLES</span></span>

### <span data-ttu-id="32e4f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="32e4f-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="32e4f-109">Utwórz zasady dotyczące przerw w ruchu usługi Office 365 z podziałem dozwolonym w celu zezwalania na i optymalizowania kategorii ruchu.</span><span class="sxs-lookup"><span data-stu-id="32e4f-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="32e4f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32e4f-110">PARAMETERS</span></span>

### <span data-ttu-id="32e4f-111">— Zezwalaj</span><span class="sxs-lookup"><span data-stu-id="32e4f-111">-Allow</span></span>
<span data-ttu-id="32e4f-112">Rozbijanie ruchu kategorii zezwalaj na.</span><span class="sxs-lookup"><span data-stu-id="32e4f-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="32e4f-113">— Domyślne</span><span class="sxs-lookup"><span data-stu-id="32e4f-113">-Default</span></span>
<span data-ttu-id="32e4f-114">Rozbijanie domyślnego ruchu kategorii.</span><span class="sxs-lookup"><span data-stu-id="32e4f-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="32e4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e4f-115">-DefaultProfile</span></span>
<span data-ttu-id="32e4f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="32e4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32e4f-117">— Optymalizowanie</span><span class="sxs-lookup"><span data-stu-id="32e4f-117">-Optimize</span></span>
<span data-ttu-id="32e4f-118">Rozbijanie ruchu kategorii optymalizowania.</span><span class="sxs-lookup"><span data-stu-id="32e4f-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="32e4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e4f-119">CommonParameters</span></span>
<span data-ttu-id="32e4f-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e4f-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32e4f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e4f-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32e4f-122">INPUTS</span></span>

### <span data-ttu-id="32e4f-123">Brak</span><span class="sxs-lookup"><span data-stu-id="32e4f-123">None</span></span>

## <span data-ttu-id="32e4f-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32e4f-124">OUTPUTS</span></span>

### <span data-ttu-id="32e4f-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="32e4f-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="32e4f-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="32e4f-126">NOTES</span></span>

## <span data-ttu-id="32e4f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32e4f-127">RELATED LINKS</span></span>
