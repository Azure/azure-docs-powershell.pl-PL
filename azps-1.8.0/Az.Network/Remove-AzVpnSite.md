---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 0215a05db7e18dad9aeb26476d7076bdc556b021
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709049"
---
# <span data-ttu-id="d398e-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="d398e-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="d398e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d398e-102">SYNOPSIS</span></span>
<span data-ttu-id="d398e-103">Usuwa zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="d398e-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="d398e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d398e-104">SYNTAX</span></span>

### <span data-ttu-id="d398e-105">ByVpnSiteName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d398e-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d398e-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="d398e-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d398e-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="d398e-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d398e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d398e-108">DESCRIPTION</span></span>
<span data-ttu-id="d398e-109">Usuwa zasób usługi Azure VpnSite.</span><span class="sxs-lookup"><span data-stu-id="d398e-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="d398e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d398e-110">EXAMPLES</span></span>

### <span data-ttu-id="d398e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d398e-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="d398e-112">Powyższa grupa utworzy grupę zasobów, wirtualną sieć WAN w zachodnim stanie Stanów Zjednoczonych w grupie zasobów "testRG" na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d398e-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="d398e-113">Następnie tworzy VpnSite do reprezentowania oddziału klienta i łączy go z wirtualną WAN.</span><span class="sxs-lookup"><span data-stu-id="d398e-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="d398e-114">Po utworzeniu witryny jest ona natychmiast usuwana przy użyciu polecenia Remove-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="d398e-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="d398e-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d398e-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="d398e-116">Taki sam jak w przykładzie 1, ale usunięcie jest wykonywane przy użyciu danych wyjściowych potoku z poziomu polecenia Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="d398e-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="d398e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d398e-117">PARAMETERS</span></span>

### <span data-ttu-id="d398e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d398e-118">-DefaultProfile</span></span>
<span data-ttu-id="d398e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d398e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d398e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d398e-120">-Force</span></span>
<span data-ttu-id="d398e-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d398e-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d398e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d398e-122">-InputObject</span></span>
<span data-ttu-id="d398e-123">Obiekt vpnSite, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="d398e-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="d398e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d398e-124">-Name</span></span>
<span data-ttu-id="d398e-125">Nazwa vpnSite.</span><span class="sxs-lookup"><span data-stu-id="d398e-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="d398e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d398e-126">-PassThru</span></span>
<span data-ttu-id="d398e-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d398e-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d398e-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d398e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d398e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d398e-129">-ResourceGroupName</span></span>
<span data-ttu-id="d398e-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d398e-130">The resource group name.</span></span>

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

### <span data-ttu-id="d398e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d398e-131">-ResourceId</span></span>
<span data-ttu-id="d398e-132">Identyfikator zasobu platformy Azure dla vpnSite, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="d398e-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="d398e-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d398e-133">-Confirm</span></span>
<span data-ttu-id="d398e-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d398e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d398e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d398e-135">-WhatIf</span></span>
<span data-ttu-id="d398e-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d398e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d398e-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d398e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d398e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d398e-138">CommonParameters</span></span>
<span data-ttu-id="d398e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d398e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d398e-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d398e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d398e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d398e-141">INPUTS</span></span>

### <span data-ttu-id="d398e-142">Microsoft. Azure. Commands. Network. models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="d398e-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="d398e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d398e-143">System.String</span></span>

## <span data-ttu-id="d398e-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d398e-144">OUTPUTS</span></span>

### <span data-ttu-id="d398e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d398e-145">System.Boolean</span></span>

## <span data-ttu-id="d398e-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d398e-146">NOTES</span></span>

## <span data-ttu-id="d398e-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d398e-147">RELATED LINKS</span></span>

[<span data-ttu-id="d398e-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="d398e-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="d398e-149">Nowe — AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="d398e-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="d398e-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="d398e-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
