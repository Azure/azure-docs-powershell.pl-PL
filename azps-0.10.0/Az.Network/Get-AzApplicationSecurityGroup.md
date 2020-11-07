---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: b23901a79262f4eb63e34b99c10b82442cb2fe6a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890838"
---
# <span data-ttu-id="65e78-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65e78-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="65e78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65e78-102">SYNOPSIS</span></span>
<span data-ttu-id="65e78-103">Pobiera grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="65e78-103">Gets an application security group.</span></span>

## <span data-ttu-id="65e78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65e78-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65e78-105">Opis</span><span class="sxs-lookup"><span data-stu-id="65e78-105">DESCRIPTION</span></span>
<span data-ttu-id="65e78-106">Polecenie cmdlet **Get-AzApplicationSecurityGroup** pobiera grupę zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="65e78-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="65e78-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65e78-107">EXAMPLES</span></span>

### <span data-ttu-id="65e78-108">Przykład 1: pobieranie wszystkich grup zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="65e78-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup
```

<span data-ttu-id="65e78-109">Powyższe polecenie zwraca wszystkie grupy zabezpieczeń aplikacji w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="65e78-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="65e78-110">Przykład 2: pobieranie grup zabezpieczeń aplikacji w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="65e78-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="65e78-111">Powyższe polecenie zwraca wszystkie grupy zabezpieczeń aplikacji należące do grupy moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="65e78-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="65e78-112">Przykład 3: pobieranie określonej grupy zabezpieczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="65e78-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="65e78-113">Powyższe polecenie zwraca grupę zabezpieczeń aplikacji MyApplicationSecurityGroup pod grupą zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="65e78-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="65e78-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65e78-114">PARAMETERS</span></span>

### <span data-ttu-id="65e78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e78-115">-DefaultProfile</span></span>
<span data-ttu-id="65e78-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65e78-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65e78-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65e78-117">-Name</span></span>
<span data-ttu-id="65e78-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="65e78-118">The resource name.</span></span>

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

### <span data-ttu-id="65e78-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e78-119">-ResourceGroupName</span></span>
<span data-ttu-id="65e78-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65e78-120">The resource group name.</span></span>

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

### <span data-ttu-id="65e78-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e78-121">CommonParameters</span></span>
<span data-ttu-id="65e78-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e78-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e78-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e78-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e78-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65e78-124">INPUTS</span></span>

### <span data-ttu-id="65e78-125">System. String</span><span class="sxs-lookup"><span data-stu-id="65e78-125">System.String</span></span>

## <span data-ttu-id="65e78-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65e78-126">OUTPUTS</span></span>

### <span data-ttu-id="65e78-127">Microsoft. Azure. Commands. Network. models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65e78-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="65e78-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65e78-128">NOTES</span></span>

## <span data-ttu-id="65e78-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65e78-129">RELATED LINKS</span></span>

[<span data-ttu-id="65e78-130">Nowe — AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65e78-130">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="65e78-131">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="65e78-131">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="65e78-132">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65e78-132">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="65e78-133">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="65e78-133">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
