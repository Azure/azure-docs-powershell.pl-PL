---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 8f2d061fa67ed8e588ae162fbf7bd0a094ae6b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544447"
---
# <span data-ttu-id="9467a-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9467a-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="9467a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9467a-102">SYNOPSIS</span></span>
<span data-ttu-id="9467a-103">Usuwa konfigurację interfejsu sieciowego z VMSS.</span><span class="sxs-lookup"><span data-stu-id="9467a-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9467a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9467a-104">SYNTAX</span></span>

### <span data-ttu-id="9467a-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9467a-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9467a-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9467a-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Id] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9467a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9467a-107">DESCRIPTION</span></span>
<span data-ttu-id="9467a-108">Polecenie cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** usuwa konfigurację interfejsu sieciowego z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9467a-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="9467a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9467a-109">EXAMPLES</span></span>

### <span data-ttu-id="9467a-110">Przykład 1: Usuwanie konfiguracji interfejsu</span><span class="sxs-lookup"><span data-stu-id="9467a-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="9467a-111">Pierwsze polecenie uzyskuje VMSS przy użyciu polecenia cmdlet Get-AzureRmVmss, a następnie zapisuje je w zmiennej $VMSS.</span><span class="sxs-lookup"><span data-stu-id="9467a-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="9467a-112">Drugie polecenie usuwa konfigurację interfejsu sieciowego o nazwie ContosoVmssInterface02 z zestawu w $VMSS.</span><span class="sxs-lookup"><span data-stu-id="9467a-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="9467a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9467a-113">PARAMETERS</span></span>

### <span data-ttu-id="9467a-114">-ID</span><span class="sxs-lookup"><span data-stu-id="9467a-114">-Id</span></span>
<span data-ttu-id="9467a-115">Określa identyfikator konfiguracji interfejsu sieciowego, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9467a-115">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9467a-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9467a-116">-Name</span></span>
<span data-ttu-id="9467a-117">Określa nazwę konfiguracji interfejsu sieciowego, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9467a-117">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9467a-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9467a-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9467a-119">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="9467a-119">Specifies the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9467a-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9467a-120">-Confirm</span></span>
<span data-ttu-id="9467a-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9467a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9467a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9467a-122">-WhatIf</span></span>
<span data-ttu-id="9467a-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9467a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9467a-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9467a-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9467a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9467a-125">CommonParameters</span></span>
<span data-ttu-id="9467a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9467a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9467a-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9467a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9467a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9467a-128">INPUTS</span></span>

### <span data-ttu-id="9467a-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9467a-129">None</span></span>
<span data-ttu-id="9467a-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9467a-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9467a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9467a-131">OUTPUTS</span></span>

## <span data-ttu-id="9467a-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9467a-132">NOTES</span></span>

## <span data-ttu-id="9467a-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9467a-133">RELATED LINKS</span></span>

[<span data-ttu-id="9467a-134">Dodaj-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9467a-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="9467a-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9467a-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


