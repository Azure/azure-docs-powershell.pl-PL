---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: e0a39aac53b13356eb9719cad6e2ade11483cfe7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982458"
---
# <span data-ttu-id="a919f-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="a919f-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="a919f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a919f-102">SYNOPSIS</span></span>
<span data-ttu-id="a919f-103">Generuje i pobiera profil vpn na VirtualWan-VpnServerConfiguration konfiguracji klienta wskaż witrynę.</span><span class="sxs-lookup"><span data-stu-id="a919f-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="a919f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a919f-104">SYNTAX</span></span>

### <span data-ttu-id="a919f-105">ByVirtualWanNameByVpnServerConfigurationObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a919f-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a919f-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a919f-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a919f-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a919f-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a919f-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a919f-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a919f-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a919f-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a919f-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a919f-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a919f-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="a919f-111">DESCRIPTION</span></span>
<span data-ttu-id="a919f-112">Polecenie **cmdlet Get-AzVirtualWanVpnServerConfigurationVpnProfile** umożliwia generowanie i pobieranie profilu vpn na VirtualWan-VpnServerConfiguration konfiguracji klienta typu Point to site.</span><span class="sxs-lookup"><span data-stu-id="a919f-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="a919f-113">Jest to wymagane do połączenia point-site z klienta point-site do usługi Azure P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a919f-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="a919f-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a919f-114">EXAMPLES</span></span>

### <span data-ttu-id="a919f-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a919f-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="a919f-116">Powyższe polecenie wygeneruje i zwróci adres URL SAS klienta w celu pobrania profilu vpn na VirtualWan-VpnServerConfiguration konfiguracji klienta typu Wskaż witrynę.</span><span class="sxs-lookup"><span data-stu-id="a919f-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="a919f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a919f-117">PARAMETERS</span></span>

### <span data-ttu-id="a919f-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="a919f-118">-AuthenticationMethod</span></span>
<span data-ttu-id="a919f-119">Metoda uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="a919f-119">Authentication Method</span></span>

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

### <span data-ttu-id="a919f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a919f-120">-DefaultProfile</span></span>
<span data-ttu-id="a919f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a919f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a919f-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a919f-122">-Name</span></span>
<span data-ttu-id="a919f-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="a919f-123">The resource name.</span></span>

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

### <span data-ttu-id="a919f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a919f-124">-ResourceGroupName</span></span>
<span data-ttu-id="a919f-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a919f-125">The resource group name.</span></span>

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

### <span data-ttu-id="a919f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a919f-126">-ResourceId</span></span>
<span data-ttu-id="a919f-127">Identyfikator zasobu Azure dla wirtualnej sieci Wan.</span><span class="sxs-lookup"><span data-stu-id="a919f-127">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="a919f-128">— VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="a919f-128">-VirtualWanObject</span></span>
<span data-ttu-id="a919f-129">Obiekt wirtualny wan.</span><span class="sxs-lookup"><span data-stu-id="a919f-129">The virtual wan object.</span></span>

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

### <span data-ttu-id="a919f-130">- VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a919f-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="a919f-131">Konfiguracja VpnServerConfiguration, z którą jest skojarzona ta wirtualna zmiana.</span><span class="sxs-lookup"><span data-stu-id="a919f-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

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

### <span data-ttu-id="a919f-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a919f-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="a919f-133">Identyfikator obiektu serwera VPN konfiguruje ten wirtualny wan.</span><span class="sxs-lookup"><span data-stu-id="a919f-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

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

### <span data-ttu-id="a919f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a919f-134">CommonParameters</span></span>
<span data-ttu-id="a919f-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a919f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a919f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a919f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a919f-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a919f-137">INPUTS</span></span>

### <span data-ttu-id="a919f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a919f-138">System.String</span></span>
<span data-ttu-id="a919f-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a919f-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a919f-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a919f-140">OUTPUTS</span></span>

### <span data-ttu-id="a919f-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="a919f-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="a919f-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a919f-142">NOTES</span></span>

## <span data-ttu-id="a919f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a919f-143">RELATED LINKS</span></span>
