---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
ms.openlocfilehash: 5a9e4f7a4a3d7b8173cf7ef797edfc354d655cc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543636"
---
# <span data-ttu-id="cfc3c-101">Remove-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cfc3c-101">Remove-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="cfc3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc3c-103">Usuwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-103">Removes an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfc3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfc3c-104">SYNTAX</span></span>

### <span data-ttu-id="cfc3c-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cfc3c-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfc3c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfc3c-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfc3c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfc3c-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfc3c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cfc3c-108">DESCRIPTION</span></span>
<span data-ttu-id="cfc3c-109">Polecenie cmdlet **Remove-AzureRmExpressRoutePort** usuwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-109">The **Remove-AzureRmExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="cfc3c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfc3c-110">EXAMPLES</span></span>

### <span data-ttu-id="cfc3c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cfc3c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="cfc3c-112">Usuwa $PortName zasób ExpressRoutePort w $rg grupy zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="cfc3c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cfc3c-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -InputObject $erPort
```
<span data-ttu-id="cfc3c-114">Usuwa zasób ExpressRoutePort w polu Inputobject.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="cfc3c-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cfc3c-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="cfc3c-116">Usuwa zasób ExpressRoutePort o identyfikatorze ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="cfc3c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfc3c-117">PARAMETERS</span></span>

### <span data-ttu-id="cfc3c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfc3c-118">-AsJob</span></span>
<span data-ttu-id="cfc3c-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cfc3c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfc3c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc3c-120">-DefaultProfile</span></span>
<span data-ttu-id="cfc3c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfc3c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cfc3c-122">-Force</span></span>
<span data-ttu-id="cfc3c-123">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="cfc3c-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="cfc3c-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cfc3c-124">-InputObject</span></span>
<span data-ttu-id="cfc3c-125">Obiekt port routingu Express</span><span class="sxs-lookup"><span data-stu-id="cfc3c-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc3c-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfc3c-126">-Name</span></span>
<span data-ttu-id="cfc3c-127">Nazwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc3c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfc3c-128">-PassThru</span></span>
<span data-ttu-id="cfc3c-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="cfc3c-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cfc3c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfc3c-131">-ResourceGroupName</span></span>
<span data-ttu-id="cfc3c-132">Nazwa grupy zasobów ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc3c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfc3c-133">-ResourceId</span></span>
<span data-ttu-id="cfc3c-134">Identyfikator zasobu Express Route port.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc3c-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cfc3c-135">-Confirm</span></span>
<span data-ttu-id="cfc3c-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfc3c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfc3c-137">-WhatIf</span></span>
<span data-ttu-id="cfc3c-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfc3c-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfc3c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc3c-140">CommonParameters</span></span>
<span data-ttu-id="cfc3c-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc3c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc3c-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfc3c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc3c-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfc3c-143">INPUTS</span></span>

### <span data-ttu-id="cfc3c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="cfc3c-144">System.String</span></span>

### <span data-ttu-id="cfc3c-145">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="cfc3c-145">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="cfc3c-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfc3c-146">OUTPUTS</span></span>

### <span data-ttu-id="cfc3c-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="cfc3c-147">System.Object</span></span>
## <span data-ttu-id="cfc3c-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfc3c-148">NOTES</span></span>

## <span data-ttu-id="cfc3c-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfc3c-149">RELATED LINKS</span></span>
