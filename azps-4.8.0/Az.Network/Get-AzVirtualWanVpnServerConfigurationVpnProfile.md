---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064399"
---
# <span data-ttu-id="f02f8-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="f02f8-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="f02f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f02f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f02f8-103">Generuje i pobiera profil sieci VPN na poziomie VirtualWan-VpnServerConfiguration, aby wskazać konfigurację klienta witryny.</span><span class="sxs-lookup"><span data-stu-id="f02f8-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="f02f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f02f8-104">SYNTAX</span></span>

### <span data-ttu-id="f02f8-105">ByVirtualWanNameByVpnServerConfigurationObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f02f8-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f02f8-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="f02f8-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f02f8-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="f02f8-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f02f8-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="f02f8-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f02f8-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="f02f8-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f02f8-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="f02f8-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f02f8-111">Opis</span><span class="sxs-lookup"><span data-stu-id="f02f8-111">DESCRIPTION</span></span>
<span data-ttu-id="f02f8-112">Polecenie cmdlet **Get-AzVirtualWanVpnServerConfigurationVpnProfile** umożliwia generowanie i pobieranie profilu sieci VPN na poziomie VirtualWan-VpnServerConfiguration, aby wskazać konfigurację klienta witryny.</span><span class="sxs-lookup"><span data-stu-id="f02f8-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="f02f8-113">Jest to wymagane do prowadzenia łączności z witryną od punktu klienckiego lokacji do usługi Azure P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f02f8-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="f02f8-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f02f8-114">EXAMPLES</span></span>

### <span data-ttu-id="f02f8-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f02f8-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="f02f8-116">Powyższe polecenie wygeneruje i zwróci adres URL SAS dla klienta w celu pobrania profilu sieci VPN na poziomie VirtualWan-VpnServerConfiguration, aby wskazać konfigurację klienta witryny.</span><span class="sxs-lookup"><span data-stu-id="f02f8-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="f02f8-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f02f8-117">PARAMETERS</span></span>

### <span data-ttu-id="f02f8-118">-Metodę uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="f02f8-118">-AuthenticationMethod</span></span>
<span data-ttu-id="f02f8-119">Metoda uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="f02f8-119">Authentication Method</span></span>

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

### <span data-ttu-id="f02f8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f02f8-120">-DefaultProfile</span></span>
<span data-ttu-id="f02f8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f02f8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f02f8-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f02f8-122">-Name</span></span>
<span data-ttu-id="f02f8-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="f02f8-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f02f8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f02f8-124">-ResourceGroupName</span></span>
<span data-ttu-id="f02f8-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f02f8-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f02f8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f02f8-126">-ResourceId</span></span>
<span data-ttu-id="f02f8-127">Identyfikator zasobu platformy Azure dla wirtualnej sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="f02f8-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02f8-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="f02f8-128">-VirtualWanObject</span></span>
<span data-ttu-id="f02f8-129">Wirtualny obiekt sieci WAN.</span><span class="sxs-lookup"><span data-stu-id="f02f8-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f02f8-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f02f8-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="f02f8-131">VpnServerConfiguration, z którym jest skojarzony ten VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f02f8-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f02f8-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f02f8-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="f02f8-133">Identyfikator obiektu configuraiton serwera sieci VPN, z którym skojarzona jest ta wirtualna sieć WAN.</span><span class="sxs-lookup"><span data-stu-id="f02f8-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f02f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02f8-134">CommonParameters</span></span>
<span data-ttu-id="f02f8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02f8-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f02f8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02f8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f02f8-137">INPUTS</span></span>

### <span data-ttu-id="f02f8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f02f8-138">System.String</span></span>
<span data-ttu-id="f02f8-139">Microsoft. Azure. Commands. Network. models. PSVirtualWan Microsoft. Azure. Commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f02f8-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="f02f8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f02f8-140">OUTPUTS</span></span>

### <span data-ttu-id="f02f8-141">Microsoft. Azure. Commands. Network. models. PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="f02f8-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="f02f8-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f02f8-142">NOTES</span></span>

## <span data-ttu-id="f02f8-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f02f8-143">RELATED LINKS</span></span>
