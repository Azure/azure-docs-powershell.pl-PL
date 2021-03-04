---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 50e335825fb43a85286be5f95696c1dd1a537129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962673"
---
# <span data-ttu-id="9b932-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9b932-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="9b932-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b932-102">SYNOPSIS</span></span>
<span data-ttu-id="9b932-103">Usuwa zasób witryny VpnSite platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b932-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="9b932-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b932-104">SYNTAX</span></span>

### <span data-ttu-id="9b932-105">ByVpnsiteName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="9b932-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b932-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="9b932-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b932-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="9b932-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b932-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b932-108">DESCRIPTION</span></span>
<span data-ttu-id="9b932-109">Usuwa zasób witryny VpnSite platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9b932-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="9b932-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b932-110">EXAMPLES</span></span>

### <span data-ttu-id="9b932-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b932-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="9b932-112">Powyższe spowoduje utworzenie grupy zasobów o wirtualnej sieci WAN w Zachód USA w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9b932-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="9b932-113">Następnie tworzy witrynę VpnSite reprezentującą gałąź klienta i łączy ją z wirtualną siecią WAN.</span><span class="sxs-lookup"><span data-stu-id="9b932-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="9b932-114">Po utworzeniu witryna jest natychmiast usuwana za pomocą Remove-AzVpnSite witryny.</span><span class="sxs-lookup"><span data-stu-id="9b932-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="9b932-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9b932-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="9b932-116">Tak samo, jak w przykładzie 1, ale tutaj usuwanie odbywa się przy użyciu danych wyjściowych potokowych z Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="9b932-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="9b932-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b932-117">PARAMETERS</span></span>

### <span data-ttu-id="9b932-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b932-118">-DefaultProfile</span></span>
<span data-ttu-id="9b932-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b932-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b932-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="9b932-120">-Force</span></span>
<span data-ttu-id="9b932-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b932-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b932-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b932-122">-InputObject</span></span>
<span data-ttu-id="9b932-123">Obiekt vpnSite do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9b932-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b932-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9b932-124">-Name</span></span>
<span data-ttu-id="9b932-125">Nazwa vpnSite.</span><span class="sxs-lookup"><span data-stu-id="9b932-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b932-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b932-126">-PassThru</span></span>
<span data-ttu-id="9b932-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="9b932-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="9b932-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9b932-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b932-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b932-129">-ResourceGroupName</span></span>
<span data-ttu-id="9b932-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9b932-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b932-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b932-131">-ResourceId</span></span>
<span data-ttu-id="9b932-132">Identyfikator zasobu Azure dla witryny vpnSite do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9b932-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b932-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b932-133">-Confirm</span></span>
<span data-ttu-id="9b932-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b932-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b932-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b932-135">-WhatIf</span></span>
<span data-ttu-id="9b932-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b932-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b932-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9b932-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b932-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b932-138">CommonParameters</span></span>
<span data-ttu-id="9b932-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b932-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b932-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b932-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b932-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b932-141">INPUTS</span></span>

### <span data-ttu-id="9b932-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="9b932-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="9b932-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9b932-143">System.String</span></span>

## <span data-ttu-id="9b932-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b932-144">OUTPUTS</span></span>

### <span data-ttu-id="9b932-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b932-145">System.Boolean</span></span>

## <span data-ttu-id="9b932-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b932-146">NOTES</span></span>

## <span data-ttu-id="9b932-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b932-147">RELATED LINKS</span></span>

[<span data-ttu-id="9b932-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9b932-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="9b932-149">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9b932-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="9b932-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="9b932-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
