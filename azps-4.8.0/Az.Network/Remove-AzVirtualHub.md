---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063346"
---
# <span data-ttu-id="459c1-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="459c1-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="459c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="459c1-102">SYNOPSIS</span></span>
<span data-ttu-id="459c1-103">Usuwa zasób usługi Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="459c1-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="459c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="459c1-104">SYNTAX</span></span>

### <span data-ttu-id="459c1-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="459c1-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="459c1-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="459c1-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="459c1-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="459c1-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="459c1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="459c1-108">DESCRIPTION</span></span>
<span data-ttu-id="459c1-109">Usuwa zasób usługi Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="459c1-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="459c1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="459c1-110">EXAMPLES</span></span>

### <span data-ttu-id="459c1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="459c1-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="459c1-112">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="459c1-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="459c1-113">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="459c1-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="459c1-114">Następnie usuwa koncentratora wirtualnego przy użyciu jego ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="459c1-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="459c1-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="459c1-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="459c1-116">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="459c1-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="459c1-117">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="459c1-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="459c1-118">Następnie usuwa koncentratora wirtualnego przy użyciu obiektu wejścia.</span><span class="sxs-lookup"><span data-stu-id="459c1-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="459c1-119">Obiekt wejściowy jest typu PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="459c1-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="459c1-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="459c1-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="459c1-121">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="459c1-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="459c1-122">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="459c1-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="459c1-123">Następnie usuwa koncentratora wirtualnego przy użyciu połączeń programu PowerShell przy użyciu danych wyjściowych z polecenia Get-AzVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="459c1-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="459c1-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="459c1-124">PARAMETERS</span></span>

### <span data-ttu-id="459c1-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="459c1-125">-AsJob</span></span>
<span data-ttu-id="459c1-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="459c1-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="459c1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="459c1-127">-DefaultProfile</span></span>
<span data-ttu-id="459c1-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="459c1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="459c1-129">-Force</span><span class="sxs-lookup"><span data-stu-id="459c1-129">-Force</span></span>
<span data-ttu-id="459c1-130">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="459c1-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="459c1-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="459c1-131">-InputObject</span></span>
<span data-ttu-id="459c1-132">Wirtualny obiekt koncentratorowy do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="459c1-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="459c1-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="459c1-133">-Name</span></span>
<span data-ttu-id="459c1-134">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="459c1-134">The resource name.</span></span>

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

### <span data-ttu-id="459c1-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="459c1-135">-PassThru</span></span>
<span data-ttu-id="459c1-136">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="459c1-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="459c1-137">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="459c1-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="459c1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="459c1-138">-ResourceGroupName</span></span>
<span data-ttu-id="459c1-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="459c1-139">The resource group name.</span></span>

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

### <span data-ttu-id="459c1-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="459c1-140">-ResourceId</span></span>
<span data-ttu-id="459c1-141">Identyfikator zasobu wirtualnego koncentratora, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="459c1-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="459c1-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="459c1-142">-Confirm</span></span>
<span data-ttu-id="459c1-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="459c1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="459c1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="459c1-144">-WhatIf</span></span>
<span data-ttu-id="459c1-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="459c1-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="459c1-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="459c1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="459c1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="459c1-147">CommonParameters</span></span>
<span data-ttu-id="459c1-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="459c1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="459c1-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="459c1-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="459c1-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="459c1-150">INPUTS</span></span>

### <span data-ttu-id="459c1-151">System. String</span><span class="sxs-lookup"><span data-stu-id="459c1-151">System.String</span></span>

### <span data-ttu-id="459c1-152">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="459c1-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="459c1-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="459c1-153">OUTPUTS</span></span>

### <span data-ttu-id="459c1-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="459c1-154">System.Boolean</span></span>

## <span data-ttu-id="459c1-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="459c1-155">NOTES</span></span>

## <span data-ttu-id="459c1-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="459c1-156">RELATED LINKS</span></span>

[<span data-ttu-id="459c1-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="459c1-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="459c1-158">Nowe — AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="459c1-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="459c1-159">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="459c1-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
