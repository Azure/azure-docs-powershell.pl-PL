---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: f99df428f99ec0e75eb4b1b220dde657be6f7458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525626"
---
# <span data-ttu-id="bd83d-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="bd83d-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="bd83d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd83d-102">SYNOPSIS</span></span>
<span data-ttu-id="bd83d-103">Usuwa rozszerzenie z VMSS.</span><span class="sxs-lookup"><span data-stu-id="bd83d-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd83d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd83d-104">SYNTAX</span></span>

### <span data-ttu-id="bd83d-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd83d-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd83d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd83d-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd83d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bd83d-107">DESCRIPTION</span></span>
<span data-ttu-id="bd83d-108">Polecenie cmdlet **Remove-AzureRmVmssExtension** usuwa rozszerzenie z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="bd83d-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="bd83d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd83d-109">EXAMPLES</span></span>

## <span data-ttu-id="bd83d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd83d-110">PARAMETERS</span></span>

### <span data-ttu-id="bd83d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd83d-111">-DefaultProfile</span></span>
<span data-ttu-id="bd83d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd83d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd83d-113">-ID</span><span class="sxs-lookup"><span data-stu-id="bd83d-113">-Id</span></span>
<span data-ttu-id="bd83d-114">Określa identyfikator rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="bd83d-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="bd83d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd83d-115">-Name</span></span>
<span data-ttu-id="bd83d-116">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="bd83d-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="bd83d-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bd83d-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bd83d-118">Określa VMSS, z którego ma zostać usunięte rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="bd83d-118">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="bd83d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd83d-119">-Confirm</span></span>
<span data-ttu-id="bd83d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd83d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd83d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd83d-121">-WhatIf</span></span>
<span data-ttu-id="bd83d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd83d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd83d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd83d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd83d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd83d-124">CommonParameters</span></span>
<span data-ttu-id="bd83d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd83d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd83d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd83d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd83d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd83d-127">INPUTS</span></span>

## <span data-ttu-id="bd83d-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd83d-128">OUTPUTS</span></span>

### <span data-ttu-id="bd83d-129">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="bd83d-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="bd83d-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd83d-130">NOTES</span></span>

## <span data-ttu-id="bd83d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd83d-131">RELATED LINKS</span></span>

[<span data-ttu-id="bd83d-132">Dodaj-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="bd83d-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
