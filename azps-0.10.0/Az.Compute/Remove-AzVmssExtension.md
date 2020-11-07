---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 8044be4e6d9c353dd50420fe73066a8f47d53855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893481"
---
# <span data-ttu-id="fb9d9-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fb9d9-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="fb9d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9d9-103">Usuwa rozszerzenie z VMSS.</span><span class="sxs-lookup"><span data-stu-id="fb9d9-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="fb9d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb9d9-104">SYNTAX</span></span>

### <span data-ttu-id="fb9d9-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb9d9-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9d9-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb9d9-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb9d9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fb9d9-107">DESCRIPTION</span></span>
<span data-ttu-id="fb9d9-108">Polecenie cmdlet **Remove-AzVmssExtension** usuwa rozszerzenie z zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fb9d9-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="fb9d9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb9d9-109">EXAMPLES</span></span>

### <span data-ttu-id="fb9d9-110">Przykład 1: Usuwanie rozszerzenia z VMSS</span><span class="sxs-lookup"><span data-stu-id="fb9d9-110">Example 1: Remove extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

## <span data-ttu-id="fb9d9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb9d9-111">PARAMETERS</span></span>

### <span data-ttu-id="fb9d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9d9-112">-DefaultProfile</span></span>
<span data-ttu-id="fb9d9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb9d9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb9d9-114">-ID</span><span class="sxs-lookup"><span data-stu-id="fb9d9-114">-Id</span></span>
<span data-ttu-id="fb9d9-115">Określa identyfikator rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="fb9d9-115">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="fb9d9-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fb9d9-116">-Name</span></span>
<span data-ttu-id="fb9d9-117">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet z VMSS.</span><span class="sxs-lookup"><span data-stu-id="fb9d9-117">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="fb9d9-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fb9d9-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fb9d9-119">Określa VMSS, z którego ma zostać usunięte rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="fb9d9-119">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="fb9d9-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fb9d9-120">-Confirm</span></span>
<span data-ttu-id="fb9d9-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb9d9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb9d9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb9d9-122">-WhatIf</span></span>
<span data-ttu-id="fb9d9-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb9d9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb9d9-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fb9d9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb9d9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9d9-125">CommonParameters</span></span>
<span data-ttu-id="fb9d9-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb9d9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9d9-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb9d9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9d9-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb9d9-128">INPUTS</span></span>

### <span data-ttu-id="fb9d9-129">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fb9d9-129">VirtualMachineScaleSet</span></span>
<span data-ttu-id="fb9d9-130">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="fb9d9-130">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="fb9d9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb9d9-131">OUTPUTS</span></span>

### <span data-ttu-id="fb9d9-132">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fb9d9-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="fb9d9-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb9d9-133">NOTES</span></span>

## <span data-ttu-id="fb9d9-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb9d9-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb9d9-135">Dodaj-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fb9d9-135">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
