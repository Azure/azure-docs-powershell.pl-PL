---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: e1d7c2d78bf58240cc87e7a224be1632828984d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052223"
---
# <span data-ttu-id="aa157-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="aa157-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="aa157-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa157-102">SYNOPSIS</span></span>
<span data-ttu-id="aa157-103">Utwórz konfigurację adresu IP usługi linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="aa157-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="aa157-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa157-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa157-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa157-105">DESCRIPTION</span></span>
<span data-ttu-id="aa157-106">Polecenie cmdlet **New-AzPrivateLinkServiceIpConfig** umożliwia utworzenie konfiguracji adresu IP usługi link Private.</span><span class="sxs-lookup"><span data-stu-id="aa157-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="aa157-107">Ta konfiguracja jest używana w przypadku źródłowego translatora NAT — przepuszczasz ruch przychodzący z prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="aa157-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="aa157-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa157-108">EXAMPLES</span></span>

### <span data-ttu-id="aa157-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa157-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="aa157-110">W tym przykładzie przedstawiono konfigurację adresu IP usługi linku prywatnego w pamięci.</span><span class="sxs-lookup"><span data-stu-id="aa157-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="aa157-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa157-111">PARAMETERS</span></span>

### <span data-ttu-id="aa157-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa157-112">-DefaultProfile</span></span>
<span data-ttu-id="aa157-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa157-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa157-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa157-114">-Name</span></span>
<span data-ttu-id="aa157-115">Nazwa elementu IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa157-115">The name of the IpConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa157-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="aa157-116">-PrivateIpAddress</span></span>
<span data-ttu-id="aa157-117">Prywatny adres IP elementu ipConfiguration, jeśli jest określony przydział statyczny.</span><span class="sxs-lookup"><span data-stu-id="aa157-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa157-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="aa157-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="aa157-119">Wersja IP konfiguracji protokołu IP</span><span class="sxs-lookup"><span data-stu-id="aa157-119">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa157-120">-Primary</span><span class="sxs-lookup"><span data-stu-id="aa157-120">-Primary</span></span>
<span data-ttu-id="aa157-121">Wskazuje, że bieżąca Konfiguracja IP jest podstawowa lub nie.</span><span class="sxs-lookup"><span data-stu-id="aa157-121">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="aa157-122">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="aa157-122">-Subnet</span></span>
<span data-ttu-id="aa157-123">Żąda</span><span class="sxs-lookup"><span data-stu-id="aa157-123">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa157-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa157-124">CommonParameters</span></span>
<span data-ttu-id="aa157-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa157-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa157-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa157-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa157-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa157-127">INPUTS</span></span>

### <span data-ttu-id="aa157-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aa157-128">None</span></span>

## <span data-ttu-id="aa157-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa157-129">OUTPUTS</span></span>

### <span data-ttu-id="aa157-130">Microsoft. Azure. Commands. Network. models. PSPrivateLinkServiceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa157-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="aa157-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa157-131">NOTES</span></span>

## <span data-ttu-id="aa157-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa157-132">RELATED LINKS</span></span>

[<span data-ttu-id="aa157-133">Nowe — AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="aa157-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)