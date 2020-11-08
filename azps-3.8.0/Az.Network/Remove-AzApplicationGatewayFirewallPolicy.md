---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051008"
---
# <span data-ttu-id="8bee3-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8bee3-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="8bee3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8bee3-102">SYNOPSIS</span></span>
<span data-ttu-id="8bee3-103">Usuwa zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8bee3-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="8bee3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8bee3-104">SYNTAX</span></span>

### <span data-ttu-id="8bee3-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8bee3-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bee3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8bee3-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bee3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8bee3-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bee3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8bee3-108">DESCRIPTION</span></span>
<span data-ttu-id="8bee3-109">Polecenie cmdlet **Remove-AzApplicationGatewayFirewallPolicy** usuwa zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8bee3-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="8bee3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8bee3-110">EXAMPLES</span></span>

### <span data-ttu-id="8bee3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8bee3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8bee3-112">To polecenie usuwa zasady zapory bramy aplikacji o nazwie ApplicationGatewayFirewallPolicy01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8bee3-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="8bee3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8bee3-113">PARAMETERS</span></span>

### <span data-ttu-id="8bee3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bee3-114">-AsJob</span></span>
<span data-ttu-id="8bee3-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8bee3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8bee3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bee3-116">-DefaultProfile</span></span>
<span data-ttu-id="8bee3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8bee3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bee3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8bee3-118">-Force</span></span>
<span data-ttu-id="8bee3-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8bee3-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8bee3-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8bee3-120">-InputObject</span></span>
<span data-ttu-id="8bee3-121">Obiekt zasady zapory</span><span class="sxs-lookup"><span data-stu-id="8bee3-121">The firewall policy object</span></span>

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

### <span data-ttu-id="8bee3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8bee3-122">-Name</span></span>
<span data-ttu-id="8bee3-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8bee3-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bee3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bee3-124">-PassThru</span></span>
<span data-ttu-id="8bee3-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="8bee3-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8bee3-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8bee3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8bee3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bee3-127">-ResourceGroupName</span></span>
<span data-ttu-id="8bee3-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8bee3-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bee3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bee3-129">-ResourceId</span></span>
<span data-ttu-id="8bee3-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8bee3-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8bee3-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8bee3-131">-Confirm</span></span>
<span data-ttu-id="8bee3-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bee3-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bee3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bee3-133">-WhatIf</span></span>
<span data-ttu-id="8bee3-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bee3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bee3-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8bee3-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bee3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bee3-136">CommonParameters</span></span>
<span data-ttu-id="8bee3-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bee3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bee3-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bee3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bee3-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8bee3-139">INPUTS</span></span>

### <span data-ttu-id="8bee3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8bee3-140">System.String</span></span>

## <span data-ttu-id="8bee3-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8bee3-141">OUTPUTS</span></span>

### <span data-ttu-id="8bee3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8bee3-142">System.Boolean</span></span>

## <span data-ttu-id="8bee3-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8bee3-143">NOTES</span></span>

## <span data-ttu-id="8bee3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8bee3-144">RELATED LINKS</span></span>
