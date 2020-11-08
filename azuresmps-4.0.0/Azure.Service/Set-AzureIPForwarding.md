---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054922"
---
# <span data-ttu-id="52dbe-101">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="52dbe-101">Set-AzureIPForwarding</span></span>

## <span data-ttu-id="52dbe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="52dbe-103">Włącza lub wyłącza przesyłanie dalej protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="52dbe-103">Enables or disables IP forwarding.</span></span>

## <span data-ttu-id="52dbe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52dbe-104">SYNTAX</span></span>

### <span data-ttu-id="52dbe-105">EnableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="52dbe-105">EnableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="52dbe-106">DisableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="52dbe-106">DisableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="52dbe-107">EnableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="52dbe-107">EnableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="52dbe-108">DisableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="52dbe-108">DisableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="52dbe-109">Opis</span><span class="sxs-lookup"><span data-stu-id="52dbe-109">DESCRIPTION</span></span>
<span data-ttu-id="52dbe-110">Polecenie cmdlet **Set-AzureIPForwarding** włącza lub wyłącza przekierowywanie IP dla maszyny wirtualnej, na platformie jako rolę usługi (PaaS) lub kartę sieciową, która należy do maszyny wirtualnej lub PaaS roli.</span><span class="sxs-lookup"><span data-stu-id="52dbe-110">The **Set-AzureIPForwarding** cmdlet enables or disables IP forwarding for a virtual machine, for a platform as a service (PaaS) role, or a network adapter that belongs to a virtual machine or PaaS role.</span></span>

## <span data-ttu-id="52dbe-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52dbe-111">EXAMPLES</span></span>

### <span data-ttu-id="52dbe-112">Przykład 1: Włączanie przekierowywania protokołu IP dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="52dbe-112">Example 1: Enable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

<span data-ttu-id="52dbe-113">To polecenie pobiera maszynę wirtualną o nazwie ContosoVM06 dla usługi o nazwie ContosoService i przekazuje ten obiekt maszyny wirtualnej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52dbe-113">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="52dbe-114">Bieżące polecenie cmdlet włącza przesyłanie dalej protokołu IP dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52dbe-114">The current cmdlet enables IP forwarding for that virtual machine.</span></span>

### <span data-ttu-id="52dbe-115">Przykład 2: wyłączanie przesyłania dalej adresów IP dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="52dbe-115">Example 2: Disable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

<span data-ttu-id="52dbe-116">To polecenie pobiera maszynę wirtualną o nazwie ContosoVM06 dla usługi o nazwie ContosoService i przekazuje ten obiekt maszyny wirtualnej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52dbe-116">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="52dbe-117">Bieżące polecenie cmdlet wyłącza przesyłanie dalej adresów IP dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="52dbe-117">The current cmdlet disables IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="52dbe-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52dbe-118">PARAMETERS</span></span>

### <span data-ttu-id="52dbe-119">-Disable</span><span class="sxs-lookup"><span data-stu-id="52dbe-119">-Disable</span></span>
<span data-ttu-id="52dbe-120">Wskazuje, że ten aplet polecenia wyłącza przesyłanie dalej protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="52dbe-120">Indicates that this cmdlet disables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52dbe-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="52dbe-121">-Enable</span></span>
<span data-ttu-id="52dbe-122">Wskazuje, że to polecenie cmdlet umożliwia przesyłanie dalej protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="52dbe-122">Indicates that this cmdlet enables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52dbe-123">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="52dbe-123">-NetworkInterfaceName</span></span>
<span data-ttu-id="52dbe-124">Określa nazwę karty sieciowej, na której to polecenie cmdlet określa przekierowywanie IP.</span><span class="sxs-lookup"><span data-stu-id="52dbe-124">Specifies the name of the network adapter on which this cmdlet sets IP forwarding.</span></span>

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

### <span data-ttu-id="52dbe-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52dbe-125">-PassThru</span></span>
<span data-ttu-id="52dbe-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="52dbe-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52dbe-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="52dbe-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52dbe-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="52dbe-128">-Profile</span></span>
<span data-ttu-id="52dbe-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52dbe-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52dbe-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="52dbe-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52dbe-131">-Rolename</span><span class="sxs-lookup"><span data-stu-id="52dbe-131">-RoleName</span></span>
<span data-ttu-id="52dbe-132">Określa nazwę roli PaaS, na której to polecenie cmdlet ustawia przekierowywanie IP.</span><span class="sxs-lookup"><span data-stu-id="52dbe-132">Specifies the name of a PaaS role on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52dbe-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="52dbe-133">-ServiceName</span></span>
<span data-ttu-id="52dbe-134">Określa nazwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="52dbe-134">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="52dbe-135">Rola PaaS należy do usługi, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="52dbe-135">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="52dbe-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="52dbe-136">-Slot</span></span>
<span data-ttu-id="52dbe-137">Określa gniazdo PaaS.</span><span class="sxs-lookup"><span data-stu-id="52dbe-137">Specifies a PaaS slot.</span></span>
<span data-ttu-id="52dbe-138">Rola PaaS, dla której to ustawienie cmdlet przesyła dalej, ma miejsce określone przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="52dbe-138">The PaaS role for which this cmdlet sets forwarding has the slot that this parameter specifies.</span></span>
<span data-ttu-id="52dbe-139">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="52dbe-139">Valid values are:</span></span>

- <span data-ttu-id="52dbe-140">BOM</span><span class="sxs-lookup"><span data-stu-id="52dbe-140">Production</span></span>
- <span data-ttu-id="52dbe-141">Most</span><span class="sxs-lookup"><span data-stu-id="52dbe-141">Staging</span></span>

<span data-ttu-id="52dbe-142">Wartością domyślną jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="52dbe-142">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52dbe-143">-VM</span><span class="sxs-lookup"><span data-stu-id="52dbe-143">-VM</span></span>
<span data-ttu-id="52dbe-144">Określa obiekt maszyny wirtualnej, na którym ten aplet cmdlet ustawia przekierowywanie IP.</span><span class="sxs-lookup"><span data-stu-id="52dbe-144">Specifies the virtual machine object on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52dbe-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52dbe-145">CommonParameters</span></span>
<span data-ttu-id="52dbe-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52dbe-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52dbe-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52dbe-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52dbe-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52dbe-148">INPUTS</span></span>

## <span data-ttu-id="52dbe-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52dbe-149">OUTPUTS</span></span>

### <span data-ttu-id="52dbe-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52dbe-150">System.Boolean</span></span>

## <span data-ttu-id="52dbe-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52dbe-151">NOTES</span></span>

## <span data-ttu-id="52dbe-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52dbe-152">RELATED LINKS</span></span>

[<span data-ttu-id="52dbe-153">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="52dbe-153">Get-AzureIPForwarding</span></span>](./Get-AzureIPForwarding.md)
