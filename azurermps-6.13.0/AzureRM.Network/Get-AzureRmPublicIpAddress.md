---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: b6d71d4c80ba30fc02bb22695132a304f94416cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543768"
---
# <span data-ttu-id="c4293-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4293-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="c4293-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4293-102">SYNOPSIS</span></span>
<span data-ttu-id="c4293-103">Pobiera publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="c4293-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4293-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4293-104">SYNTAX</span></span>

### <span data-ttu-id="c4293-105">NoExpandStandAloneIp (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c4293-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4293-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="c4293-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4293-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="c4293-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4293-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="c4293-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4293-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c4293-109">DESCRIPTION</span></span>
<span data-ttu-id="c4293-110">Polecenie cmdlet **Get-AzureRmPublicIPAddress** pobiera co najmniej jeden publiczny adres IP w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c4293-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="c4293-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4293-111">EXAMPLES</span></span>

### <span data-ttu-id="c4293-112">1: uzyskiwanie publicznego zasobu IP</span><span class="sxs-lookup"><span data-stu-id="c4293-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="c4293-113">To polecenie pobiera publiczny zasób adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="c4293-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="c4293-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4293-114">PARAMETERS</span></span>

### <span data-ttu-id="c4293-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4293-115">-DefaultProfile</span></span>
<span data-ttu-id="c4293-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4293-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4293-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c4293-117">-ExpandResource</span></span>
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

### <span data-ttu-id="c4293-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c4293-118">-IpConfigurationName</span></span>
<span data-ttu-id="c4293-119">Nazwa konfiguracji adresu IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c4293-119">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="c4293-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4293-120">-Name</span></span>
<span data-ttu-id="c4293-121">Określa nazwę publicznego adresu IP, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4293-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c4293-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="c4293-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="c4293-123">Nazwa interfejsu sieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c4293-123">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="c4293-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4293-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4293-125">Określa nazwę grupy zasobów zawierającej publiczny adres IP, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4293-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c4293-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="c4293-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="c4293-127">Indeks maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c4293-127">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="c4293-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c4293-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="c4293-129">Nazwa zestawu skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c4293-129">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="c4293-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4293-130">CommonParameters</span></span>
<span data-ttu-id="c4293-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4293-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4293-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4293-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4293-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4293-133">INPUTS</span></span>

### <span data-ttu-id="c4293-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c4293-134">System.String</span></span>

## <span data-ttu-id="c4293-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4293-135">OUTPUTS</span></span>

### <span data-ttu-id="c4293-136">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4293-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="c4293-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4293-137">NOTES</span></span>

## <span data-ttu-id="c4293-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4293-138">RELATED LINKS</span></span>

[<span data-ttu-id="c4293-139">Nowe — AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4293-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c4293-140">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4293-140">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="c4293-141">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4293-141">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


