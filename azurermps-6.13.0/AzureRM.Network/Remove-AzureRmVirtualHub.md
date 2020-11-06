---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHub.md
ms.openlocfilehash: 65d319749424697c882012d23bf12f87f92adbc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552655"
---
# <span data-ttu-id="8700b-101">Remove-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8700b-101">Remove-AzureRmVirtualHub</span></span>

## <span data-ttu-id="8700b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8700b-102">SYNOPSIS</span></span>
<span data-ttu-id="8700b-103">Usuwa zasób usługi Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="8700b-103">Removes an Azure VirtualHub resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8700b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8700b-104">SYNTAX</span></span>

### <span data-ttu-id="8700b-105">ByVirtualHubName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8700b-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzureRmVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8700b-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="8700b-106">ByVirtualHubResourceId</span></span>
```
Remove-AzureRmVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8700b-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="8700b-107">ByVirtualHubObject</span></span>
```
Remove-AzureRmVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8700b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8700b-108">DESCRIPTION</span></span>
<span data-ttu-id="8700b-109">Usuwa zasób usługi Azure VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="8700b-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="8700b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8700b-110">EXAMPLES</span></span>

### <span data-ttu-id="8700b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8700b-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="8700b-112">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8700b-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="8700b-113">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="8700b-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="8700b-114">Następnie usuwa koncentratora wirtualnego przy użyciu jego ResourceGroupName i ResourceName.</span><span class="sxs-lookup"><span data-stu-id="8700b-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="8700b-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8700b-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzureRmVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="8700b-116">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8700b-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="8700b-117">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="8700b-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="8700b-118">Następnie usuwa koncentratora wirtualnego przy użyciu obiektu wejścia.</span><span class="sxs-lookup"><span data-stu-id="8700b-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="8700b-119">Obiekt wejściowy jest typu PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="8700b-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="8700b-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8700b-120">Example 3</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzureRmVirtualHub
```

<span data-ttu-id="8700b-121">Powyższy sposób spowoduje utworzenie grupy zasobów "testRG", wirtualnej sieci WAN i wirtualnego centrum na zachodnim terenie w tej grupie zasobów na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8700b-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="8700b-122">Koncentrator wirtualny będzie miał przestrzeń adresową "10.0.1.0/24".</span><span class="sxs-lookup"><span data-stu-id="8700b-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="8700b-123">Następnie usuwa koncentratora wirtualnego przy użyciu połączeń programu PowerShell przy użyciu danych wyjściowych z polecenia Get-AzureRmVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="8700b-123">It then deletes the virtual hub using powershell piping using output from Get-AzureRmVirtualHub.</span></span>

## <span data-ttu-id="8700b-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8700b-124">PARAMETERS</span></span>

### <span data-ttu-id="8700b-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8700b-125">-AsJob</span></span>
<span data-ttu-id="8700b-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8700b-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8700b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8700b-127">-DefaultProfile</span></span>
<span data-ttu-id="8700b-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8700b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8700b-129">-Force</span><span class="sxs-lookup"><span data-stu-id="8700b-129">-Force</span></span>
<span data-ttu-id="8700b-130">Nie pytaj o potwierdzenie, czy zachodzi konieczność przestania się zasobu</span><span class="sxs-lookup"><span data-stu-id="8700b-130">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="8700b-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8700b-131">-InputObject</span></span>
<span data-ttu-id="8700b-132">Wirtualny obiekt koncentratorowy do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="8700b-132">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="8700b-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8700b-133">-Name</span></span>
<span data-ttu-id="8700b-134">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="8700b-134">The resource name.</span></span>

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

### <span data-ttu-id="8700b-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8700b-135">-PassThru</span></span>
<span data-ttu-id="8700b-136">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="8700b-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8700b-137">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8700b-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8700b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8700b-138">-ResourceGroupName</span></span>
<span data-ttu-id="8700b-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8700b-139">The resource group name.</span></span>

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

### <span data-ttu-id="8700b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8700b-140">-ResourceId</span></span>
<span data-ttu-id="8700b-141">Identyfikator zasobu wirtualnego koncentratora, który ma zostać zmodyfikowany.</span><span class="sxs-lookup"><span data-stu-id="8700b-141">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="8700b-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8700b-142">-Confirm</span></span>
<span data-ttu-id="8700b-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8700b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8700b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8700b-144">-WhatIf</span></span>
<span data-ttu-id="8700b-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8700b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8700b-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8700b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8700b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8700b-147">CommonParameters</span></span>
<span data-ttu-id="8700b-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8700b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8700b-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8700b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8700b-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8700b-150">INPUTS</span></span>

### <span data-ttu-id="8700b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="8700b-151">System.String</span></span>

### <span data-ttu-id="8700b-152">Microsoft. Azure. Commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8700b-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="8700b-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8700b-153">OUTPUTS</span></span>

### <span data-ttu-id="8700b-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8700b-154">System.Boolean</span></span>

## <span data-ttu-id="8700b-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8700b-155">NOTES</span></span>

## <span data-ttu-id="8700b-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8700b-156">RELATED LINKS</span></span>
