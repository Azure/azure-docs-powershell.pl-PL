---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azp2svpngatewayvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayVpnProfile.md
ms.openlocfilehash: e606f961cf54eb390e76e3f9bc8c00e556aff7fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954241"
---
# <span data-ttu-id="c43d6-101">Get-AzP2sVpnGatewayVpnProfile</span><span class="sxs-lookup"><span data-stu-id="c43d6-101">Get-AzP2sVpnGatewayVpnProfile</span></span>

## <span data-ttu-id="c43d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c43d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c43d6-103">Generuje i zwraca adres URL SAS klienta, aby pobrać profil VPN, aby wskazać konfigurację klienta witryny, która ma wskazać łączność z witryną P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c43d6-103">Generates and returns a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span>

## <span data-ttu-id="c43d6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c43d6-104">SYNTAX</span></span>

### <span data-ttu-id="c43d6-105">ByP2SVpnGatewayName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c43d6-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayVpnProfile [-Name <String>] -ResourceGroupName <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c43d6-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c43d6-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -InputObject <PSP2SVpnGateway> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c43d6-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c43d6-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayVpnProfile -ResourceId <String> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c43d6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c43d6-108">DESCRIPTION</span></span>
<span data-ttu-id="c43d6-109">Polecenie cmdlet **Get-AzP2sVpnGatewayVpnProfile** umożliwia generowanie i pobieranie adresu URL SAS klienta w celu pobrania profilu vpn w celu przekierowania konfiguracji klienta witryny do łączności z witryną P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c43d6-109">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="c43d6-110">Wskaż konfigurację klienta witryny przy użyciu tego profilu vpn, który może połączyć się tylko z tą konkretną aplikacją P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c43d6-110">Point to site client setup using this Vpn profile can connect to this specific P2SVpnGateway only.</span></span>

## <span data-ttu-id="c43d6-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c43d6-111">EXAMPLES</span></span>

### <span data-ttu-id="c43d6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c43d6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayVpnProfile -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -AuthenticationMethod EAPTLS


ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/8cf00031-37ec-4949-b74a-48f9021bf4c0/vpnprofile/2f132439-1051-44c6-9128-b704c1c48cf7/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=HmBSprVrs
             6hDY3x1HX958nimOjavnEjL2rlSuKIIW8Q%3D&st=2019-10-25T19%3A20%3A04Z&se=2019-10-25T20%3A20%3A04Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="c43d6-113">Polecenie cmdlet **Get-AzP2sVpnGatewayVpnProfile** umożliwia generowanie i pobieranie adresu URL SAS klienta w celu pobrania profilu vpn w celu przekierowania konfiguracji klienta witryny do łączności z witryną P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="c43d6-113">The **Get-AzP2sVpnGatewayVpnProfile** cmdlet enables you to generate and get a SAS url for customer to download Vpn profile for point to site client setup to have point to site connectivity to P2SVpnGateway.</span></span> <span data-ttu-id="c43d6-114">ProfileUrl pokazuje adres URL SAS, z którego klient może pobrać profil VPN w celu punktu konfiguracji klienta witryny.</span><span class="sxs-lookup"><span data-stu-id="c43d6-114">ProfileUrl shows the SAS url from where customer can download Vpn profile for point to site client setup.</span></span>

## <span data-ttu-id="c43d6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c43d6-115">PARAMETERS</span></span>

### <span data-ttu-id="c43d6-116">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="c43d6-116">-AuthenticationMethod</span></span>
<span data-ttu-id="c43d6-117">Metoda uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="c43d6-117">Authentication Method</span></span>

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

### <span data-ttu-id="c43d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43d6-118">-DefaultProfile</span></span>
<span data-ttu-id="c43d6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c43d6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c43d6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c43d6-120">-InputObject</span></span>
<span data-ttu-id="c43d6-121">Obiekt bramy sieci vpn p2s do modyfikacji</span><span class="sxs-lookup"><span data-stu-id="c43d6-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="c43d6-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c43d6-122">-Name</span></span>
<span data-ttu-id="c43d6-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c43d6-123">The resource name.</span></span>

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

### <span data-ttu-id="c43d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c43d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="c43d6-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c43d6-125">The resource group name.</span></span>

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

### <span data-ttu-id="c43d6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c43d6-126">-ResourceId</span></span>
<span data-ttu-id="c43d6-127">Identyfikator zasobu Azure p2SVpnGateway do modyfikacji.</span><span class="sxs-lookup"><span data-stu-id="c43d6-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="c43d6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43d6-128">CommonParameters</span></span>
<span data-ttu-id="c43d6-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c43d6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43d6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c43d6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43d6-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c43d6-131">INPUTS</span></span>

### <span data-ttu-id="c43d6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c43d6-132">System.String</span></span>
<span data-ttu-id="c43d6-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="c43d6-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="c43d6-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c43d6-134">OUTPUTS</span></span>

### <span data-ttu-id="c43d6-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="c43d6-135">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="c43d6-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c43d6-136">NOTES</span></span>

## <span data-ttu-id="c43d6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c43d6-137">RELATED LINKS</span></span>
