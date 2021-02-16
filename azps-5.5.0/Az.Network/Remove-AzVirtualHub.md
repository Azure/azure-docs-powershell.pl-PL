---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186923"
---
# <span data-ttu-id="51536-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="51536-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="51536-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51536-102">SYNOPSIS</span></span>
<span data-ttu-id="51536-103">Usuwa zasób usługi Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="51536-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="51536-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51536-104">SYNTAX</span></span>

### <span data-ttu-id="51536-105">ByVirtualHubName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="51536-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51536-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="51536-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51536-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="51536-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51536-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="51536-108">DESCRIPTION</span></span>
<span data-ttu-id="51536-109">Usuwa zasób usługi Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="51536-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="51536-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51536-110">EXAMPLES</span></span>

### <span data-ttu-id="51536-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="51536-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="51536-112">Powyższe spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i centrum wirtualnego w Zachód w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="51536-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="51536-113">Centrum wirtualne będzie mieć przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="51536-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="51536-114">Następnie usuwa centrum wirtualne za pomocą nazwy ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="51536-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="51536-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="51536-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="51536-116">Powyższe spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i centrum wirtualnego w Zachód w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="51536-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="51536-117">Centrum wirtualne będzie mieć przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="51536-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="51536-118">Następnie usuwa centrum wirtualne za pomocą obiektu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="51536-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="51536-119">Obiekt wejściowy jest typu PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="51536-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="51536-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="51536-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="51536-121">Powyższe spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i centrum wirtualnego w Zachód w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="51536-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="51536-122">Centrum wirtualne będzie mieć przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="51536-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="51536-123">Następnie usuwa centrum wirtualne za pomocą rur programu PowerShell przy użyciu danych wyjściowych z aplikacji Get-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="51536-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="51536-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51536-124">PARAMETERS</span></span>

### <span data-ttu-id="51536-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="51536-125">-AsJob</span></span>
<span data-ttu-id="51536-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="51536-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51536-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51536-127">-DefaultProfile</span></span>
<span data-ttu-id="51536-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="51536-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51536-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="51536-129">-Force</span></span>
<span data-ttu-id="51536-130">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="51536-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="51536-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51536-131">-InputObject</span></span>
<span data-ttu-id="51536-132">Obiekt centrum wirtualnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="51536-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51536-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="51536-133">-Name</span></span>
<span data-ttu-id="51536-134">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="51536-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51536-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51536-135">-PassThru</span></span>
<span data-ttu-id="51536-136">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="51536-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="51536-137">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="51536-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51536-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51536-138">-ResourceGroupName</span></span>
<span data-ttu-id="51536-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51536-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51536-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51536-140">-ResourceId</span></span>
<span data-ttu-id="51536-141">Identyfikator zasobu centrum wirtualnego do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="51536-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51536-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51536-142">-Confirm</span></span>
<span data-ttu-id="51536-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51536-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51536-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51536-144">-WhatIf</span></span>
<span data-ttu-id="51536-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51536-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51536-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="51536-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51536-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51536-147">CommonParameters</span></span>
<span data-ttu-id="51536-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51536-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51536-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51536-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51536-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51536-150">INPUTS</span></span>

### <span data-ttu-id="51536-151">System.String</span><span class="sxs-lookup"><span data-stu-id="51536-151">System.String</span></span>

### <span data-ttu-id="51536-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="51536-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="51536-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51536-153">OUTPUTS</span></span>

### <span data-ttu-id="51536-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51536-154">System.Boolean</span></span>

## <span data-ttu-id="51536-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51536-155">NOTES</span></span>

## <span data-ttu-id="51536-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51536-156">RELATED LINKS</span></span>

[<span data-ttu-id="51536-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="51536-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="51536-158">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="51536-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="51536-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="51536-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
