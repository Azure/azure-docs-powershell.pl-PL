---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333457"
---
# <span data-ttu-id="eeed9-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="eeed9-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="eeed9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eeed9-102">SYNOPSIS</span></span>
<span data-ttu-id="eeed9-103">Usuwa konfigurację wybraną z danego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="eeed9-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="eeed9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eeed9-104">SYNTAX</span></span>

### <span data-ttu-id="eeed9-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eeed9-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeed9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeed9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeed9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeed9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeed9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="eeed9-108">DESCRIPTION</span></span>
<span data-ttu-id="eeed9-109">Polecenie cmdlet **Remove-AzNetworkInterfaceTapConfig** usuwa konfigurację sieci Azure TAP z listy interfejsów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="eeed9-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="eeed9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eeed9-110">EXAMPLES</span></span>

### <span data-ttu-id="eeed9-111">Przykład 1: Usuwanie konfiguracji naciśnięcia</span><span class="sxs-lookup"><span data-stu-id="eeed9-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="eeed9-112">To polecenie usuwa TapConfiguration z NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="eeed9-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="eeed9-113">Ponieważ parametr *Force* nie jest wykorzystywany, użytkownik zostanie poproszony o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="eeed9-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="eeed9-114">Przykład 2: Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="eeed9-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="eeed9-115">To polecenie usuwa TapConfiguration z NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="eeed9-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="eeed9-116">Ponieważ parametr *Force* jest wykorzystywany, użytkownik nie jest monitowany o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eeed9-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="eeed9-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eeed9-117">PARAMETERS</span></span>

### <span data-ttu-id="eeed9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeed9-118">-DefaultProfile</span></span>
<span data-ttu-id="eeed9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eeed9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeed9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="eeed9-120">-Force</span></span>
<span data-ttu-id="eeed9-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eeed9-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eeed9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eeed9-122">-InputObject</span></span>
<span data-ttu-id="eeed9-123">Odwołanie do NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="eeed9-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="eeed9-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eeed9-124">-Name</span></span>
<span data-ttu-id="eeed9-125">Nazwa elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eeed9-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="eeed9-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="eeed9-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="eeed9-127">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="eeed9-127">The virtual network name.</span></span>

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

### <span data-ttu-id="eeed9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eeed9-128">-PassThru</span></span>
<span data-ttu-id="eeed9-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="eeed9-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eeed9-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="eeed9-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eeed9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeed9-131">-ResourceGroupName</span></span>
<span data-ttu-id="eeed9-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eeed9-132">The resource group name.</span></span>

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

### <span data-ttu-id="eeed9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeed9-133">-ResourceId</span></span>
<span data-ttu-id="eeed9-134">Identyfikator zasobu NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="eeed9-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="eeed9-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eeed9-135">-Confirm</span></span>
<span data-ttu-id="eeed9-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeed9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeed9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeed9-137">-WhatIf</span></span>
<span data-ttu-id="eeed9-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeed9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeed9-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eeed9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeed9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeed9-140">CommonParameters</span></span>
<span data-ttu-id="eeed9-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeed9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeed9-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeed9-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeed9-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eeed9-143">INPUTS</span></span>

### <span data-ttu-id="eeed9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="eeed9-144">System.String</span></span>

### <span data-ttu-id="eeed9-145">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeed9-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="eeed9-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eeed9-146">OUTPUTS</span></span>

### <span data-ttu-id="eeed9-147">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="eeed9-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="eeed9-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eeed9-148">NOTES</span></span>

## <span data-ttu-id="eeed9-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eeed9-149">RELATED LINKS</span></span>

[<span data-ttu-id="eeed9-150">Dodaj-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="eeed9-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="eeed9-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="eeed9-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="eeed9-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="eeed9-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
