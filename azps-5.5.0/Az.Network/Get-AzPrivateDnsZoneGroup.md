---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193754"
---
# <span data-ttu-id="66f68-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="66f68-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="66f68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66f68-102">SYNOPSIS</span></span>
<span data-ttu-id="66f68-103">Pobiera prywatną grupę strefy DNS</span><span class="sxs-lookup"><span data-stu-id="66f68-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="66f68-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="66f68-104">SYNTAX</span></span>

### <span data-ttu-id="66f68-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="66f68-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66f68-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="66f68-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66f68-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="66f68-107">DESCRIPTION</span></span>
<span data-ttu-id="66f68-108">Polecenie **cmdlet Get-AzPrivateDnsZoneGroup** pobiera co najmniej jedną prywatną grupę strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="66f68-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="66f68-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="66f68-109">EXAMPLES</span></span>

### <span data-ttu-id="66f68-110">Przykład 1. Pobieranie prywatnej grupy stref DNS</span><span class="sxs-lookup"><span data-stu-id="66f68-110">Example 1: Retrieve private DNS zone group</span></span>
```powershell
PS C:\> Get-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name "dnsgroup1"
Name                  : dnsgroup1
Id                    : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateEndpoints/test-pr-endpoint/privateDnsZoneGroups/dnsgroup1
ProvisioningState     : Succeeded
PrivateDnsZoneConfigs : [
                          {
                            "Name": "test-vault-azure-com",
                            "PrivateDnsZoneId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg/providers/Microsoft.Network/privateDnsZones/test.vault.azure.com",
                            "RecordSets": []
                          }
                        ]
```

<span data-ttu-id="66f68-111">Powyższy przykład pobiera prywatną grupę strefy DNS o nazwie dnsgroup1 w obszarze rg grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66f68-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="66f68-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66f68-112">PARAMETERS</span></span>

### <span data-ttu-id="66f68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f68-113">-DefaultProfile</span></span>
<span data-ttu-id="66f68-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="66f68-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66f68-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="66f68-115">-Name</span></span>
<span data-ttu-id="66f68-116">Nazwa prywatnej grupy stref DNS.</span><span class="sxs-lookup"><span data-stu-id="66f68-116">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f68-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="66f68-117">-PrivateEndpointName</span></span>
<span data-ttu-id="66f68-118">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="66f68-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f68-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f68-119">-ResourceGroupName</span></span>
<span data-ttu-id="66f68-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="66f68-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f68-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f68-121">CommonParameters</span></span>
<span data-ttu-id="66f68-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66f68-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f68-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66f68-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f68-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66f68-124">INPUTS</span></span>

### <span data-ttu-id="66f68-125">System.String</span><span class="sxs-lookup"><span data-stu-id="66f68-125">System.String</span></span>

## <span data-ttu-id="66f68-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="66f68-126">OUTPUTS</span></span>

### <span data-ttu-id="66f68-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="66f68-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="66f68-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="66f68-128">NOTES</span></span>

## <span data-ttu-id="66f68-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66f68-129">RELATED LINKS</span></span>
