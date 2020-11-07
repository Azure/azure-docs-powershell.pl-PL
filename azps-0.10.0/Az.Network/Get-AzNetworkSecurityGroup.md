---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: beb2b723a0b72f7ab485846f6f55fabd4e6ef9aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890754"
---
# <span data-ttu-id="b1469-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1469-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="b1469-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1469-102">SYNOPSIS</span></span>
<span data-ttu-id="b1469-103">Pobiera grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b1469-103">Gets a network security group.</span></span>

## <span data-ttu-id="b1469-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1469-104">SYNTAX</span></span>

### <span data-ttu-id="b1469-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="b1469-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1469-106">Większa</span><span class="sxs-lookup"><span data-stu-id="b1469-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1469-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b1469-107">DESCRIPTION</span></span>
<span data-ttu-id="b1469-108">Polecenie cmdlet **Get-AzNetworkSecurityGroup** pobiera grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="b1469-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="b1469-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1469-109">EXAMPLES</span></span>

### <span data-ttu-id="b1469-110">1: pobieranie istniejącej grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="b1469-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="b1469-111">To polecenie zwraca zawartość grupy zabezpieczeń sieci Azure "nsg1" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="b1469-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="b1469-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1469-112">PARAMETERS</span></span>

### <span data-ttu-id="b1469-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1469-113">-DefaultProfile</span></span>
<span data-ttu-id="b1469-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1469-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1469-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b1469-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1469-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b1469-116">-Name</span></span>
<span data-ttu-id="b1469-117">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet pobiera.</span><span class="sxs-lookup"><span data-stu-id="b1469-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1469-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1469-118">-ResourceGroupName</span></span>
<span data-ttu-id="b1469-119">Określa nazwę grupy zasobów, do której należy Grupa zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b1469-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1469-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1469-120">CommonParameters</span></span>
<span data-ttu-id="b1469-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1469-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1469-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1469-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1469-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1469-123">INPUTS</span></span>

## <span data-ttu-id="b1469-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1469-124">OUTPUTS</span></span>

### <span data-ttu-id="b1469-125">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1469-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b1469-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1469-126">NOTES</span></span>

## <span data-ttu-id="b1469-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1469-127">RELATED LINKS</span></span>

[<span data-ttu-id="b1469-128">Nowe — AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1469-128">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="b1469-129">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1469-129">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="b1469-130">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b1469-130">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


