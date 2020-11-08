---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055314"
---
# <span data-ttu-id="cab5d-101">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="cab5d-101">Get-AzureIPForwarding</span></span>

## <span data-ttu-id="cab5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cab5d-102">SYNOPSIS</span></span>
<span data-ttu-id="cab5d-103">Pobiera stan przekierowywania IP.</span><span class="sxs-lookup"><span data-stu-id="cab5d-103">Gets the status of IP forwarding.</span></span>

## <span data-ttu-id="cab5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cab5d-104">SYNTAX</span></span>

### <span data-ttu-id="cab5d-105">IaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="cab5d-105">IaaSIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cab5d-106">SlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="cab5d-106">SlotIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cab5d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cab5d-107">DESCRIPTION</span></span>
<span data-ttu-id="cab5d-108">Polecenie cmdlet **Get-AzureIPForwarding** Pobiera stan przesyłania dalej IP.</span><span class="sxs-lookup"><span data-stu-id="cab5d-108">The **Get-AzureIPForwarding** cmdlet gets the status of IP forwarding.</span></span>

## <span data-ttu-id="cab5d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cab5d-109">EXAMPLES</span></span>

### <span data-ttu-id="cab5d-110">Przykład 1: pobieranie stanu przekierowywania adresów IP dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="cab5d-110">Example 1: Get IP forwarding status for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

<span data-ttu-id="cab5d-111">To polecenie pobiera maszynę wirtualną o nazwie ContosoVM06 dla usługi o nazwie ContosoService i przekazuje ten obiekt maszyny wirtualnej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cab5d-111">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="cab5d-112">Bieżące polecenie cmdlet uzyskuje stan przekierowywania IP dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="cab5d-112">The current cmdlet gets the status of IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="cab5d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cab5d-113">PARAMETERS</span></span>

### <span data-ttu-id="cab5d-114">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="cab5d-114">-NetworkInterfaceName</span></span>
<span data-ttu-id="cab5d-115">Określa nazwę karty sieciowej, dla której to polecenie cmdlet pobiera stan przekierowywania protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="cab5d-115">Specifies the name of the network adapter for which this cmdlet gets IP forwarding status.</span></span>

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

### <span data-ttu-id="cab5d-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="cab5d-116">-Profile</span></span>
<span data-ttu-id="cab5d-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cab5d-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="cab5d-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="cab5d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cab5d-119">-Rolename</span><span class="sxs-lookup"><span data-stu-id="cab5d-119">-RoleName</span></span>
<span data-ttu-id="cab5d-120">Określa nazwę roli PaaS, dla której to polecenie cmdlet pobiera stan przekierowywania protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="cab5d-120">Specifies the name of a PaaS role for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab5d-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cab5d-121">-ServiceName</span></span>
<span data-ttu-id="cab5d-122">Określa nazwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="cab5d-122">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="cab5d-123">Rola PaaS należy do usługi, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cab5d-123">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="cab5d-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="cab5d-124">-Slot</span></span>
<span data-ttu-id="cab5d-125">Określa gniazdo PaaS.</span><span class="sxs-lookup"><span data-stu-id="cab5d-125">Specifies a PaaS slot.</span></span>
<span data-ttu-id="cab5d-126">Rola PaaS, dla której to polecenie cmdlet pobiera stan przekazania, ma miejsce określone przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cab5d-126">The PaaS role for which this cmdlet gets forwarding status has the slot that this parameter specifies.</span></span>
<span data-ttu-id="cab5d-127">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="cab5d-127">Valid values are:</span></span> 

- <span data-ttu-id="cab5d-128">BOM</span><span class="sxs-lookup"><span data-stu-id="cab5d-128">Production</span></span>
- <span data-ttu-id="cab5d-129">Most</span><span class="sxs-lookup"><span data-stu-id="cab5d-129">Staging</span></span> 

<span data-ttu-id="cab5d-130">Wartością domyślną jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="cab5d-130">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab5d-131">-VM</span><span class="sxs-lookup"><span data-stu-id="cab5d-131">-VM</span></span>
<span data-ttu-id="cab5d-132">Określa obiekt maszyny wirtualnej, dla którego to polecenie cmdlet pobiera stan przekierowywania protokołu IP.</span><span class="sxs-lookup"><span data-stu-id="cab5d-132">Specifies the virtual machine object for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cab5d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab5d-133">CommonParameters</span></span>
<span data-ttu-id="cab5d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab5d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab5d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab5d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab5d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cab5d-136">INPUTS</span></span>

## <span data-ttu-id="cab5d-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cab5d-137">OUTPUTS</span></span>

### <span data-ttu-id="cab5d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cab5d-138">System.String</span></span>

## <span data-ttu-id="cab5d-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cab5d-139">NOTES</span></span>

## <span data-ttu-id="cab5d-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cab5d-140">RELATED LINKS</span></span>

[<span data-ttu-id="cab5d-141">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="cab5d-141">Set-AzureIPForwarding</span></span>](./Set-AzureIPForwarding.md)


