---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 16095113dcc0604bfb7b739b1227db337a0cf6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544475"
---
# <span data-ttu-id="299ba-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="299ba-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="299ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="299ba-102">SYNOPSIS</span></span>
<span data-ttu-id="299ba-103">Usuwa rozszerzenie VMAccess z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="299ba-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="299ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="299ba-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="299ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="299ba-105">DESCRIPTION</span></span>
<span data-ttu-id="299ba-106">Polecenie cmdlet **Remove-AzureRmVMAccessExtension** usuwa rozszerzenie maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess) z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="299ba-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="299ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="299ba-107">EXAMPLES</span></span>

## <span data-ttu-id="299ba-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="299ba-108">PARAMETERS</span></span>

### <span data-ttu-id="299ba-109">-Force</span><span class="sxs-lookup"><span data-stu-id="299ba-109">-Force</span></span>
<span data-ttu-id="299ba-110">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="299ba-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="299ba-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="299ba-111">-Name</span></span>
<span data-ttu-id="299ba-112">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="299ba-112">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="299ba-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="299ba-113">-ResourceGroupName</span></span>
<span data-ttu-id="299ba-114">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="299ba-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="299ba-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="299ba-115">-VMName</span></span>
<span data-ttu-id="299ba-116">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="299ba-116">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="299ba-117">To polecenie cmdlet usuwa VMAccess dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="299ba-117">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="299ba-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="299ba-118">-Confirm</span></span>
<span data-ttu-id="299ba-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="299ba-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="299ba-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="299ba-120">-WhatIf</span></span>
<span data-ttu-id="299ba-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="299ba-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="299ba-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="299ba-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="299ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299ba-123">CommonParameters</span></span>
<span data-ttu-id="299ba-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="299ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299ba-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="299ba-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299ba-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="299ba-126">INPUTS</span></span>

### <span data-ttu-id="299ba-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="299ba-127">None</span></span>
<span data-ttu-id="299ba-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="299ba-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="299ba-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="299ba-129">OUTPUTS</span></span>

## <span data-ttu-id="299ba-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="299ba-130">NOTES</span></span>

## <span data-ttu-id="299ba-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="299ba-131">RELATED LINKS</span></span>

[<span data-ttu-id="299ba-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="299ba-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="299ba-133">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="299ba-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="299ba-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="299ba-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
