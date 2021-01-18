---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: dc90facde7d79b308ff456be9f2df1b8c087a4a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504479"
---
# <span data-ttu-id="5d20f-101">Get-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="5d20f-101">Get-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="5d20f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d20f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d20f-103">Pobiera grupę prywatnych stref DNS</span><span class="sxs-lookup"><span data-stu-id="5d20f-103">Gets private DNS zone group</span></span>

## <span data-ttu-id="5d20f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d20f-104">SYNTAX</span></span>

### <span data-ttu-id="5d20f-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="5d20f-105">List (Default)</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d20f-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="5d20f-106">GetByName</span></span>
```
Get-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d20f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5d20f-107">DESCRIPTION</span></span>
<span data-ttu-id="5d20f-108">Polecenie cmdlet **Get-AzPrivateDnsZoneGroup umożliwia pobranie** jednej lub wielu prywatnych grup stref DNS.</span><span class="sxs-lookup"><span data-stu-id="5d20f-108">The **Get-AzPrivateDnsZoneGroup** cmdlet gets one or more private DNS zone groups.</span></span>

## <span data-ttu-id="5d20f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d20f-109">EXAMPLES</span></span>

### <span data-ttu-id="5d20f-110">Przykład 1: pobieranie grupy prywatnych stref DNS</span><span class="sxs-lookup"><span data-stu-id="5d20f-110">Example 1: Retrieve private DNS zone group</span></span>
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

<span data-ttu-id="5d20f-111">Powyższy przykład pobiera prywatną grupę DNS o nazwie dnsgroup1 w RG Group (zasób).</span><span class="sxs-lookup"><span data-stu-id="5d20f-111">Above example gets a private DNS zone group named dnsgroup1 in the resource group rg.</span></span>

## <span data-ttu-id="5d20f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d20f-112">PARAMETERS</span></span>

### <span data-ttu-id="5d20f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d20f-113">-DefaultProfile</span></span>
<span data-ttu-id="5d20f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d20f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d20f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d20f-115">-Name</span></span>
<span data-ttu-id="5d20f-116">Nazwa grupy prywatna strefa DNS.</span><span class="sxs-lookup"><span data-stu-id="5d20f-116">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="5d20f-117">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="5d20f-117">-PrivateEndpointName</span></span>
<span data-ttu-id="5d20f-118">Nazwa prywatnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="5d20f-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="5d20f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d20f-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d20f-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d20f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d20f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d20f-121">CommonParameters</span></span>
<span data-ttu-id="5d20f-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d20f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d20f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d20f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d20f-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d20f-124">INPUTS</span></span>

### <span data-ttu-id="5d20f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5d20f-125">System.String</span></span>

## <span data-ttu-id="5d20f-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d20f-126">OUTPUTS</span></span>

### <span data-ttu-id="5d20f-127">Microsoft. Azure. Commands. Network. models. PSPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="5d20f-127">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="5d20f-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d20f-128">NOTES</span></span>

## <span data-ttu-id="5d20f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d20f-129">RELATED LINKS</span></span>
