---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: 9864ba724d20e088e410bc99e8642fae97d71fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552395"
---
# <span data-ttu-id="8ddd3-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ddd3-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="8ddd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ddd3-102">SYNOPSIS</span></span>
<span data-ttu-id="8ddd3-103">Pobiera publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ddd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ddd3-104">SYNTAX</span></span>

### <span data-ttu-id="8ddd3-105">NoExpandStandAloneIp (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8ddd3-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ddd3-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="8ddd3-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ddd3-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="8ddd3-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ddd3-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="8ddd3-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ddd3-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8ddd3-109">DESCRIPTION</span></span>
<span data-ttu-id="8ddd3-110">Polecenie cmdlet **Get-AzureRmPublicIPAddress** pobiera co najmniej jeden publiczny adres IP w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="8ddd3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ddd3-111">EXAMPLES</span></span>

### <span data-ttu-id="8ddd3-112">1: uzyskiwanie publicznego zasobu IP</span><span class="sxs-lookup"><span data-stu-id="8ddd3-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="8ddd3-113">To polecenie pobiera publiczny zasób adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="8ddd3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ddd3-114">PARAMETERS</span></span>

### <span data-ttu-id="8ddd3-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8ddd3-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-116">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8ddd3-116">-IpConfigurationName</span></span>
<span data-ttu-id="8ddd3-117">Nazwa konfiguracji adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-117">Network Interface IP Configuration Name.</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ddd3-118">-Name</span></span>
<span data-ttu-id="8ddd3-119">Określa nazwę publicznego adresu IP, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-119">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-120">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="8ddd3-120">-NetworkInterfaceName</span></span>
<span data-ttu-id="8ddd3-121">Nazwa interfejsu sieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-121">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ddd3-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ddd3-123">Określa nazwę grupy zasobów zawierającej publiczny adres IP, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-123">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="8ddd3-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="8ddd3-125">Indeks maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-125">Virtual Machine Index.</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8ddd3-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="8ddd3-127">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-127">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ddd3-128">-DefaultProfile</span></span>
<span data-ttu-id="8ddd3-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ddd3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ddd3-130">CommonParameters</span></span>
<span data-ttu-id="8ddd3-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ddd3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ddd3-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ddd3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ddd3-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ddd3-133">INPUTS</span></span>

## <span data-ttu-id="8ddd3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ddd3-134">OUTPUTS</span></span>

### <span data-ttu-id="8ddd3-135">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ddd3-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="8ddd3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ddd3-136">NOTES</span></span>

## <span data-ttu-id="8ddd3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ddd3-137">RELATED LINKS</span></span>

[<span data-ttu-id="8ddd3-138">Nowe — AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ddd3-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="8ddd3-139">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ddd3-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="8ddd3-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ddd3-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


