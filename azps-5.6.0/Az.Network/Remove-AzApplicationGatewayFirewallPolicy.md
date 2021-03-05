---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 2d7bdd9a1669859f0bcd650577ed3169a0aeea2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992552"
---
# <span data-ttu-id="cc52f-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cc52f-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="cc52f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc52f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc52f-103">Usuwa zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc52f-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="cc52f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cc52f-104">SYNTAX</span></span>

### <span data-ttu-id="cc52f-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="cc52f-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc52f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cc52f-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc52f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc52f-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc52f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cc52f-108">DESCRIPTION</span></span>
<span data-ttu-id="cc52f-109">Polecenie **cmdlet Remove-AzApplicationGatewayFirewallPolicy** usuwa zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cc52f-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="cc52f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cc52f-110">EXAMPLES</span></span>

### <span data-ttu-id="cc52f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cc52f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cc52f-112">To polecenie usuwa zasady zapory bramy aplikacji o nazwie ApplicationGatewayFirewallPolicy01 w grupie zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="cc52f-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="cc52f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc52f-113">PARAMETERS</span></span>

### <span data-ttu-id="cc52f-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cc52f-114">-AsJob</span></span>
<span data-ttu-id="cc52f-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cc52f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc52f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc52f-116">-DefaultProfile</span></span>
<span data-ttu-id="cc52f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc52f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc52f-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="cc52f-118">-Force</span></span>
<span data-ttu-id="cc52f-119">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cc52f-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cc52f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc52f-120">-InputObject</span></span>
<span data-ttu-id="cc52f-121">Obiekt zasad zapory</span><span class="sxs-lookup"><span data-stu-id="cc52f-121">The firewall policy object</span></span>

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

### <span data-ttu-id="cc52f-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cc52f-122">-Name</span></span>
<span data-ttu-id="cc52f-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cc52f-123">The resource name.</span></span>

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

### <span data-ttu-id="cc52f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc52f-124">-PassThru</span></span>
<span data-ttu-id="cc52f-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="cc52f-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc52f-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cc52f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc52f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc52f-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc52f-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc52f-128">The resource group name.</span></span>

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

### <span data-ttu-id="cc52f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc52f-129">-ResourceId</span></span>
<span data-ttu-id="cc52f-130">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="cc52f-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cc52f-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc52f-131">-Confirm</span></span>
<span data-ttu-id="cc52f-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cc52f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc52f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc52f-133">-WhatIf</span></span>
<span data-ttu-id="cc52f-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc52f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc52f-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cc52f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc52f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc52f-136">CommonParameters</span></span>
<span data-ttu-id="cc52f-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc52f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc52f-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc52f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc52f-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc52f-139">INPUTS</span></span>

### <span data-ttu-id="cc52f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cc52f-140">System.String</span></span>

## <span data-ttu-id="cc52f-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc52f-141">OUTPUTS</span></span>

### <span data-ttu-id="cc52f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc52f-142">System.Boolean</span></span>

## <span data-ttu-id="cc52f-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cc52f-143">NOTES</span></span>

## <span data-ttu-id="cc52f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc52f-144">RELATED LINKS</span></span>
