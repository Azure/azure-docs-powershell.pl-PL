---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 263293ea117f85caf32029ee0cfbf0dff2142cc3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899273"
---
# <span data-ttu-id="351a4-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="351a4-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="351a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="351a4-102">SYNOPSIS</span></span>
<span data-ttu-id="351a4-103">Pobiera interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="351a4-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="351a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="351a4-104">SYNTAX</span></span>

### <span data-ttu-id="351a4-105">NoExpandStandAloneNic (domyślny)</span><span class="sxs-lookup"><span data-stu-id="351a4-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="351a4-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="351a4-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="351a4-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="351a4-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="351a4-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="351a4-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="351a4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="351a4-109">DESCRIPTION</span></span>
<span data-ttu-id="351a4-110">Polecenie cmdlet **Get-AzureRmNetworkInterface** pobiera interfejs sieci Azure lub listę interfejsów sieciowych platformy Azure w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="351a4-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="351a4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="351a4-111">EXAMPLES</span></span>

### <span data-ttu-id="351a4-112">Przykład 1: pobieranie wszystkich interfejsów sieciowych</span><span class="sxs-lookup"><span data-stu-id="351a4-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="351a4-113">To polecenie pobiera wszystkie interfejsy sieciowe dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="351a4-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="351a4-114">Przykład 2: uzyskiwanie wszystkich interfejsów sieciowych z określonym stanem inicjowania obsługi</span><span class="sxs-lookup"><span data-stu-id="351a4-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="351a4-115">To polecenie pobiera wszystkie interfejsy sieciowe w grupie zasobów o nazwie ResourceGroup1, która ma stan aprowizacji zakończonych powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="351a4-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="351a4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="351a4-116">PARAMETERS</span></span>

### <span data-ttu-id="351a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351a4-117">-DefaultProfile</span></span>
<span data-ttu-id="351a4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="351a4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="351a4-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="351a4-119">-ExpandResource</span></span>
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

### <span data-ttu-id="351a4-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="351a4-120">-Name</span></span>
<span data-ttu-id="351a4-121">Określa nazwę interfejsu sieciowego, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="351a4-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

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

### <span data-ttu-id="351a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="351a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="351a4-123">Określa nazwę grupy zasobów, z której to polecenie cmdlet pobiera interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="351a4-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="351a4-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="351a4-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="351a4-125">Określa indeks maszyny wirtualnej zestawu skali maszyny wirtualnej, na podstawie którego to polecenie cmdlet pobiera interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="351a4-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="351a4-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="351a4-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="351a4-127">Określa nazwę zestawu skali maszyny wirtualnej, na podstawie którego to polecenie cmdlet pobiera interfejsy sieciowe.</span><span class="sxs-lookup"><span data-stu-id="351a4-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="351a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351a4-128">CommonParameters</span></span>
<span data-ttu-id="351a4-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="351a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351a4-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="351a4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351a4-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="351a4-131">INPUTS</span></span>

## <span data-ttu-id="351a4-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="351a4-132">OUTPUTS</span></span>

### <span data-ttu-id="351a4-133">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="351a4-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="351a4-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="351a4-134">NOTES</span></span>

## <span data-ttu-id="351a4-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="351a4-135">RELATED LINKS</span></span>

[<span data-ttu-id="351a4-136">Nowe — AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="351a4-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="351a4-137">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="351a4-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="351a4-138">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="351a4-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


