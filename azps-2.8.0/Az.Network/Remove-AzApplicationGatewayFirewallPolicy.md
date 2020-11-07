---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 58800beae60292029a7a9b3245f274355c887a5b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871295"
---
# <span data-ttu-id="2adf5-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2adf5-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="2adf5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2adf5-102">SYNOPSIS</span></span>
<span data-ttu-id="2adf5-103">Usuwa zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2adf5-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="2adf5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2adf5-104">SYNTAX</span></span>

### <span data-ttu-id="2adf5-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2adf5-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2adf5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2adf5-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2adf5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2adf5-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2adf5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2adf5-108">DESCRIPTION</span></span>
<span data-ttu-id="2adf5-109">Polecenie cmdlet **Remove-AzApplicationGatewayFirewallPolicy** usuwa zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2adf5-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="2adf5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2adf5-110">EXAMPLES</span></span>

### <span data-ttu-id="2adf5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2adf5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2adf5-112">To polecenie usuwa zasady zapory bramy aplikacji o nazwie ApplicationGatewayFirewallPolicy01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2adf5-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="2adf5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2adf5-113">PARAMETERS</span></span>

### <span data-ttu-id="2adf5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2adf5-114">-AsJob</span></span>
<span data-ttu-id="2adf5-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2adf5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2adf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2adf5-116">-DefaultProfile</span></span>
<span data-ttu-id="2adf5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2adf5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2adf5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2adf5-118">-Force</span></span>
<span data-ttu-id="2adf5-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2adf5-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2adf5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2adf5-120">-InputObject</span></span>
<span data-ttu-id="2adf5-121">Obiekt zasady zapory</span><span class="sxs-lookup"><span data-stu-id="2adf5-121">The firewall policy object</span></span>

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

### <span data-ttu-id="2adf5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2adf5-122">-Name</span></span>
<span data-ttu-id="2adf5-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="2adf5-123">The resource name.</span></span>

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

### <span data-ttu-id="2adf5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2adf5-124">-PassThru</span></span>
<span data-ttu-id="2adf5-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2adf5-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2adf5-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2adf5-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2adf5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2adf5-127">-ResourceGroupName</span></span>
<span data-ttu-id="2adf5-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2adf5-128">The resource group name.</span></span>

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

### <span data-ttu-id="2adf5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2adf5-129">-ResourceId</span></span>
<span data-ttu-id="2adf5-130">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2adf5-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2adf5-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2adf5-131">-Confirm</span></span>
<span data-ttu-id="2adf5-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2adf5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2adf5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2adf5-133">-WhatIf</span></span>
<span data-ttu-id="2adf5-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2adf5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2adf5-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2adf5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2adf5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2adf5-136">CommonParameters</span></span>
<span data-ttu-id="2adf5-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2adf5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2adf5-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2adf5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2adf5-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2adf5-139">INPUTS</span></span>

### <span data-ttu-id="2adf5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2adf5-140">System.String</span></span>

## <span data-ttu-id="2adf5-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2adf5-141">OUTPUTS</span></span>

### <span data-ttu-id="2adf5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2adf5-142">System.Boolean</span></span>

## <span data-ttu-id="2adf5-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2adf5-143">NOTES</span></span>

## <span data-ttu-id="2adf5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2adf5-144">RELATED LINKS</span></span>
