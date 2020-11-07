---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/Remove-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 9833a2e66eb6471efb9aed021af7ae07e8e520c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718807"
---
# <span data-ttu-id="74faa-101">Remove-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="74faa-101">Remove-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="74faa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74faa-102">SYNOPSIS</span></span>
<span data-ttu-id="74faa-103">Usuwa konfigurację wybraną z danego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="74faa-103">Removes a tap configuration from given network interface</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74faa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74faa-104">SYNTAX</span></span>

### <span data-ttu-id="74faa-105">RemoveByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="74faa-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74faa-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74faa-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74faa-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74faa-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74faa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="74faa-108">DESCRIPTION</span></span>
<span data-ttu-id="74faa-109">Polecenie cmdlet **Remove-AzureRmNetworkInterfaceTapConfig** usuwa konfigurację sieci Azure TAP z listy interfejsów sieciowych.</span><span class="sxs-lookup"><span data-stu-id="74faa-109">The **Remove-AzureRmNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="74faa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74faa-110">EXAMPLES</span></span>

### <span data-ttu-id="74faa-111">Przykład 1: Usuwanie konfiguracji naciśnięcia</span><span class="sxs-lookup"><span data-stu-id="74faa-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzureRmNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="74faa-112">To polecenie usuwa TapConfiguration z NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="74faa-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="74faa-113">Ponieważ parametr *Force* nie jest wykorzystywany, użytkownik zostanie poproszony o potwierdzenie tej akcji.</span><span class="sxs-lookup"><span data-stu-id="74faa-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="74faa-114">Przykład 2: Usuwanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="74faa-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzureRmNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="74faa-115">To polecenie usuwa TapConfiguration z NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="74faa-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="74faa-116">Ponieważ parametr *Force* jest wykorzystywany, użytkownik nie jest monitowany o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74faa-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="74faa-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74faa-117">PARAMETERS</span></span>

### <span data-ttu-id="74faa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74faa-118">-DefaultProfile</span></span>
<span data-ttu-id="74faa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74faa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74faa-120">-Force</span><span class="sxs-lookup"><span data-stu-id="74faa-120">-Force</span></span>
<span data-ttu-id="74faa-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74faa-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="74faa-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74faa-122">-InputObject</span></span>
<span data-ttu-id="74faa-123">Odwołanie do NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="74faa-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="74faa-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74faa-124">-Name</span></span>
<span data-ttu-id="74faa-125">Nazwa elementu równorzędnego sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="74faa-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="74faa-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="74faa-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="74faa-127">Nazwa sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="74faa-127">The virtual network name.</span></span>

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

### <span data-ttu-id="74faa-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74faa-128">-PassThru</span></span>
<span data-ttu-id="74faa-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="74faa-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="74faa-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="74faa-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74faa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74faa-131">-ResourceGroupName</span></span>
<span data-ttu-id="74faa-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74faa-132">The resource group name.</span></span>

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

### <span data-ttu-id="74faa-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74faa-133">-ResourceId</span></span>
<span data-ttu-id="74faa-134">Identyfikator zasobu NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="74faa-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="74faa-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74faa-135">-Confirm</span></span>
<span data-ttu-id="74faa-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74faa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74faa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74faa-137">-WhatIf</span></span>
<span data-ttu-id="74faa-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74faa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74faa-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74faa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74faa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74faa-140">CommonParameters</span></span>
<span data-ttu-id="74faa-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74faa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74faa-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74faa-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74faa-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74faa-143">INPUTS</span></span>

### <span data-ttu-id="74faa-144">System. String</span><span class="sxs-lookup"><span data-stu-id="74faa-144">System.String</span></span>

## <span data-ttu-id="74faa-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74faa-145">OUTPUTS</span></span>

### <span data-ttu-id="74faa-146">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="74faa-146">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="74faa-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74faa-147">NOTES</span></span>

## <span data-ttu-id="74faa-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74faa-148">RELATED LINKS</span></span>
