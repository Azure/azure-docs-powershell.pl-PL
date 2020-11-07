---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 1404acfa32de79096e990adbe2f66b43af0d4e96
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899262"
---
# <span data-ttu-id="d9b49-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9b49-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="d9b49-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9b49-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b49-103">Pobiera publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="d9b49-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9b49-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9b49-104">SYNTAX</span></span>

### <span data-ttu-id="d9b49-105">NoExpandStandAloneIp (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d9b49-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9b49-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="d9b49-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9b49-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="d9b49-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9b49-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="d9b49-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9b49-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d9b49-109">DESCRIPTION</span></span>
<span data-ttu-id="d9b49-110">Polecenie cmdlet **Get-AzureRmPublicIPAddress** pobiera co najmniej jeden publiczny adres IP w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9b49-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="d9b49-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9b49-111">EXAMPLES</span></span>

### <span data-ttu-id="d9b49-112">1: uzyskiwanie publicznego zasobu IP</span><span class="sxs-lookup"><span data-stu-id="d9b49-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="d9b49-113">To polecenie pobiera publiczny zasób adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="d9b49-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="d9b49-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9b49-114">PARAMETERS</span></span>

### <span data-ttu-id="d9b49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b49-115">-DefaultProfile</span></span>
<span data-ttu-id="d9b49-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b49-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9b49-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d9b49-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b49-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d9b49-118">-IpConfigurationName</span></span>
<span data-ttu-id="d9b49-119">Nazwa konfiguracji adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="d9b49-119">Network Interface IP Configuration Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b49-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9b49-120">-Name</span></span>
<span data-ttu-id="d9b49-121">Określa nazwę publicznego adresu IP, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9b49-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b49-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="d9b49-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="d9b49-123">Nazwa interfejsu sieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d9b49-123">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b49-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9b49-125">Określa nazwę grupy zasobów zawierającej publiczny adres IP, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9b49-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b49-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="d9b49-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="d9b49-127">Indeks maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d9b49-127">Virtual Machine Index.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b49-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d9b49-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="d9b49-129">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d9b49-129">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b49-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b49-130">CommonParameters</span></span>
<span data-ttu-id="d9b49-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b49-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b49-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b49-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b49-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9b49-133">INPUTS</span></span>

## <span data-ttu-id="d9b49-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9b49-134">OUTPUTS</span></span>

### <span data-ttu-id="d9b49-135">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9b49-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d9b49-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9b49-136">NOTES</span></span>

## <span data-ttu-id="d9b49-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9b49-137">RELATED LINKS</span></span>

[<span data-ttu-id="d9b49-138">Nowe — AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9b49-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d9b49-139">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9b49-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d9b49-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9b49-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


