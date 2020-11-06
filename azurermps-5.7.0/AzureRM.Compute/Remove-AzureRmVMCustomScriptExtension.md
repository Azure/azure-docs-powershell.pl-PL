---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1e2dc6fe56cfaf182fb0614121ad9511edcfc2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544467"
---
# <span data-ttu-id="3fad7-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3fad7-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="3fad7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fad7-102">SYNOPSIS</span></span>
<span data-ttu-id="3fad7-103">Usuwa niestandardowe rozszerzenie skryptu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3fad7-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fad7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fad7-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fad7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3fad7-105">DESCRIPTION</span></span>
<span data-ttu-id="3fad7-106">Polecenie cmdlet **Remove-AzureRmVMCustomScriptExtension** usuwa rozszerzenie maszyny wirtualnej skryptu niestandardowego z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3fad7-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="3fad7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fad7-107">EXAMPLES</span></span>

## <span data-ttu-id="3fad7-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fad7-108">PARAMETERS</span></span>

### <span data-ttu-id="3fad7-109">-Force</span><span class="sxs-lookup"><span data-stu-id="3fad7-109">-Force</span></span>
<span data-ttu-id="3fad7-110">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3fad7-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3fad7-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3fad7-111">-Name</span></span>
<span data-ttu-id="3fad7-112">Określa nazwę niestandardowego rozszerzenia skryptu, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fad7-112">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3fad7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fad7-113">-ResourceGroupName</span></span>
<span data-ttu-id="3fad7-114">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3fad7-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3fad7-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="3fad7-115">-VMName</span></span>
<span data-ttu-id="3fad7-116">Określa nazwę maszyny wirtualnej, z poziomu której to polecenie cmdlet usuwa niestandardowe rozszerzenie skryptu.</span><span class="sxs-lookup"><span data-stu-id="3fad7-116">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="3fad7-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3fad7-117">-Confirm</span></span>
<span data-ttu-id="3fad7-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fad7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fad7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fad7-119">-WhatIf</span></span>
<span data-ttu-id="3fad7-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fad7-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3fad7-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3fad7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fad7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fad7-122">CommonParameters</span></span>
<span data-ttu-id="3fad7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fad7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fad7-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fad7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fad7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fad7-125">INPUTS</span></span>

### <span data-ttu-id="3fad7-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3fad7-126">None</span></span>
<span data-ttu-id="3fad7-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3fad7-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3fad7-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fad7-128">OUTPUTS</span></span>

## <span data-ttu-id="3fad7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fad7-129">NOTES</span></span>

## <span data-ttu-id="3fad7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fad7-130">RELATED LINKS</span></span>

[<span data-ttu-id="3fad7-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3fad7-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="3fad7-132">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3fad7-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
