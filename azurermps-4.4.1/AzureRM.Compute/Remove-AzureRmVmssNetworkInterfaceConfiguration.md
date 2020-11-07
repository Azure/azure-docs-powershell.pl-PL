---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 85f593c1d66b02f9982cecc4606603fbef1385d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716538"
---
# <span data-ttu-id="5bf85-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bf85-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="5bf85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5bf85-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf85-103">Usuwa konfigurację interfejsu sieciowego z VMSS.</span><span class="sxs-lookup"><span data-stu-id="5bf85-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bf85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5bf85-104">SYNTAX</span></span>

### <span data-ttu-id="5bf85-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bf85-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bf85-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bf85-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf85-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5bf85-107">DESCRIPTION</span></span>
<span data-ttu-id="5bf85-108">Polecenie cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** usuwa konfigurację interfejsu sieciowego z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5bf85-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5bf85-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5bf85-109">EXAMPLES</span></span>

### <span data-ttu-id="5bf85-110">Przykład 1: Usuwanie konfiguracji interfejsu</span><span class="sxs-lookup"><span data-stu-id="5bf85-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="5bf85-111">Pierwsze polecenie uzyskuje VMSS przy użyciu polecenia cmdlet Get-AzureRmVmss, a następnie zapisuje je w zmiennej $VMSS.</span><span class="sxs-lookup"><span data-stu-id="5bf85-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="5bf85-112">Drugie polecenie usuwa konfigurację interfejsu sieciowego o nazwie ContosoVmssInterface02 z zestawu w $VMSS.</span><span class="sxs-lookup"><span data-stu-id="5bf85-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="5bf85-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5bf85-113">PARAMETERS</span></span>

### <span data-ttu-id="5bf85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf85-114">-DefaultProfile</span></span>
<span data-ttu-id="5bf85-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bf85-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bf85-116">-ID</span><span class="sxs-lookup"><span data-stu-id="5bf85-116">-Id</span></span>
<span data-ttu-id="5bf85-117">Określa identyfikator konfiguracji interfejsu sieciowego, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf85-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5bf85-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5bf85-118">-Name</span></span>
<span data-ttu-id="5bf85-119">Określa nazwę konfiguracji interfejsu sieciowego, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf85-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5bf85-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5bf85-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5bf85-121">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="5bf85-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="5bf85-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5bf85-122">-Confirm</span></span>
<span data-ttu-id="5bf85-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf85-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf85-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf85-124">-WhatIf</span></span>
<span data-ttu-id="5bf85-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf85-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bf85-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5bf85-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf85-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf85-127">CommonParameters</span></span>
<span data-ttu-id="5bf85-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf85-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf85-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf85-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf85-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bf85-130">INPUTS</span></span>

## <span data-ttu-id="5bf85-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5bf85-131">OUTPUTS</span></span>

## <span data-ttu-id="5bf85-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5bf85-132">NOTES</span></span>

## <span data-ttu-id="5bf85-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bf85-133">RELATED LINKS</span></span>

[<span data-ttu-id="5bf85-134">Dodaj-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bf85-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="5bf85-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5bf85-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


