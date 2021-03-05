---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 4a34899a4e6c37ad3d4c84c173d07012110dcad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986742"
---
# <span data-ttu-id="ed06f-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed06f-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="ed06f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed06f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed06f-103">Tworzy konfigurację adresów IP, która ma zostać skojarzona z konfiguracją privatelinku</span><span class="sxs-lookup"><span data-stu-id="ed06f-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="ed06f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed06f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed06f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed06f-105">DESCRIPTION</span></span>
<span data-ttu-id="ed06f-106">Polecenie cmdlet **New-AzApplicationGatewayPrivateLinkIpConfiguration** tworzy konfigurację ip, która ma być skojarzona z konfiguracją privatelinku dla bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="ed06f-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="ed06f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed06f-107">EXAMPLES</span></span>

### <span data-ttu-id="ed06f-108">Przykład 1. Konfiguracja adresu IP PrivateLink</span><span class="sxs-lookup"><span data-stu-id="ed06f-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="ed06f-109">To polecenie tworzy konfigurację adresów IP PrivateLink o nazwie "ipConfig01" i zapisuje wynik w zmiennej o nazwie $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ed06f-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="ed06f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed06f-110">PARAMETERS</span></span>

### <span data-ttu-id="ed06f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed06f-111">-DefaultProfile</span></span>
<span data-ttu-id="ed06f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed06f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed06f-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ed06f-113">-Name</span></span>
<span data-ttu-id="ed06f-114">Nazwa konfiguracji IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed06f-114">The name of the IpConfiguration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed06f-115">— podstawowy</span><span class="sxs-lookup"><span data-stu-id="ed06f-115">-Primary</span></span>
<span data-ttu-id="ed06f-116">Wskazuje, że konfiguracja adresu IP jest podstawowa.</span><span class="sxs-lookup"><span data-stu-id="ed06f-116">Indicate the ip configuration is primary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed06f-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ed06f-117">-PrivateIpAddress</span></span>
<span data-ttu-id="ed06f-118">Prywatny adres IP konfiguracji ip, jeśli jest wymagany przydział statyczny.</span><span class="sxs-lookup"><span data-stu-id="ed06f-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="ed06f-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="ed06f-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="ed06f-120">Wersja ip konfiguracji protokołu IP</span><span class="sxs-lookup"><span data-stu-id="ed06f-120">The ip version of the ip configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed06f-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="ed06f-121">-Subnet</span></span>
<span data-ttu-id="ed06f-122">Podsieci</span><span class="sxs-lookup"><span data-stu-id="ed06f-122">Subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed06f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed06f-123">CommonParameters</span></span>
<span data-ttu-id="ed06f-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed06f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed06f-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed06f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed06f-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed06f-126">INPUTS</span></span>

### <span data-ttu-id="ed06f-127">Brak</span><span class="sxs-lookup"><span data-stu-id="ed06f-127">None</span></span>

## <span data-ttu-id="ed06f-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed06f-128">OUTPUTS</span></span>

### <span data-ttu-id="ed06f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed06f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="ed06f-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed06f-130">NOTES</span></span>

## <span data-ttu-id="ed06f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed06f-131">RELATED LINKS</span></span>

[<span data-ttu-id="ed06f-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed06f-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
