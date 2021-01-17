---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372038"
---
# <span data-ttu-id="88592-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="88592-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="88592-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88592-102">SYNOPSIS</span></span>
<span data-ttu-id="88592-103">Pobiera istniejące VpnServerConfiguration dla połączeń z witryną.</span><span class="sxs-lookup"><span data-stu-id="88592-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="88592-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88592-104">SYNTAX</span></span>

### <span data-ttu-id="88592-105">ListBySubscriptionId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="88592-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88592-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88592-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88592-107">Opis</span><span class="sxs-lookup"><span data-stu-id="88592-107">DESCRIPTION</span></span>
<span data-ttu-id="88592-108">Polecenie cmdlet **Get-AzVpnServerConfiguration** zwraca istniejące VpnServerConfiguration na potrzeby połączenia z witryną.</span><span class="sxs-lookup"><span data-stu-id="88592-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="88592-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88592-109">EXAMPLES</span></span>

### <span data-ttu-id="88592-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88592-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name test1config

ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="88592-111">Powyższe polecenie otrzyma istniejące VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="88592-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="88592-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88592-112">PARAMETERS</span></span>

### <span data-ttu-id="88592-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88592-113">-DefaultProfile</span></span>
<span data-ttu-id="88592-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88592-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88592-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88592-115">-Name</span></span>
<span data-ttu-id="88592-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="88592-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnServerConfigurationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88592-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88592-117">-ResourceGroupName</span></span>
<span data-ttu-id="88592-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="88592-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88592-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88592-119">CommonParameters</span></span>
<span data-ttu-id="88592-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88592-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88592-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88592-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88592-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88592-122">INPUTS</span></span>

### <span data-ttu-id="88592-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="88592-123">None</span></span>

## <span data-ttu-id="88592-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88592-124">OUTPUTS</span></span>

### <span data-ttu-id="88592-125">Microsoft. Azure. Commands. Network. models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="88592-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="88592-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88592-126">NOTES</span></span>

## <span data-ttu-id="88592-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88592-127">RELATED LINKS</span></span>
