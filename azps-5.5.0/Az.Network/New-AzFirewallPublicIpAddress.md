---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202812"
---
# <span data-ttu-id="a79e9-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a79e9-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="a79e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a79e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a79e9-103">Jest to symbol zastępczy adresu IP, który może być używany dla wielu rur w zaporze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a79e9-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="a79e9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a79e9-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a79e9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a79e9-105">DESCRIPTION</span></span>
<span data-ttu-id="a79e9-106">Jest to symbol zastępczy adresu IP, który może być używany dla wielu rur w zaporze platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a79e9-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="a79e9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a79e9-107">EXAMPLES</span></span>

### <span data-ttu-id="a79e9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a79e9-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="a79e9-109">$publicIp będzie symbolem zastępczym adresu IP 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="a79e9-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="a79e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a79e9-110">PARAMETERS</span></span>

### <span data-ttu-id="a79e9-111">— Adres</span><span class="sxs-lookup"><span data-stu-id="a79e9-111">-Address</span></span>
<span data-ttu-id="a79e9-112">Adresy IP zapory podłączonej do centrum</span><span class="sxs-lookup"><span data-stu-id="a79e9-112">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79e9-113">-DefaultProfile</span></span>
<span data-ttu-id="a79e9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a79e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79e9-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a79e9-115">-Confirm</span></span>
<span data-ttu-id="a79e9-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a79e9-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79e9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a79e9-117">-WhatIf</span></span>
<span data-ttu-id="a79e9-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a79e9-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a79e9-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a79e9-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79e9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79e9-120">CommonParameters</span></span>
<span data-ttu-id="a79e9-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a79e9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79e9-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a79e9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79e9-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a79e9-123">INPUTS</span></span>

### <span data-ttu-id="a79e9-124">Brak</span><span class="sxs-lookup"><span data-stu-id="a79e9-124">None</span></span>

## <span data-ttu-id="a79e9-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a79e9-125">OUTPUTS</span></span>

### <span data-ttu-id="a79e9-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a79e9-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="a79e9-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a79e9-127">NOTES</span></span>

## <span data-ttu-id="a79e9-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a79e9-128">RELATED LINKS</span></span>
