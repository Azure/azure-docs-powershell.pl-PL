---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 8bead12111148d193e0e5dfe880ed3b28c6dcd01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893541"
---
# <span data-ttu-id="25d9d-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="25d9d-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="25d9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="25d9d-103">Usuwa niestandardowe rozszerzenie skryptu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="25d9d-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="25d9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25d9d-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25d9d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="25d9d-106">Polecenie cmdlet **Remove-AzVMCustomScriptExtension** usuwa rozszerzenie maszyny wirtualnej skryptu niestandardowego z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="25d9d-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="25d9d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25d9d-107">EXAMPLES</span></span>

## <span data-ttu-id="25d9d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25d9d-108">PARAMETERS</span></span>

### <span data-ttu-id="25d9d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d9d-109">-DefaultProfile</span></span>
<span data-ttu-id="25d9d-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25d9d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25d9d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="25d9d-111">-Force</span></span>
<span data-ttu-id="25d9d-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="25d9d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25d9d-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25d9d-113">-Name</span></span>
<span data-ttu-id="25d9d-114">Określa nazwę niestandardowego rozszerzenia skryptu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d9d-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d9d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d9d-115">-ResourceGroupName</span></span>
<span data-ttu-id="25d9d-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="25d9d-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d9d-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="25d9d-117">-VMName</span></span>
<span data-ttu-id="25d9d-118">Określa nazwę maszyny wirtualnej, z poziomu której to polecenie cmdlet usuwa niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="25d9d-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25d9d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25d9d-119">-Confirm</span></span>
<span data-ttu-id="25d9d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d9d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d9d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d9d-121">-WhatIf</span></span>
<span data-ttu-id="25d9d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d9d-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="25d9d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25d9d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d9d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d9d-124">CommonParameters</span></span>
<span data-ttu-id="25d9d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d9d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d9d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d9d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d9d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25d9d-127">INPUTS</span></span>

### <span data-ttu-id="25d9d-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="25d9d-128">None</span></span>
<span data-ttu-id="25d9d-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="25d9d-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25d9d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25d9d-130">OUTPUTS</span></span>

### <span data-ttu-id="25d9d-131">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="25d9d-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="25d9d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25d9d-132">NOTES</span></span>

## <span data-ttu-id="25d9d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25d9d-133">RELATED LINKS</span></span>

[<span data-ttu-id="25d9d-134">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="25d9d-134">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="25d9d-135">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="25d9d-135">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
