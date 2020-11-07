---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: a1a134905795123311d1ce0fb89e461678f9f41a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709470"
---
# <span data-ttu-id="5c48a-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c48a-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="5c48a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c48a-102">SYNOPSIS</span></span>
<span data-ttu-id="5c48a-103">Pobiera publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="5c48a-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="5c48a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c48a-104">SYNTAX</span></span>

### <span data-ttu-id="5c48a-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5c48a-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c48a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c48a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c48a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5c48a-107">DESCRIPTION</span></span>
<span data-ttu-id="5c48a-108">Polecenie cmdlet **Get-AzPublicIpPrefix** pobiera co najmniej jeden publiczny prefiks adresów IP w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c48a-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="5c48a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c48a-109">EXAMPLES</span></span>

### <span data-ttu-id="5c48a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c48a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="5c48a-111">To polecenie uzyskuje publiczny zasób prefiksu IP z myPublicIpPrefix1 w grupie zasób myRg</span><span class="sxs-lookup"><span data-stu-id="5c48a-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="5c48a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5c48a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="5c48a-113">To polecenie umożliwia pobieranie wszystkich publicznych zasobów prefiksów IP, które zaczynają się od myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="5c48a-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="5c48a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c48a-114">PARAMETERS</span></span>

### <span data-ttu-id="5c48a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c48a-115">-DefaultProfile</span></span>
<span data-ttu-id="5c48a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c48a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c48a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c48a-117">-Name</span></span>
<span data-ttu-id="5c48a-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c48a-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5c48a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c48a-119">-ResourceGroupName</span></span>
<span data-ttu-id="5c48a-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c48a-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5c48a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c48a-121">-ResourceId</span></span>
<span data-ttu-id="5c48a-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c48a-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c48a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c48a-123">CommonParameters</span></span>
<span data-ttu-id="5c48a-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c48a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c48a-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c48a-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c48a-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c48a-126">INPUTS</span></span>

### <span data-ttu-id="5c48a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5c48a-127">System.String</span></span>

## <span data-ttu-id="5c48a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c48a-128">OUTPUTS</span></span>

### <span data-ttu-id="5c48a-129">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c48a-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="5c48a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c48a-130">NOTES</span></span>

## <span data-ttu-id="5c48a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c48a-131">RELATED LINKS</span></span>

[<span data-ttu-id="5c48a-132">Nowe — AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c48a-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="5c48a-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c48a-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="5c48a-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5c48a-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
