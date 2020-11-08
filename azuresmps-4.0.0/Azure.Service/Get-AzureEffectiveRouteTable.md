---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055319"
---
# <span data-ttu-id="93aa3-101">Get-AzureEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="93aa3-101">Get-AzureEffectiveRouteTable</span></span>

## <span data-ttu-id="93aa3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="93aa3-103">Pobiera trasę założoną na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="93aa3-103">Gets the route applied in a virtual machine.</span></span>

## <span data-ttu-id="93aa3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93aa3-104">SYNTAX</span></span>

### <span data-ttu-id="93aa3-105">IaaSGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="93aa3-105">IaaSGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="93aa3-106">SlotGetEffectiveRouteTableParamSet</span><span class="sxs-lookup"><span data-stu-id="93aa3-106">SlotGetEffectiveRouteTableParamSet</span></span>
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="93aa3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="93aa3-107">DESCRIPTION</span></span>
<span data-ttu-id="93aa3-108">Polecenie cmdlet **Get-AzureEffectiveRouteTable** umożliwia pobieranie trasy zastosowanej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="93aa3-108">The **Get-AzureEffectiveRouteTable** cmdlet gets the route applied in a virtual machine.</span></span>
<span data-ttu-id="93aa3-109">Ukończenie tej operacji może potrwać kilka sekund.</span><span class="sxs-lookup"><span data-stu-id="93aa3-109">This operation could take several seconds to finish.</span></span>

## <span data-ttu-id="93aa3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93aa3-110">EXAMPLES</span></span>

### <span data-ttu-id="93aa3-111">Przykład 1: pobieranie efektywnej trasy zastosowała maszynę wirtualną</span><span class="sxs-lookup"><span data-stu-id="93aa3-111">Example 1: Get the effective route applied a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

<span data-ttu-id="93aa3-112">To polecenie pobiera maszynę wirtualną o nazwie ContosoVM06 dla usługi o nazwie ContosoService i przekazuje ten obiekt maszyny wirtualnej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93aa3-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="93aa3-113">Bieżące polecenie cmdlet umożliwia pobieranie trasy zastosowanej do tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="93aa3-113">The current cmdlet gets the route applied to that virtual machine.</span></span>

## <span data-ttu-id="93aa3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93aa3-114">PARAMETERS</span></span>

### <span data-ttu-id="93aa3-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="93aa3-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="93aa3-116">Określa nazwę karty sieciowej, za pomocą której to polecenie cmdlet pobiera efektywne trasy.</span><span class="sxs-lookup"><span data-stu-id="93aa3-116">Specifies the name of the network adapter for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93aa3-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="93aa3-117">-Profile</span></span>
<span data-ttu-id="93aa3-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93aa3-118">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="93aa3-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="93aa3-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93aa3-120">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="93aa3-120">-RoleInstanceName</span></span>
<span data-ttu-id="93aa3-121">Określa nazwę roli PaaS, dla której to polecenie cmdlet pobiera efektywne trasy.</span><span class="sxs-lookup"><span data-stu-id="93aa3-121">Specifies the name of a PaaS role for which this cmdlet gets effective routes.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93aa3-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="93aa3-122">-ServiceName</span></span>
<span data-ttu-id="93aa3-123">Określa nazwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="93aa3-123">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="93aa3-124">Rola PaaS, dla której to polecenie cmdlet pobiera efektywne trasy, należy do usługi, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="93aa3-124">The PaaS role for which this cmdlet gets effective routes belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93aa3-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="93aa3-125">-Slot</span></span>
<span data-ttu-id="93aa3-126">Określa gniazdo PaaS.</span><span class="sxs-lookup"><span data-stu-id="93aa3-126">Specifies a PaaS slot.</span></span>
<span data-ttu-id="93aa3-127">Rola PaaS, dla której to polecenie cmdlet pobiera efektywne trasy, ma miejsce określone przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="93aa3-127">The PaaS role for which this cmdlet gets effective routes has the slot that this parameter specifies.</span></span>
<span data-ttu-id="93aa3-128">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="93aa3-128">Valid values are:</span></span> 

- <span data-ttu-id="93aa3-129">BOM</span><span class="sxs-lookup"><span data-stu-id="93aa3-129">Production</span></span>
- <span data-ttu-id="93aa3-130">Most</span><span class="sxs-lookup"><span data-stu-id="93aa3-130">Staging</span></span> 

<span data-ttu-id="93aa3-131">Wartością domyślną jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="93aa3-131">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93aa3-132">-VM</span><span class="sxs-lookup"><span data-stu-id="93aa3-132">-VM</span></span>
<span data-ttu-id="93aa3-133">Określa obiekt maszyny wirtualnej, dla którego ten aplet polecenia pobiera efektywne trasy.</span><span class="sxs-lookup"><span data-stu-id="93aa3-133">Specifies the virtual machine object for which this cmdlet gets effective routes.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93aa3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93aa3-134">CommonParameters</span></span>
<span data-ttu-id="93aa3-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93aa3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93aa3-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93aa3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93aa3-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93aa3-137">INPUTS</span></span>

## <span data-ttu-id="93aa3-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93aa3-138">OUTPUTS</span></span>

### <span data-ttu-id="93aa3-139">System. Collections. Generic. IEnumerable<Microsoft. platformy windowsazure. Management. Network. models. EffectiveRouteTable, Microsoft.> platformy windowsazure</span><span class="sxs-lookup"><span data-stu-id="93aa3-139">System.Collections.Generic.IEnumerable<Microsoft.WindowsAzure.Management.Network.Models.EffectiveRouteTable, Microsoft.WindowsAzure.Management.Network></span></span>

## <span data-ttu-id="93aa3-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93aa3-140">NOTES</span></span>

## <span data-ttu-id="93aa3-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93aa3-141">RELATED LINKS</span></span>

[<span data-ttu-id="93aa3-142">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="93aa3-142">Get-AzureRouteTable</span></span>](./Get-AzureRouteTable.md)

[<span data-ttu-id="93aa3-143">Nowe — AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="93aa3-143">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="93aa3-144">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="93aa3-144">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)

[<span data-ttu-id="93aa3-145">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="93aa3-145">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="93aa3-146">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="93aa3-146">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


