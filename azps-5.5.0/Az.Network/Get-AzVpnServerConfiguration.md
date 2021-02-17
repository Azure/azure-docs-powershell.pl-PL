---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184563"
---
# <span data-ttu-id="03f42-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="03f42-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="03f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03f42-102">SYNOPSIS</span></span>
<span data-ttu-id="03f42-103">Pobiera istniejącą konfigurację VpnServerConfiguration dla łączności punktowej z witryną.</span><span class="sxs-lookup"><span data-stu-id="03f42-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="03f42-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03f42-104">SYNTAX</span></span>

### <span data-ttu-id="03f42-105">ListBySubscriptionId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="03f42-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03f42-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03f42-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03f42-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="03f42-107">DESCRIPTION</span></span>
<span data-ttu-id="03f42-108">Polecenie **cmdlet Get-AzVpnServerConfiguration** zwraca istniejącą konfigurację VpnServerConfiguration dla łączności typu Point to site.</span><span class="sxs-lookup"><span data-stu-id="03f42-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="03f42-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03f42-109">EXAMPLES</span></span>

### <span data-ttu-id="03f42-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03f42-110">Example 1</span></span>
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

<span data-ttu-id="03f42-111">Powyższe polecenie pobierze istniejącą konfigurację VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="03f42-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="03f42-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03f42-112">PARAMETERS</span></span>

### <span data-ttu-id="03f42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03f42-113">-DefaultProfile</span></span>
<span data-ttu-id="03f42-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="03f42-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03f42-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="03f42-115">-Name</span></span>
<span data-ttu-id="03f42-116">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="03f42-116">The resource name.</span></span>

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

### <span data-ttu-id="03f42-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03f42-117">-ResourceGroupName</span></span>
<span data-ttu-id="03f42-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03f42-118">The resource group name.</span></span>

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

### <span data-ttu-id="03f42-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f42-119">CommonParameters</span></span>
<span data-ttu-id="03f42-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03f42-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f42-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03f42-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f42-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03f42-122">INPUTS</span></span>

### <span data-ttu-id="03f42-123">Brak</span><span class="sxs-lookup"><span data-stu-id="03f42-123">None</span></span>

## <span data-ttu-id="03f42-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="03f42-124">OUTPUTS</span></span>

### <span data-ttu-id="03f42-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="03f42-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="03f42-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03f42-126">NOTES</span></span>

## <span data-ttu-id="03f42-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03f42-127">RELATED LINKS</span></span>
