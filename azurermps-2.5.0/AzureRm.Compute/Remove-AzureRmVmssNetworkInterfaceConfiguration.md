---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
ms.openlocfilehash: 46058901188b99eb30d088e2ea784fdc0df8d782
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899142"
---
# <span data-ttu-id="64a98-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="64a98-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="64a98-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64a98-102">SYNOPSIS</span></span>
<span data-ttu-id="64a98-103">Usuwa konfigurację interfejsu sieciowego z VMSS.</span><span class="sxs-lookup"><span data-stu-id="64a98-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64a98-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64a98-104">SYNTAX</span></span>

### <span data-ttu-id="64a98-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64a98-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a98-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64a98-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64a98-107">Opis</span><span class="sxs-lookup"><span data-stu-id="64a98-107">DESCRIPTION</span></span>
<span data-ttu-id="64a98-108">Polecenie cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** usuwa konfigurację interfejsu sieciowego z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="64a98-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="64a98-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64a98-109">EXAMPLES</span></span>

### <span data-ttu-id="64a98-110">Przykład 1: Usuwanie konfiguracji interfejsu</span><span class="sxs-lookup"><span data-stu-id="64a98-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="64a98-111">Pierwsze polecenie uzyskuje VMSS przy użyciu polecenia cmdlet Get-AzureRmVmss, a następnie zapisuje je w zmiennej $VMSS.</span><span class="sxs-lookup"><span data-stu-id="64a98-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="64a98-112">Drugie polecenie usuwa konfigurację interfejsu sieciowego o nazwie ContosoVmssInterface02 z zestawu w $VMSS.</span><span class="sxs-lookup"><span data-stu-id="64a98-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="64a98-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64a98-113">PARAMETERS</span></span>

### <span data-ttu-id="64a98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a98-114">-DefaultProfile</span></span>
<span data-ttu-id="64a98-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64a98-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64a98-116">-ID</span><span class="sxs-lookup"><span data-stu-id="64a98-116">-Id</span></span>
<span data-ttu-id="64a98-117">Określa identyfikator konfiguracji interfejsu sieciowego, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a98-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="64a98-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64a98-118">-Name</span></span>
<span data-ttu-id="64a98-119">Określa nazwę konfiguracji interfejsu sieciowego, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a98-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="64a98-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64a98-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="64a98-121">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="64a98-121">Specifies the VMSS object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64a98-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64a98-122">-Confirm</span></span>
<span data-ttu-id="64a98-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a98-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a98-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a98-124">-WhatIf</span></span>
<span data-ttu-id="64a98-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a98-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64a98-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64a98-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a98-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a98-127">CommonParameters</span></span>
<span data-ttu-id="64a98-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a98-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a98-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64a98-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a98-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64a98-130">INPUTS</span></span>

### <span data-ttu-id="64a98-131">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64a98-131">VirtualMachineScaleSet</span></span>
<span data-ttu-id="64a98-132">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="64a98-132">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="64a98-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64a98-133">OUTPUTS</span></span>

### <span data-ttu-id="64a98-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="64a98-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="64a98-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64a98-135">NOTES</span></span>

## <span data-ttu-id="64a98-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64a98-136">RELATED LINKS</span></span>

[<span data-ttu-id="64a98-137">Dodaj-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="64a98-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="64a98-138">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="64a98-138">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


