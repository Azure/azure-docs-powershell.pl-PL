---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179874"
---
# <span data-ttu-id="75823-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="75823-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="75823-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75823-102">SYNOPSIS</span></span>
<span data-ttu-id="75823-103">Pobiera zasób konfiguracji naciśnięcia.</span><span class="sxs-lookup"><span data-stu-id="75823-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="75823-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75823-104">SYNTAX</span></span>

### <span data-ttu-id="75823-105">GetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="75823-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75823-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75823-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75823-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="75823-107">DESCRIPTION</span></span>
<span data-ttu-id="75823-108">Polecenie **cmdlet Get-AzNetworkInterfaceTapConfig** pobiera konfigurację usługi Azure Tap Configuration dla danej grupy zasobów, interfejsu sieciowego i nazwę konfiguracji naciśnij lub listę konfiguracji naciśnięcia w grupie zasobów i interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="75823-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="75823-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75823-109">EXAMPLES</span></span>

### <span data-ttu-id="75823-110">Przykład 1. Uzyskiwanie wszystkich konfiguracji naciśnięcia dla danego interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="75823-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="75823-111">To polecenie pobiera konfiguracje naciśnięcia dodane dla danego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="75823-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="75823-112">Przykład 2. Uzyskiwanie konfiguracji naciśnięcia</span><span class="sxs-lookup"><span data-stu-id="75823-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="75823-113">To polecenie pobiera określoną konfigurację naciśnięcia dodaną dla danego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="75823-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="75823-114">Przykład 3. Uzyskiwanie konfiguracji naciśnięcia</span><span class="sxs-lookup"><span data-stu-id="75823-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="75823-115">To polecenie pobiera konfiguracje naciśnięcia dodane dla danego interfejsu sieciowego o nazwie zaczynającej się od "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="75823-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="75823-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75823-116">PARAMETERS</span></span>

### <span data-ttu-id="75823-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75823-117">-DefaultProfile</span></span>
<span data-ttu-id="75823-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="75823-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75823-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="75823-119">-Name</span></span>
<span data-ttu-id="75823-120">Nazwa konkretnej konfiguracji naciśnięcia.</span><span class="sxs-lookup"><span data-stu-id="75823-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="75823-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="75823-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="75823-122">Nazwa interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="75823-122">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75823-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75823-123">-ResourceGroupName</span></span>
<span data-ttu-id="75823-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="75823-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75823-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75823-125">-ResourceId</span></span>
<span data-ttu-id="75823-126">ResourceId zasobu TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="75823-126">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75823-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75823-127">-Confirm</span></span>
<span data-ttu-id="75823-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="75823-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75823-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75823-129">-WhatIf</span></span>
<span data-ttu-id="75823-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75823-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75823-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="75823-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75823-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75823-132">CommonParameters</span></span>
<span data-ttu-id="75823-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75823-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75823-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75823-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75823-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75823-135">INPUTS</span></span>

### <span data-ttu-id="75823-136">System.String</span><span class="sxs-lookup"><span data-stu-id="75823-136">System.String</span></span>

## <span data-ttu-id="75823-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75823-137">OUTPUTS</span></span>

### <span data-ttu-id="75823-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="75823-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="75823-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75823-139">NOTES</span></span>

## <span data-ttu-id="75823-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75823-140">RELATED LINKS</span></span>

[<span data-ttu-id="75823-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="75823-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="75823-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="75823-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="75823-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="75823-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
