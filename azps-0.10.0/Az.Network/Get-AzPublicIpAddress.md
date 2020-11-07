---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: b9eaacb9a9d779814fc5f0b873aa8e98afedd362
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890685"
---
# <span data-ttu-id="275c0-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="275c0-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="275c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="275c0-102">SYNOPSIS</span></span>
<span data-ttu-id="275c0-103">Pobiera publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="275c0-103">Gets a public IP address.</span></span>

## <span data-ttu-id="275c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="275c0-104">SYNTAX</span></span>

### <span data-ttu-id="275c0-105">NoExpandStandAloneIp (domyślny)</span><span class="sxs-lookup"><span data-stu-id="275c0-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="275c0-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="275c0-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="275c0-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="275c0-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="275c0-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="275c0-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="275c0-109">Opis</span><span class="sxs-lookup"><span data-stu-id="275c0-109">DESCRIPTION</span></span>
<span data-ttu-id="275c0-110">Polecenie cmdlet **Get-AzPublicIPAddress** pobiera co najmniej jeden publiczny adres IP w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="275c0-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="275c0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="275c0-111">EXAMPLES</span></span>

### <span data-ttu-id="275c0-112">1: uzyskiwanie publicznego zasobu IP</span><span class="sxs-lookup"><span data-stu-id="275c0-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="275c0-113">To polecenie pobiera publiczny zasób adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="275c0-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="275c0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="275c0-114">PARAMETERS</span></span>

### <span data-ttu-id="275c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275c0-115">-DefaultProfile</span></span>
<span data-ttu-id="275c0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="275c0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="275c0-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="275c0-117">-ExpandResource</span></span>
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

### <span data-ttu-id="275c0-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="275c0-118">-IpConfigurationName</span></span>
<span data-ttu-id="275c0-119">Nazwa konfiguracji adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="275c0-119">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="275c0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="275c0-120">-Name</span></span>
<span data-ttu-id="275c0-121">Określa nazwę publicznego adresu IP, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275c0-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="275c0-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="275c0-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="275c0-123">Nazwa interfejsu sieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="275c0-123">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="275c0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275c0-124">-ResourceGroupName</span></span>
<span data-ttu-id="275c0-125">Określa nazwę grupy zasobów zawierającej publiczny adres IP, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275c0-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="275c0-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="275c0-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="275c0-127">Indeks maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="275c0-127">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="275c0-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="275c0-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="275c0-129">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="275c0-129">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="275c0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275c0-130">CommonParameters</span></span>
<span data-ttu-id="275c0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275c0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275c0-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275c0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275c0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="275c0-133">INPUTS</span></span>

## <span data-ttu-id="275c0-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="275c0-134">OUTPUTS</span></span>

### <span data-ttu-id="275c0-135">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="275c0-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="275c0-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="275c0-136">NOTES</span></span>

## <span data-ttu-id="275c0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="275c0-137">RELATED LINKS</span></span>

[<span data-ttu-id="275c0-138">Nowe — AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="275c0-138">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="275c0-139">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="275c0-139">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="275c0-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="275c0-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


