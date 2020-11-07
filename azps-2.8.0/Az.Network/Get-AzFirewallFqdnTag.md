---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 28a7fa45c8c6dc291f5e0c2a54c9fcf5fb5242dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870699"
---
# <span data-ttu-id="abc7b-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="abc7b-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="abc7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="abc7b-102">SYNOPSIS</span></span>
<span data-ttu-id="abc7b-103">Pobiera dostępne znaczniki FQDN zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="abc7b-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="abc7b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="abc7b-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abc7b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="abc7b-105">DESCRIPTION</span></span>
<span data-ttu-id="abc7b-106">Polecenie cmdlet **Get-AzFirewallFqdnTag** pobiera listę tagów FQDN, których można użyć w regułach aplikacji Zapora platformy Azure</span><span class="sxs-lookup"><span data-stu-id="abc7b-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="abc7b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="abc7b-107">EXAMPLES</span></span>

### <span data-ttu-id="abc7b-108">1: pobieranie wszystkich dostępnych tagów FQDN</span><span class="sxs-lookup"><span data-stu-id="abc7b-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="abc7b-109">W tym przykładzie są pobierane wszystkie dostępne znaczniki FQDN.</span><span class="sxs-lookup"><span data-stu-id="abc7b-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="abc7b-110">2: używanie znacznika pierwszy dostępny numer FQDN w regule aplikacji</span><span class="sxs-lookup"><span data-stu-id="abc7b-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="abc7b-111">W tym przykładzie przedstawiono tworzenie reguły aplikacji zapory przy użyciu pierwszego dostępnego tagu FQDN</span><span class="sxs-lookup"><span data-stu-id="abc7b-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="abc7b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abc7b-112">PARAMETERS</span></span>

### <span data-ttu-id="abc7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc7b-113">-DefaultProfile</span></span>
<span data-ttu-id="abc7b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="abc7b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abc7b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc7b-115">CommonParameters</span></span>
<span data-ttu-id="abc7b-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc7b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc7b-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abc7b-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc7b-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abc7b-118">INPUTS</span></span>

### <span data-ttu-id="abc7b-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="abc7b-119">None</span></span>

## <span data-ttu-id="abc7b-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="abc7b-120">OUTPUTS</span></span>

### <span data-ttu-id="abc7b-121">Microsoft. Azure. Commands. Network. models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="abc7b-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="abc7b-122">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. models. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. PowerShell</span><span class="sxs-lookup"><span data-stu-id="abc7b-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="abc7b-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="abc7b-123">NOTES</span></span>

## <span data-ttu-id="abc7b-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abc7b-124">RELATED LINKS</span></span>

[<span data-ttu-id="abc7b-125">Nowe — AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="abc7b-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="abc7b-126">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="abc7b-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
