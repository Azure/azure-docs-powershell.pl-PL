---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: df769ff4a6e4eb47bc47b881ac8c06de1fdb9e4c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890758"
---
# <span data-ttu-id="bf413-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bf413-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="bf413-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf413-102">SYNOPSIS</span></span>
<span data-ttu-id="bf413-103">Pobiera interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="bf413-103">Gets a network interface.</span></span>

## <span data-ttu-id="bf413-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf413-104">SYNTAX</span></span>

### <span data-ttu-id="bf413-105">NoExpandStandAloneNic (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf413-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf413-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="bf413-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf413-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="bf413-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf413-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="bf413-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf413-109">Opis</span><span class="sxs-lookup"><span data-stu-id="bf413-109">DESCRIPTION</span></span>
<span data-ttu-id="bf413-110">Polecenie cmdlet **Get-AzNetworkInterface** pobiera interfejs sieci Azure lub listę interfejsów sieciowych platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf413-110">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="bf413-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf413-111">EXAMPLES</span></span>

### <span data-ttu-id="bf413-112">Przykład 1: pobieranie wszystkich interfejsów sieciowych</span><span class="sxs-lookup"><span data-stu-id="bf413-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzNetworkInterface
```

<span data-ttu-id="bf413-113">To polecenie pobiera wszystkie interfejsy sieciowe dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bf413-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="bf413-114">Przykład 2: uzyskiwanie wszystkich interfejsów sieciowych z określonym stanem inicjowania obsługi</span><span class="sxs-lookup"><span data-stu-id="bf413-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="bf413-115">To polecenie pobiera wszystkie interfejsy sieciowe w grupie zasobów o nazwie ResourceGroup1, która ma stan aprowizacji zakończonych powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="bf413-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="bf413-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf413-116">PARAMETERS</span></span>

### <span data-ttu-id="bf413-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf413-117">-DefaultProfile</span></span>
<span data-ttu-id="bf413-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf413-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf413-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="bf413-119">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf413-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf413-120">-Name</span></span>
<span data-ttu-id="bf413-121">Określa nazwę interfejsu sieciowego, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf413-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf413-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf413-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf413-123">Określa nazwę grupy zasobów, z której to polecenie cmdlet pobiera interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="bf413-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf413-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="bf413-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="bf413-125">Określa indeks maszyny wirtualnej zestawu skali maszyny wirtualnej, na podstawie którego to polecenie cmdlet pobiera interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="bf413-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf413-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="bf413-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="bf413-127">Określa nazwę zestawu skali maszyny wirtualnej, na podstawie którego to polecenie cmdlet pobiera interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="bf413-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf413-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf413-128">CommonParameters</span></span>
<span data-ttu-id="bf413-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf413-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf413-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf413-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf413-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf413-131">INPUTS</span></span>

## <span data-ttu-id="bf413-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf413-132">OUTPUTS</span></span>

### <span data-ttu-id="bf413-133">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bf413-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="bf413-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf413-134">NOTES</span></span>

## <span data-ttu-id="bf413-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf413-135">RELATED LINKS</span></span>

[<span data-ttu-id="bf413-136">Nowe — AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bf413-136">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="bf413-137">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bf413-137">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="bf413-138">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="bf413-138">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


