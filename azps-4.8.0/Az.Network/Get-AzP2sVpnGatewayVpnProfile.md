---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: 60937898e7e8c0532a0f0815ee44f2e9f75041c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219524"
---
# <span data-ttu-id="d12a7-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="d12a7-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="d12a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d12a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d12a7-103">Generuje i zwraca adres URL SAS, aby klient mógł pobrać profil sieci VPN dla konfiguracji klienta witryny, aby wskazywały łączność witryny z P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d12a7-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="d12a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d12a7-104">SYNTAX</span></span>

### <span data-ttu-id="d12a7-105">ByP2SVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d12a7-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12a7-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d12a7-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12a7-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d12a7-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d12a7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d12a7-108">DESCRIPTION</span></span>
<span data-ttu-id="d12a7-109">Polecenie cmdlet **Get-AzP2sVpnGatewayVpnProfile** umożliwia generowanie i uzyskiwanie adresu URL SAS, aby klient mógł pobrać profil sieci VPN dla konfiguracji klienta witryny, aby wskazywały łączność witryny z P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d12a7-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="d12a7-110">Wskaż pozycję Konfiguracja klienta witryny przy użyciu tego profilu sieci VPN, aby połączyć się tylko z tym konkretnym P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d12a7-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="d12a7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d12a7-111">EXAMPLES</span></span>

### <span data-ttu-id="d12a7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d12a7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="d12a7-113">Polecenie cmdlet **Get-AzP2sVpnGatewayVpnProfile** umożliwia generowanie i uzyskiwanie adresu URL SAS, aby klient mógł pobrać profil sieci VPN dla konfiguracji klienta witryny, aby wskazywały łączność witryny z P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d12a7-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="d12a7-114">ProfileUrl przedstawia adres URL SAS, z którego klient może pobrać profil sieci VPN dla konfiguracji klienta witryny.</span><span class="sxs-lookup"><span data-stu-id="d12a7-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="d12a7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d12a7-115">PARAMETERS</span></span>

### <span data-ttu-id="d12a7-116">-Metodę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="d12a7-116">-AuthenticationMethod</span></span>
<span data-ttu-id="d12a7-117">Metoda uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="d12a7-117">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d12a7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12a7-118">-DefaultProfile</span></span>
<span data-ttu-id="d12a7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d12a7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d12a7-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d12a7-120">-InputObject</span></span>
<span data-ttu-id="d12a7-121">Obiekt bramy sieci VPN P2S, który ma zostać zmodyfikowany</span><span class="sxs-lookup"><span data-stu-id="d12a7-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d12a7-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d12a7-122">-Name</span></span>
<span data-ttu-id="d12a7-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d12a7-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d12a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d12a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="d12a7-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d12a7-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d12a7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d12a7-126">-ResourceId</span></span>
<span data-ttu-id="d12a7-127">Identyfikator zasobu platformy Azure P2SVpnGateway, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="d12a7-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d12a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12a7-128">CommonParameters</span></span>
<span data-ttu-id="d12a7-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d12a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12a7-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d12a7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12a7-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d12a7-131">INPUTS</span></span>

### <span data-ttu-id="d12a7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d12a7-132">System.String</span></span>
<span data-ttu-id="d12a7-133">Microsoft. Azure. Commands. Network. models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d12a7-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="d12a7-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d12a7-134">OUTPUTS</span></span>

### <span data-ttu-id="d12a7-135">Microsoft. Azure. Commands. Network. models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="d12a7-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="d12a7-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d12a7-136">NOTES</span></span>

## <span data-ttu-id="d12a7-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d12a7-137">RELATED LINKS</span></span>
