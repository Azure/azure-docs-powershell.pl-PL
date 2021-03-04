---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: a2b3a4878db022018bd0fae1d8e43e3700dd5e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958362"
---
# <span data-ttu-id="b282c-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="b282c-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="b282c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b282c-102">SYNOPSIS</span></span>
<span data-ttu-id="b282c-103">Tworzenie obiektu zasad podziału ruchu usługi Office 365.</span><span class="sxs-lookup"><span data-stu-id="b282c-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="b282c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b282c-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b282c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b282c-105">DESCRIPTION</span></span>
<span data-ttu-id="b282c-106">Utwórz zasady podziału usługi Office 365, które będą używane z New-AzVpnSite i Update-AzVpnSite cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b282c-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="b282c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b282c-107">EXAMPLES</span></span>

### <span data-ttu-id="b282c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b282c-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="b282c-109">Utwórz zasady dotyczące przerw w ruchu usługi Office 365 z przerwami dozwolonymi w celu zezwalania na i optymalizowania kategorii ruchu.</span><span class="sxs-lookup"><span data-stu-id="b282c-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="b282c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b282c-110">PARAMETERS</span></span>

### <span data-ttu-id="b282c-111">— Zezwalaj</span><span class="sxs-lookup"><span data-stu-id="b282c-111">-Allow</span></span>
<span data-ttu-id="b282c-112">Rozbijanie ruchu kategorii zezwalania.</span><span class="sxs-lookup"><span data-stu-id="b282c-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="b282c-113">— Domyślne</span><span class="sxs-lookup"><span data-stu-id="b282c-113">-Default</span></span>
<span data-ttu-id="b282c-114">Rozbijanie domyślnego ruchu kategorii.</span><span class="sxs-lookup"><span data-stu-id="b282c-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="b282c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b282c-115">-DefaultProfile</span></span>
<span data-ttu-id="b282c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b282c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b282c-117">— Optymalizowanie</span><span class="sxs-lookup"><span data-stu-id="b282c-117">-Optimize</span></span>
<span data-ttu-id="b282c-118">Rozbijanie ruchu kategorii optymalizowania.</span><span class="sxs-lookup"><span data-stu-id="b282c-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="b282c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b282c-119">CommonParameters</span></span>
<span data-ttu-id="b282c-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b282c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b282c-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b282c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b282c-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b282c-122">INPUTS</span></span>

### <span data-ttu-id="b282c-123">Brak</span><span class="sxs-lookup"><span data-stu-id="b282c-123">None</span></span>

## <span data-ttu-id="b282c-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b282c-124">OUTPUTS</span></span>

### <span data-ttu-id="b282c-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="b282c-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="b282c-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b282c-126">NOTES</span></span>

## <span data-ttu-id="b282c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b282c-127">RELATED LINKS</span></span>
