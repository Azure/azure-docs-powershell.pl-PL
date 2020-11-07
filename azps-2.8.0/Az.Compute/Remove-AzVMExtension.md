---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 0925b526fa70718fbd648668f80af98882382f57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706257"
---
# <span data-ttu-id="e8677-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e8677-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="e8677-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8677-102">SYNOPSIS</span></span>
<span data-ttu-id="e8677-103">Usuwa rozszerzenie z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8677-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="e8677-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8677-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8677-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8677-105">DESCRIPTION</span></span>
<span data-ttu-id="e8677-106">Polecenie cmdlet **Remove-AzVMExtension** usuwa rozszerzenie z rozszerzeń maszyny wirtualnej na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8677-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="e8677-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8677-107">EXAMPLES</span></span>

### <span data-ttu-id="e8677-108">Przykład 1: Usuwanie rozszerzenia z maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e8677-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="e8677-109">To polecenie usuwa rozszerzenie o nazwie ContosoTest z maszyny wirtualnej o nazwie VirtualMachine22 w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e8677-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="e8677-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8677-110">PARAMETERS</span></span>

### <span data-ttu-id="e8677-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8677-111">-DefaultProfile</span></span>
<span data-ttu-id="e8677-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8677-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8677-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e8677-113">-Force</span></span>
<span data-ttu-id="e8677-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e8677-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8677-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8677-115">-Name</span></span>
<span data-ttu-id="e8677-116">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8677-116">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8677-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8677-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8677-118">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e8677-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8677-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="e8677-119">-VMName</span></span>
<span data-ttu-id="e8677-120">Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie.</span><span class="sxs-lookup"><span data-stu-id="e8677-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8677-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8677-121">-Confirm</span></span>
<span data-ttu-id="e8677-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8677-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8677-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8677-123">-WhatIf</span></span>
<span data-ttu-id="e8677-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8677-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8677-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8677-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8677-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8677-126">CommonParameters</span></span>
<span data-ttu-id="e8677-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8677-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8677-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8677-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8677-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8677-129">INPUTS</span></span>

### <span data-ttu-id="e8677-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8677-130">System.String</span></span>

## <span data-ttu-id="e8677-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8677-131">OUTPUTS</span></span>

### <span data-ttu-id="e8677-132">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e8677-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e8677-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8677-133">NOTES</span></span>

## <span data-ttu-id="e8677-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8677-134">RELATED LINKS</span></span>

[<span data-ttu-id="e8677-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e8677-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="e8677-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e8677-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

