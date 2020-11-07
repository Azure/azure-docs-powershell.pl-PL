---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 5a1c519bd545ecb750f3842dac490eb31703e4d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717489"
---
# <span data-ttu-id="90113-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="90113-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="90113-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90113-102">SYNOPSIS</span></span>
<span data-ttu-id="90113-103">Pobiera grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="90113-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90113-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90113-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90113-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90113-105">DESCRIPTION</span></span>
<span data-ttu-id="90113-106">Polecenie cmdlet **Get-AzureRmApplicationSecurityGroup** pobiera grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="90113-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="90113-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90113-107">EXAMPLES</span></span>

### <span data-ttu-id="90113-108">Przykład 1: pobieranie wszystkich grup zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="90113-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="90113-109">Powyższe polecenie zwraca wszystkie grupy zabezpieczeń aplikacji w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="90113-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="90113-110">Przykład 2: pobieranie grup zabezpieczeń aplikacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="90113-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="90113-111">Powyższe polecenie zwraca wszystkie grupy zabezpieczeń aplikacji należące do grupy moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="90113-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="90113-112">Przykład 3: pobieranie określonej grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="90113-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="90113-113">Powyższe polecenie zwraca grupę zabezpieczeń aplikacji MyApplicationSecurityGroup pod grupą zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="90113-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="90113-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90113-114">PARAMETERS</span></span>

### <span data-ttu-id="90113-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90113-115">-DefaultProfile</span></span>
<span data-ttu-id="90113-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90113-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90113-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90113-117">-Name</span></span>
<span data-ttu-id="90113-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="90113-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90113-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90113-119">-ResourceGroupName</span></span>
<span data-ttu-id="90113-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="90113-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90113-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90113-121">CommonParameters</span></span>
<span data-ttu-id="90113-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90113-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90113-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90113-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90113-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90113-124">INPUTS</span></span>

### <span data-ttu-id="90113-125">System. String</span><span class="sxs-lookup"><span data-stu-id="90113-125">System.String</span></span>

## <span data-ttu-id="90113-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90113-126">OUTPUTS</span></span>

### <span data-ttu-id="90113-127">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="90113-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="90113-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90113-128">NOTES</span></span>

## <span data-ttu-id="90113-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90113-129">RELATED LINKS</span></span>

[<span data-ttu-id="90113-130">Nowe — AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="90113-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="90113-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="90113-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="90113-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="90113-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="90113-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="90113-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
