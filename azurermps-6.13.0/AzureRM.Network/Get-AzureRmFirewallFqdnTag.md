---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719088"
---
# <span data-ttu-id="2c37a-101">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="2c37a-101">Get-AzureRmFirewallFqdnTag</span></span>

## <span data-ttu-id="2c37a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c37a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c37a-103">Pobiera dostępne znaczniki FQDN zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2c37a-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c37a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c37a-104">SYNTAX</span></span>

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c37a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2c37a-105">DESCRIPTION</span></span>
<span data-ttu-id="2c37a-106">Polecenie cmdlet **Get-AzureRmFirewallFqdnTag** pobiera listę tagów FQDN, których można użyć w regułach aplikacji Zapora platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2c37a-106">The **Get-AzureRmFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="2c37a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c37a-107">EXAMPLES</span></span>

### <span data-ttu-id="2c37a-108">1: pobieranie wszystkich dostępnych tagów FQDN</span><span class="sxs-lookup"><span data-stu-id="2c37a-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzureRmFirewallFqdnTag
```

<span data-ttu-id="2c37a-109">W tym przykładzie są pobierane wszystkie dostępne znaczniki FQDN.</span><span class="sxs-lookup"><span data-stu-id="2c37a-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="2c37a-110">2: używanie znacznika pierwszy dostępny numer FQDN w regule aplikacji</span><span class="sxs-lookup"><span data-stu-id="2c37a-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="2c37a-111">W tym przykładzie przedstawiono tworzenie reguły aplikacji zapory przy użyciu pierwszego dostępnego tagu FQDN</span><span class="sxs-lookup"><span data-stu-id="2c37a-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="2c37a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c37a-112">PARAMETERS</span></span>

### <span data-ttu-id="2c37a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c37a-113">-DefaultProfile</span></span>
<span data-ttu-id="2c37a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c37a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c37a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c37a-115">CommonParameters</span></span>
<span data-ttu-id="2c37a-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c37a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c37a-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c37a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c37a-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c37a-118">INPUTS</span></span>

### <span data-ttu-id="2c37a-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2c37a-119">None</span></span>
<span data-ttu-id="2c37a-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2c37a-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c37a-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c37a-121">OUTPUTS</span></span>

### <span data-ttu-id="2c37a-122">Microsoft. Azure. Commands. Network. models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="2c37a-122">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

## <span data-ttu-id="2c37a-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c37a-123">NOTES</span></span>

## <span data-ttu-id="2c37a-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c37a-124">RELATED LINKS</span></span>

[<span data-ttu-id="2c37a-125">Nowe — AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="2c37a-125">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="2c37a-126">Nowe — AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="2c37a-126">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)
