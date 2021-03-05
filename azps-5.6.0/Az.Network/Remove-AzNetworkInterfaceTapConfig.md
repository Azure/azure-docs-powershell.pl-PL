---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 54468717f979188d31d6ba318556be87c37e50b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993637"
---
# <span data-ttu-id="279fc-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="279fc-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="279fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="279fc-102">SYNOPSIS</span></span>
<span data-ttu-id="279fc-103">Usuwa konfigurację naciśnięcia z danego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="279fc-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="279fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="279fc-104">SYNTAX</span></span>

### <span data-ttu-id="279fc-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="279fc-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279fc-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="279fc-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="279fc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="279fc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="279fc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="279fc-108">DESCRIPTION</span></span>
<span data-ttu-id="279fc-109">Polecenie **cmdlet Remove-AzNetworkInterfaceTapConfig** usuwa konfigurację usługi Azure Tap z listy interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="279fc-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="279fc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="279fc-110">EXAMPLES</span></span>

### <span data-ttu-id="279fc-111">Przykład 1. Usuwanie konfiguracji naciśnięcia</span><span class="sxs-lookup"><span data-stu-id="279fc-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="279fc-112">To polecenie usuwa konfigurację TapConfiguration z kroju NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="279fc-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="279fc-113">Ponieważ parametr *Force* nie jest używany, użytkownik zostanie wyświetlony monit o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="279fc-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="279fc-114">Przykład 2. Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="279fc-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="279fc-115">To polecenie usuwa konfigurację TapConfiguration z kroju NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="279fc-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="279fc-116">Parametr *Force jest* używany, dlatego użytkownik nie jest monitowany o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="279fc-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="279fc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="279fc-117">PARAMETERS</span></span>

### <span data-ttu-id="279fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="279fc-118">-DefaultProfile</span></span>
<span data-ttu-id="279fc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="279fc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="279fc-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="279fc-120">-Force</span></span>
<span data-ttu-id="279fc-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="279fc-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="279fc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="279fc-122">-InputObject</span></span>
<span data-ttu-id="279fc-123">Odwołanie do pliku NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="279fc-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="279fc-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="279fc-124">-Name</span></span>
<span data-ttu-id="279fc-125">Nazwa komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="279fc-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279fc-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="279fc-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="279fc-127">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="279fc-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279fc-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="279fc-128">-PassThru</span></span>
<span data-ttu-id="279fc-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="279fc-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="279fc-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="279fc-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="279fc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="279fc-131">-ResourceGroupName</span></span>
<span data-ttu-id="279fc-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="279fc-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279fc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="279fc-133">-ResourceId</span></span>
<span data-ttu-id="279fc-134">Identyfikator zasobu NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="279fc-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="279fc-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="279fc-135">-Confirm</span></span>
<span data-ttu-id="279fc-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="279fc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="279fc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="279fc-137">-WhatIf</span></span>
<span data-ttu-id="279fc-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="279fc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="279fc-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="279fc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="279fc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="279fc-140">CommonParameters</span></span>
<span data-ttu-id="279fc-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="279fc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="279fc-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="279fc-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="279fc-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="279fc-143">INPUTS</span></span>

### <span data-ttu-id="279fc-144">System.String</span><span class="sxs-lookup"><span data-stu-id="279fc-144">System.String</span></span>

### <span data-ttu-id="279fc-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="279fc-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="279fc-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="279fc-146">OUTPUTS</span></span>

### <span data-ttu-id="279fc-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="279fc-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="279fc-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="279fc-148">NOTES</span></span>

## <span data-ttu-id="279fc-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="279fc-149">RELATED LINKS</span></span>

[<span data-ttu-id="279fc-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="279fc-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="279fc-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="279fc-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="279fc-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="279fc-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
