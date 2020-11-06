---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 32bcc3b83ad34a0f60b01048212d402745934317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554270"
---
# <span data-ttu-id="82632-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82632-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="82632-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82632-102">SYNOPSIS</span></span>
<span data-ttu-id="82632-103">Pobiera grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="82632-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82632-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82632-104">SYNTAX</span></span>

### <span data-ttu-id="82632-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="82632-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82632-106">Większa</span><span class="sxs-lookup"><span data-stu-id="82632-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82632-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82632-107">DESCRIPTION</span></span>
<span data-ttu-id="82632-108">Polecenie cmdlet **Get-AzureRmNetworkSecurityGroup** pobiera grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="82632-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="82632-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82632-109">EXAMPLES</span></span>

### <span data-ttu-id="82632-110">1: pobieranie istniejącej grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="82632-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="82632-111">To polecenie zwraca zawartość grupy zabezpieczeń sieci Azure "nsg1" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="82632-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="82632-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82632-112">PARAMETERS</span></span>

### <span data-ttu-id="82632-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82632-113">-DefaultProfile</span></span>
<span data-ttu-id="82632-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82632-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82632-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="82632-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82632-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82632-116">-Name</span></span>
<span data-ttu-id="82632-117">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet pobiera.</span><span class="sxs-lookup"><span data-stu-id="82632-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82632-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82632-118">-ResourceGroupName</span></span>
<span data-ttu-id="82632-119">Określa nazwę grupy zasobów, do której należy Grupa zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="82632-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82632-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82632-120">CommonParameters</span></span>
<span data-ttu-id="82632-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82632-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82632-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82632-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82632-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82632-123">INPUTS</span></span>

### <span data-ttu-id="82632-124">System. String</span><span class="sxs-lookup"><span data-stu-id="82632-124">System.String</span></span>

## <span data-ttu-id="82632-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82632-125">OUTPUTS</span></span>

### <span data-ttu-id="82632-126">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82632-126">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="82632-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82632-127">NOTES</span></span>

## <span data-ttu-id="82632-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82632-128">RELATED LINKS</span></span>

[<span data-ttu-id="82632-129">Nowe — AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82632-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="82632-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82632-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="82632-131">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="82632-131">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


