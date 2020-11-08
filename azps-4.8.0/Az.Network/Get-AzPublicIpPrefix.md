---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 35e6496cf8dbbcc9bb183bef2e8c83f7fba4a9b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219510"
---
# <span data-ttu-id="c62dc-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c62dc-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="c62dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c62dc-102">SYNOPSIS</span></span>
<span data-ttu-id="c62dc-103">Pobiera publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="c62dc-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="c62dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c62dc-104">SYNTAX</span></span>

### <span data-ttu-id="c62dc-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c62dc-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c62dc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c62dc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c62dc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c62dc-107">DESCRIPTION</span></span>
<span data-ttu-id="c62dc-108">Polecenie cmdlet **Get-AzPublicIpPrefix** pobiera co najmniej jeden publiczny prefiks adresów IP w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c62dc-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="c62dc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c62dc-109">EXAMPLES</span></span>

### <span data-ttu-id="c62dc-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c62dc-110">Example 1</span></span>
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

<span data-ttu-id="c62dc-111">To polecenie uzyskuje publiczny zasób prefiksu IP z myPublicIpPrefix1 w grupie zasób myRg</span><span class="sxs-lookup"><span data-stu-id="c62dc-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="c62dc-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c62dc-112">Example 2</span></span>
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

<span data-ttu-id="c62dc-113">To polecenie umożliwia pobieranie wszystkich publicznych zasobów prefiksów IP, które zaczynają się od myPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="c62dc-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="c62dc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c62dc-114">PARAMETERS</span></span>

### <span data-ttu-id="c62dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c62dc-115">-DefaultProfile</span></span>
<span data-ttu-id="c62dc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c62dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c62dc-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c62dc-117">-Name</span></span>
<span data-ttu-id="c62dc-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="c62dc-118">The resource name.</span></span>

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

### <span data-ttu-id="c62dc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c62dc-119">-ResourceGroupName</span></span>
<span data-ttu-id="c62dc-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c62dc-120">The resource group name.</span></span>

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

### <span data-ttu-id="c62dc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c62dc-121">-ResourceId</span></span>
<span data-ttu-id="c62dc-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c62dc-122">The resource Id.</span></span>

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

### <span data-ttu-id="c62dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62dc-123">CommonParameters</span></span>
<span data-ttu-id="c62dc-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c62dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62dc-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c62dc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62dc-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c62dc-126">INPUTS</span></span>

### <span data-ttu-id="c62dc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c62dc-127">System.String</span></span>

## <span data-ttu-id="c62dc-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c62dc-128">OUTPUTS</span></span>

### <span data-ttu-id="c62dc-129">Microsoft. Azure. Commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c62dc-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="c62dc-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c62dc-130">NOTES</span></span>

## <span data-ttu-id="c62dc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c62dc-131">RELATED LINKS</span></span>

[<span data-ttu-id="c62dc-132">Nowe — AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c62dc-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="c62dc-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c62dc-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="c62dc-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c62dc-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
