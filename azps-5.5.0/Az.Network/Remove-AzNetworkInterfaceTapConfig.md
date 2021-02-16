---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179482"
---
# <span data-ttu-id="c56a0-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c56a0-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="c56a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c56a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c56a0-103">Usuwa konfigurację naciśnięcia z danego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c56a0-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="c56a0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c56a0-104">SYNTAX</span></span>

### <span data-ttu-id="c56a0-105">RemoveByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c56a0-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c56a0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c56a0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c56a0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c56a0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c56a0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c56a0-108">DESCRIPTION</span></span>
<span data-ttu-id="c56a0-109">Polecenie **cmdlet Remove-AzNetworkInterfaceTapConfig** usuwa konfigurację usługi Azure Tap z listy interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c56a0-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="c56a0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c56a0-110">EXAMPLES</span></span>

### <span data-ttu-id="c56a0-111">Przykład 1. Usuwanie konfiguracji naciśnięcia</span><span class="sxs-lookup"><span data-stu-id="c56a0-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="c56a0-112">To polecenie usuwa konfigurację TapConfiguration z kroju NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="c56a0-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="c56a0-113">Ponieważ parametr *Force* nie jest używany, użytkownik zostanie wyświetlony monit o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="c56a0-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="c56a0-114">Przykład 2. Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="c56a0-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="c56a0-115">To polecenie usuwa konfigurację TapConfiguration z kroju NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="c56a0-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="c56a0-116">Parametr *Force jest* używany, dlatego użytkownik nie jest monitowany o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c56a0-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="c56a0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c56a0-117">PARAMETERS</span></span>

### <span data-ttu-id="c56a0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56a0-118">-DefaultProfile</span></span>
<span data-ttu-id="c56a0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c56a0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c56a0-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c56a0-120">-Force</span></span>
<span data-ttu-id="c56a0-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c56a0-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c56a0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c56a0-122">-InputObject</span></span>
<span data-ttu-id="c56a0-123">Odwołanie do pliku NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="c56a0-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="c56a0-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c56a0-124">-Name</span></span>
<span data-ttu-id="c56a0-125">Nazwa komunikacji równorzędnej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c56a0-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="c56a0-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="c56a0-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="c56a0-127">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c56a0-127">The virtual network name.</span></span>

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

### <span data-ttu-id="c56a0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c56a0-128">-PassThru</span></span>
<span data-ttu-id="c56a0-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c56a0-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c56a0-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c56a0-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c56a0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c56a0-131">-ResourceGroupName</span></span>
<span data-ttu-id="c56a0-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c56a0-132">The resource group name.</span></span>

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

### <span data-ttu-id="c56a0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c56a0-133">-ResourceId</span></span>
<span data-ttu-id="c56a0-134">Identyfikator zasobu NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="c56a0-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="c56a0-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c56a0-135">-Confirm</span></span>
<span data-ttu-id="c56a0-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c56a0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c56a0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56a0-137">-WhatIf</span></span>
<span data-ttu-id="c56a0-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c56a0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c56a0-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c56a0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c56a0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56a0-140">CommonParameters</span></span>
<span data-ttu-id="c56a0-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c56a0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56a0-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c56a0-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56a0-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c56a0-143">INPUTS</span></span>

### <span data-ttu-id="c56a0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c56a0-144">System.String</span></span>

### <span data-ttu-id="c56a0-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="c56a0-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="c56a0-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c56a0-146">OUTPUTS</span></span>

### <span data-ttu-id="c56a0-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c56a0-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c56a0-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c56a0-148">NOTES</span></span>

## <span data-ttu-id="c56a0-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c56a0-149">RELATED LINKS</span></span>

[<span data-ttu-id="c56a0-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c56a0-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="c56a0-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c56a0-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="c56a0-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c56a0-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
