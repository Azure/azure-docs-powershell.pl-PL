---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 888ba66f1949a687228f5b9f2563c3d810c7cd5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893554"
---
# <span data-ttu-id="48b23-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="48b23-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="48b23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48b23-102">SYNOPSIS</span></span>
<span data-ttu-id="48b23-103">Usuwa rozszerzenie VMAccess z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="48b23-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="48b23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48b23-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48b23-105">Opis</span><span class="sxs-lookup"><span data-stu-id="48b23-105">DESCRIPTION</span></span>
<span data-ttu-id="48b23-106">Polecenie cmdlet **Remove-AzVMAccessExtension** usuwa rozszerzenie maszyny wirtualnej dostępu do maszyny wirtualnej (VMAccess) z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="48b23-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="48b23-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48b23-107">EXAMPLES</span></span>

## <span data-ttu-id="48b23-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48b23-108">PARAMETERS</span></span>

### <span data-ttu-id="48b23-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b23-109">-DefaultProfile</span></span>
<span data-ttu-id="48b23-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="48b23-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48b23-111">-Force</span><span class="sxs-lookup"><span data-stu-id="48b23-111">-Force</span></span>
<span data-ttu-id="48b23-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="48b23-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="48b23-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48b23-113">-Name</span></span>
<span data-ttu-id="48b23-114">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48b23-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="48b23-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48b23-115">-ResourceGroupName</span></span>
<span data-ttu-id="48b23-116">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="48b23-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="48b23-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="48b23-117">-VMName</span></span>
<span data-ttu-id="48b23-118">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="48b23-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="48b23-119">To polecenie cmdlet usuwa VMAccess dla maszyny wirtualnej, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="48b23-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="48b23-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48b23-120">-Confirm</span></span>
<span data-ttu-id="48b23-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48b23-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b23-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b23-122">-WhatIf</span></span>
<span data-ttu-id="48b23-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48b23-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="48b23-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="48b23-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48b23-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b23-125">CommonParameters</span></span>
<span data-ttu-id="48b23-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b23-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b23-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b23-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b23-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48b23-128">INPUTS</span></span>

### <span data-ttu-id="48b23-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="48b23-129">None</span></span>
<span data-ttu-id="48b23-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="48b23-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="48b23-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48b23-131">OUTPUTS</span></span>

### <span data-ttu-id="48b23-132">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="48b23-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="48b23-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48b23-133">NOTES</span></span>

## <span data-ttu-id="48b23-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48b23-134">RELATED LINKS</span></span>

[<span data-ttu-id="48b23-135">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="48b23-135">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="48b23-136">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="48b23-136">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="48b23-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="48b23-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
