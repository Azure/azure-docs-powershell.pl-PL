---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869612"
---
# <span data-ttu-id="de358-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="de358-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="de358-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de358-102">SYNOPSIS</span></span>
<span data-ttu-id="de358-103">Aktualizuje zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="de358-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="de358-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de358-104">SYNTAX</span></span>

### <span data-ttu-id="de358-105">ByFactoryObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de358-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de358-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="de358-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de358-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="de358-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de358-108">Opis</span><span class="sxs-lookup"><span data-stu-id="de358-108">DESCRIPTION</span></span>
<span data-ttu-id="de358-109">Polecenie cmdlet **Set-AzApplicationGatewayFirewallPolicy** aktualizuje zasady zapory Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="de358-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="de358-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de358-110">EXAMPLES</span></span>

### <span data-ttu-id="de358-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de358-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="de358-112">To polecenie aktualizuje zasady zapory bramy aplikacji za pomocą ustawień w zmiennej $AppGwFirewallPolicy i przechowuje zaktualizowaną bramę w zmiennej $UpdatedAppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="de358-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="de358-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de358-113">PARAMETERS</span></span>

### <span data-ttu-id="de358-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de358-114">-AsJob</span></span>
<span data-ttu-id="de358-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="de358-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de358-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="de358-116">-CustomRule</span></span>
<span data-ttu-id="de358-117">Lista CustomRules</span><span class="sxs-lookup"><span data-stu-id="de358-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de358-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de358-118">-DefaultProfile</span></span>
<span data-ttu-id="de358-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de358-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de358-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="de358-120">-InputObject</span></span>
<span data-ttu-id="de358-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="de358-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de358-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de358-122">-Name</span></span>
<span data-ttu-id="de358-123">Nazwa zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="de358-123">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de358-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de358-124">-ResourceGroupName</span></span>
<span data-ttu-id="de358-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="de358-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de358-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de358-126">-ResourceId</span></span>
<span data-ttu-id="de358-127">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="de358-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de358-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de358-128">CommonParameters</span></span>
<span data-ttu-id="de358-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de358-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de358-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de358-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de358-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de358-131">INPUTS</span></span>

### <span data-ttu-id="de358-132">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="de358-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="de358-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de358-133">OUTPUTS</span></span>

### <span data-ttu-id="de358-134">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="de358-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="de358-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de358-135">NOTES</span></span>

## <span data-ttu-id="de358-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de358-136">RELATED LINKS</span></span>
