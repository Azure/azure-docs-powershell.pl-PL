---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202455"
---
# <span data-ttu-id="41308-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="41308-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="41308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41308-102">SYNOPSIS</span></span>
<span data-ttu-id="41308-103">Zaktualizuj zasób bramy nat przy użyciu publicznego adresu IP, publicznego prefiksu IP i idleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="41308-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="41308-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="41308-104">SYNTAX</span></span>

### <span data-ttu-id="41308-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="41308-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41308-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41308-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41308-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41308-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41308-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="41308-108">DESCRIPTION</span></span>
<span data-ttu-id="41308-109">Zaktualizuj zasób bramy nat przy użyciu publicznego adresu IP, publicznego prefiksu IP i idleTimeoutInMinutes.</span><span class="sxs-lookup"><span data-stu-id="41308-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="41308-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="41308-110">EXAMPLES</span></span>

### <span data-ttu-id="41308-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41308-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="41308-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41308-112">PARAMETERS</span></span>

### <span data-ttu-id="41308-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="41308-113">-AsJob</span></span>
<span data-ttu-id="41308-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="41308-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41308-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41308-115">-DefaultProfile</span></span>
<span data-ttu-id="41308-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="41308-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41308-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="41308-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="41308-118">Limit czasu bezczynności bramy nat.</span><span class="sxs-lookup"><span data-stu-id="41308-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41308-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41308-119">-InputObject</span></span>
<span data-ttu-id="41308-120">Określa zasób bramy nat.</span><span class="sxs-lookup"><span data-stu-id="41308-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41308-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="41308-121">-Name</span></span>
<span data-ttu-id="41308-122">Nazwa zasobu bramy nat.</span><span class="sxs-lookup"><span data-stu-id="41308-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41308-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="41308-123">-PublicIpAddress</span></span>
<span data-ttu-id="41308-124">Tablica publicznych adresów IP skojarzonych z zasobem bramy nat.</span><span class="sxs-lookup"><span data-stu-id="41308-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41308-125">- PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="41308-125">-PublicIpPrefix</span></span>
<span data-ttu-id="41308-126">Tablica publicznych prefiksów IP skojarzonych z zasobem bramy nat.</span><span class="sxs-lookup"><span data-stu-id="41308-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41308-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41308-127">-ResourceGroupName</span></span>
<span data-ttu-id="41308-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41308-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41308-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41308-129">-ResourceId</span></span>
<span data-ttu-id="41308-130">Określa identyfikator zasobu Brama nat.</span><span class="sxs-lookup"><span data-stu-id="41308-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41308-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41308-131">-Confirm</span></span>
<span data-ttu-id="41308-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="41308-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41308-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41308-133">-WhatIf</span></span>
<span data-ttu-id="41308-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41308-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41308-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="41308-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41308-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41308-136">CommonParameters</span></span>
<span data-ttu-id="41308-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41308-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41308-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41308-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41308-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41308-139">INPUTS</span></span>

### <span data-ttu-id="41308-140">System.String</span><span class="sxs-lookup"><span data-stu-id="41308-140">System.String</span></span>

### <span data-ttu-id="41308-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="41308-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="41308-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41308-142">OUTPUTS</span></span>

### <span data-ttu-id="41308-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="41308-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="41308-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="41308-144">NOTES</span></span>

## <span data-ttu-id="41308-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41308-145">RELATED LINKS</span></span>
