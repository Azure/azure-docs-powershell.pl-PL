---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 58029017f4a6a272856f7badd6b09a9ba1f37ac3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706239"
---
# <span data-ttu-id="78e12-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="78e12-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="78e12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78e12-102">SYNOPSIS</span></span>
<span data-ttu-id="78e12-103">Usuwa konfigurację interfejsu sieciowego z VMSS.</span><span class="sxs-lookup"><span data-stu-id="78e12-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="78e12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78e12-104">SYNTAX</span></span>

### <span data-ttu-id="78e12-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e12-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78e12-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e12-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78e12-107">Opis</span><span class="sxs-lookup"><span data-stu-id="78e12-107">DESCRIPTION</span></span>
<span data-ttu-id="78e12-108">Polecenie cmdlet **Remove-AzVmssNetworkInterfaceConfiguration** usuwa konfigurację interfejsu sieciowego z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="78e12-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="78e12-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78e12-109">EXAMPLES</span></span>

### <span data-ttu-id="78e12-110">Przykład 1: Usuwanie konfiguracji interfejsu</span><span class="sxs-lookup"><span data-stu-id="78e12-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="78e12-111">Pierwsze polecenie uzyskuje VMSS przy użyciu polecenia cmdlet Get-AzVmss, a następnie zapisuje je w zmiennej $VMSS.</span><span class="sxs-lookup"><span data-stu-id="78e12-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="78e12-112">Drugie polecenie usuwa konfigurację interfejsu sieciowego o nazwie ContosoVmssInterface02 z zestawu w $VMSS.</span><span class="sxs-lookup"><span data-stu-id="78e12-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="78e12-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78e12-113">PARAMETERS</span></span>

### <span data-ttu-id="78e12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e12-114">-DefaultProfile</span></span>
<span data-ttu-id="78e12-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78e12-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e12-116">-ID</span><span class="sxs-lookup"><span data-stu-id="78e12-116">-Id</span></span>
<span data-ttu-id="78e12-117">Określa identyfikator konfiguracji interfejsu sieciowego, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78e12-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e12-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78e12-118">-Name</span></span>
<span data-ttu-id="78e12-119">Określa nazwę konfiguracji interfejsu sieciowego, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78e12-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78e12-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78e12-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="78e12-121">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="78e12-121">Specifies the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78e12-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78e12-122">-Confirm</span></span>
<span data-ttu-id="78e12-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78e12-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e12-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78e12-124">-WhatIf</span></span>
<span data-ttu-id="78e12-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78e12-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78e12-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78e12-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e12-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e12-127">CommonParameters</span></span>
<span data-ttu-id="78e12-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78e12-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e12-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78e12-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e12-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78e12-130">INPUTS</span></span>

### <span data-ttu-id="78e12-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78e12-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="78e12-132">System. String</span><span class="sxs-lookup"><span data-stu-id="78e12-132">System.String</span></span>

## <span data-ttu-id="78e12-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78e12-133">OUTPUTS</span></span>

### <span data-ttu-id="78e12-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78e12-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="78e12-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78e12-135">NOTES</span></span>

## <span data-ttu-id="78e12-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78e12-136">RELATED LINKS</span></span>

[<span data-ttu-id="78e12-137">Dodaj-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="78e12-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="78e12-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="78e12-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


