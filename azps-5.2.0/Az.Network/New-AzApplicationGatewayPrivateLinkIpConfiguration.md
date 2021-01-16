---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333358"
---
# <span data-ttu-id="ebc36-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebc36-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="ebc36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebc36-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc36-103">Tworzy konfigurację IP, która ma być skojarzona z konfiguracją PrivateLink</span><span class="sxs-lookup"><span data-stu-id="ebc36-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="ebc36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebc36-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebc36-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ebc36-105">DESCRIPTION</span></span>
<span data-ttu-id="ebc36-106">Polecenie cmdlet **New-AzApplicationGatewayPrivateLinkIpConfiguration** umożliwia utworzenie konfiguracji IP, która ma być skojarzona z konfiguracją usługi PrivateLink dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ebc36-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="ebc36-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebc36-107">EXAMPLES</span></span>

### <span data-ttu-id="ebc36-108">Przykład 1: PrivateLink IP</span><span class="sxs-lookup"><span data-stu-id="ebc36-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="ebc36-109">To polecenie tworzy PrivateLink IP o nazwie "ipConfig01". zapisuje wynik w zmiennej o nazwie $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ebc36-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="ebc36-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebc36-110">PARAMETERS</span></span>

### <span data-ttu-id="ebc36-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc36-111">-DefaultProfile</span></span>
<span data-ttu-id="ebc36-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebc36-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebc36-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ebc36-113">-Name</span></span>
<span data-ttu-id="ebc36-114">Nazwa elementu IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebc36-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="ebc36-115">-Primary</span><span class="sxs-lookup"><span data-stu-id="ebc36-115">-Primary</span></span>
<span data-ttu-id="ebc36-116">Wskazuje, że Konfiguracja IP jest podstawowa.</span><span class="sxs-lookup"><span data-stu-id="ebc36-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="ebc36-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ebc36-117">-PrivateIpAddress</span></span>
<span data-ttu-id="ebc36-118">Prywatny adres IP elementu ipConfiguration, jeśli alokacja statyczna jest pożądana.</span><span class="sxs-lookup"><span data-stu-id="ebc36-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="ebc36-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="ebc36-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="ebc36-120">Wersja IP konfiguracji protokołu IP</span><span class="sxs-lookup"><span data-stu-id="ebc36-120">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="ebc36-121">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="ebc36-121">-Subnet</span></span>
<span data-ttu-id="ebc36-122">Żąda</span><span class="sxs-lookup"><span data-stu-id="ebc36-122">Subnet</span></span>

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

### <span data-ttu-id="ebc36-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc36-123">CommonParameters</span></span>
<span data-ttu-id="ebc36-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebc36-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc36-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebc36-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc36-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebc36-126">INPUTS</span></span>

### <span data-ttu-id="ebc36-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ebc36-127">None</span></span>

## <span data-ttu-id="ebc36-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebc36-128">OUTPUTS</span></span>

### <span data-ttu-id="ebc36-129">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebc36-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="ebc36-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebc36-130">NOTES</span></span>

## <span data-ttu-id="ebc36-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebc36-131">RELATED LINKS</span></span>

[<span data-ttu-id="ebc36-132">Nowe — AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebc36-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
